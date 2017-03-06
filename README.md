# workflowy-native-app

WorkFlowy is an awesome task manager/organizer todo-list do-everything do-anything web app. However, the only desktop offering they have is a Chrome app. Unfortunately, when using keyboard shortcuts (command + tab) to switch between applications, the WorkFlowy Chrome app and Chrome itself show and hide together and the behavior is clunky at best.

This project will help you create a native desktop WorkFlowy app. It uses [Electron](https://electron.atom.io/) and [`electron-packager`](https://github.com/electron-userland/electron-packager) to create a native app for your operating system (macOS, Windows or Linux). Internally, it renders the WorkFlowy web app. There is no offline support. However, it will correctly render external links in your browser, an improvement over another [similar solution](https://itunes.apple.com/us/app/workflowy-menuapp/id965079797?mt=12).

> NOTE: it appears WorkFlowy is [working on a native app for real](https://workflowy.zendesk.com/hc/en-us/articles/203295295-Offline-Apps), so this is a stopgap solution (without offline support).

## Prerequisites

[NodeJS](https://nodejs.org) version 4.0 or greater.

## Usage

Download or clone this repo and `cd` into the directory:

```
$ git clone git@github.com:kweiberth/workflowy-native-app.git
$ cd workflowy-native-app
```

Install the project dependencies and build the native app

```
$ npm install
$ npm run build
```

`electron-packager` will build the app specifically for your OS, and the output of the build process will be located in a folder in this current directory. In the case of macOS, you will see a folder called `WorkFlowy-darwin-x64`. Inside of this folder will be the `.app` application file called `WorkFlowy.app`. Copy this into your `Applications` folder, open it and you should be good to go! Once it's working, feel free to delete the cloned project from your computer. The `.app` file is all you need.

If you are a Windows or Linux user, the output of the build step and application file itself will be similar... but different. Hopefully you can figure it out 😬.
