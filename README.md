# React Boilerplate

This is a React boilerplate with a bunch of features including linting for Sass/SCSS and ECMAScript with AirBnB's rules, Webpack Bundling and Minification, Jest Testing, PWA service worker generating, Offline packages with Yarn, and a Node server with Express for hosting.

## To Do
[ ] Get fix for `why-did-you-update` from [this issue](https://github.com/garbles/why-did-you-update/issues/45)

## Docker

### Docker Commands
- Build the Container: `bash ./manage.sh build`
- Run the Container: `bash ./manage.sh start`
- Start a terminal session in the Container: `bash ./manage.sh shell`
- Run a single command in your container: `bash ./manage.sh run <command>`

#### Helpful Commands:
- `docker container exec -it {container_name} /bin/bash` Attach shell.
- `docker image ls` List images.
- `docker container ls` List containers.

## Yarn Offline
To run [Yarn Offline](https://yarnpkg.com/blog/2016/11/24/offline-mirror/) just run `yarn install –offline` in your shell.

## Tools

### Chrome Extensions
- [React Developer Tools](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi)
- [Redux DevTools](https://chrome.google.com/webstore/detail/redux-devtools/lmhkpmbekcpmknklioeibfkpmmfibljd)
- [Lighthouse](https://chrome.google.com/webstore/detail/lighthouse/blipmdconlkpinefehnmjammfjpmpbjk)

### Fish Shell
1. Download at [fishshell.com/](https://fishshell.com/) and install.
1. Then install oh-my-fish with curl `curl -L https://get.oh-my.fish | fish`.
1. Finally set your theme in a new terminal window with `omf install toaster` and then the command `omf theme toaster`.
