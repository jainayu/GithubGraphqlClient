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