# github_graphql_client
Learnt how to develop desktop application for linux using **flutter** through a codelab provided by the flutter team.

## Introduction
Flutter is Google's UI toolkit for building beautiful, natively compiled applications for mobile, web, and desktop from a single codebase. In the [codelab](https://codelabs.developers.google.com/codelabs/flutter-github-graphql-client), I built a Flutter desktop app that accesses GitHub APIs to retrieve your repositories, assigned issues, and pull requests. In accomplishing this task, I created and used plugins to interact with native APIs and desktop applications, and use code generation to build type safe client libraries for GitHub's APIs.

What I learnt
- How to create a Flutter desktop application
- How to authenticate using OAuth2 on desktop
- How to use GraphQL from Flutter with code generation
- How to create a Flutter plugin to integrate with native APIs

## Installation

For installin this Linux desktop application, you'll need:
- Clang
- CMake
- GTK development headers
- Ninja build
- pkg-config

Installing these requirements varies depending on which Linux distribution you are using, but the following is what you could use to install the above software on Ubuntu.
```bash
$ sudo apt-get install clang cmake ninja-build pkg-config libgtk-3-dev
```
**To register an application for GitHub's OAuth2 flow**, surf to [github.com](https://github.com) and follow the instructions in only the first step of GitHub's [Building OAuth Apps](https://docs.github.com/en/developers/apps/building-oauth-apps).

In completing [Creating an OAuth App](https://docs.github.com/en/developers/apps/creating-an-oauth-app), Step 8 asks you to provide the Authorization callback URL. For a desktop app, enter http://localhost/ as the callback URL. GitHub's OAuth2 flow was set up such that defining a localhost callback URL allows any port, enabling you to stand up a web server on an ephemeral local high port. This avoids asking the user to copy the OAuth code token into the application as part of the OAuth process.

Add client credentials to a new file, lib/github_oauth_credentials.dart, as follows:
```lib/github_oauth_credentials.dart```
```dart
// TODO(CodelabUser): Create an OAuth App
const githubClientId = 'YOUR_GITHUB_CLIENT_ID_HERE';
const githubClientSecret = 'YOUR_GITHUB_CLIENT_SECRET_HERE';

// OAuth scopes for repository and user information
const githubScopes = ['repo', 'read:org'];
```
Copy and paste your client credentials from the previous step into this file.