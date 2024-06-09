# Devcontainer Node 18

This repository contains a development environment for Node.js 18, packaged as a Docker container and configured for use with Visual Studio Code's Remote - Containers extension.

## Features

- Node.js 18 runtime
- Pre-installed global utilities: git, curl, wget, unzip, less, man-db, neovim, bash
- Starship shell prompt, with a custom configuration
- Forwarded port 3000 for web server development

## Usage

1. Install the [Remote - Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension in VS Code.
2. Open this repository in VS Code.
3. Press F1, then select "Remote-Containers: Reopen in Container".

## Customization

You can customize the development environment by modifying the Dockerfile or the devcontainer.json file.

For more information on using devcontainers in VS Code, see the [official documentation](https://code.visualstudio.com/docs/remote/containers).