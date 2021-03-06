# cra-lerna-electron

Minimal starter kit: ⚛️ [`create-react-app`](https://github.com/facebook/create-react-app) + 🐉 [`Lerna`](https://github.com/lerna/lerna) + :electron: [`Electron`](https://github.com/electron/electron)

## Getting Started

```bash
# Fetch this repo
git clone https://github.com/amaurym/cra-lerna-electron my-app
cd my-app

# Bootstrap the Lerna project, will install all modules
yarn install
```

## Folder structure

The main idea of this starer kit is to separate the Electron and React parts.

```
.
├── lerna.json                    # Config for Lerna
├── package.json                  # Package.json for the whole repo
├── packages/
│   ├── crale-electron/
│   │   ├── electron-builder.json # Config for electron-build
│   │   ├── electron-webpack.json # Config for electron-webpack
│   │   ├── dist/                 # Binaries bundles by electron-builder
│   │   ├── package.json
│   │   ├── src/
│   │   │   ├── main/             # Your electron app goes here
│   │   ├── static/               # Symlinks to ../crale-react/build/ folder
│   ├── crale-react
│   │   ├── build/                # The built app generated by CRA
│   │   ├── package.json
│   │   ├── src/                  # Your react app goes here
```

## Available Commands

All these commands should be run from the project root.

| Command         | Description                                                                                   |
| --------------- | --------------------------------------------------------------------------------------------- |
| `yarn start`    | Run Electron and React in dev mode, with live reload on file changes. Allows fast iterations. |
| `yarn build`    | Build Electron and React.                                                                     |
| `yarn electron` | Build Electron and React, and open Electron with these built files.                           |
| `yarn package`  | Build Electron and React, and generate binaries with these built files.                       |
| `yarn lint`     | Check for linting issues in the code.                                                         |
| `yarn test`     | Run tests.                                                                                    |

For the exhaustive list of available commands, check `package.json`.

## Tooling

| Tool                                                                        | Description                                                                     |
| --------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| [`create-react-app`](https://github.com/facebook/create-react-app)          | All tooling needed for React apps.                                              |
| [`lerna`](https://github.com/lerna/lerna)                                   | Manage JavaScript projects with multiple packages.                              |
| [`electron-webpack`](https://github.com/electron-userland/electron-webpack) | Scripts and configurations to compile Electron applications using webpack.      |
| [`electron-builder`]()                                                      | A complete solution to package and build a ready for distribution Electron app. |

## License

MIT.
