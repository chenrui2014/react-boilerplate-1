# React Boilerplate

[![license](https://img.shields.io/badge/license-MIT-red.svg?style=flat)](https://github.com/jgunnison/react-boilerplate/blob/master/LICENSE.md)
[![Build Status](https://circleci.com/gh/jgunnison/react-boilerplate.svg?style=shield)](https://circleci.com/gh/jgunnison/react-boilerplate)
[![dependencies Status](https://david-dm.org/jgunnison/react-boilerplate/status.svg)](https://david-dm.org/jgunnison/react-boilerplate)
[![devDependencies Status](https://david-dm.org/jgunnison/react-boilerplate/dev-status.svg)](https://david-dm.org/jgunnison/react-boilerplate?type=dev)
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Fjgunnison%2Freact-boilerplate.svg?type=shield)](https://app.fossa.io/projects/git%2Bgithub.com%2Fjgunnison%2Freact-boilerplate?ref=badge_shield)

[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
[![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/d20-compendium?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)

This is a React boilerplate with a bunch of features including linting for Sass/SCSS and ECMAScript with AirBnB's rules, Webpack Bundling and Minification, Jest Testing, PWA service worker generating, Offline packages with Yarn, and a Node server with Express for hosting.

[![React](/internals/img/react.png)](https://facebook.github.io/react/)
[![Webpack](/internals/img/webpack.png)](https://webpack.github.io/)
[![Redux](/internals/img/redux.png)](http://redux.js.org/)
[![React Router](/internals/img/react-router.png)](https://github.com/ReactTraining/react-router)
[![ESLint](/internals/img/eslint.png)](http://eslint.org/)
[![Jest](/internals/img/jest.png)](https://facebook.github.io/jest/)
[![Yarn](/internals/img/yarn.png)](https://yarnpkg.com/)

## Quick Start
1. Clone the Repo.
1. Navigate to the repo directory and install packages with `yarn`.
1. Start the development server with `yarn start`

## Initial Machine Setup
1. **Install [Node 6.x.x or greater](https://nodejs.org)**
1. **Install Yarn with `npm i -g yarn`**
1. **Install [Git](https://git-scm.com/downloads)**. 
1. **[Disable safe write in your editor](http://webpack.github.io/docs/webpack-dev-server.html#working-with-editors-ides-supporting-safe-write)** to assure hot reloading works properly.
1. On a Mac? You're all set. If you're on Linux or Windows, complete the steps for your OS below.  

**On Linux:**  

 * Run this to [increase the limit](http://stackoverflow.com/questions/16748737/grunt-watch-error-waiting-fatal-error-watch-enospc) on the number of files Linux will watch. [Here's why](https://github.com/coryhouse/react-slingshot/issues/6).    
`echo fs.inotify.max_user_watches=524288 | sudo tee -a /etc/sysctl.conf && sudo sysctl -p` 

**On Windows:** 

* **Install [Python 2.7](https://www.python.org/downloads/)**. Some node modules may rely on node-gyp, which requires Python on Windows.
* **Install C++ Compiler**. Browser-sync requires a C++ compiler on Windows. [Visual Studio Express](https://www.visualstudio.com/en-US/products/visual-studio-express-vs) comes bundled with a free C++ compiler. Or, if you already have Visual Studio installed: Open Visual Studio and go to File -> New -> Project -> Visual C++ -> Install Visual C++ Tools for Windows Desktop. The C++ compiler is used to compile browser-sync (and perhaps other Node modules).

## To Do
- Upgrade `why-did-you-update` to remove setter and resolve [this issue](https://github.com/garbles/why-did-you-update/issues/45).
- Add [prepack-webpack-plugin](https://github.com/gajus/prepack-webpack-plugin) once it's reached a stable build.
- Add [Coveralls](https://coveralls.io) for coverage reporting.

## Technologies

| **Tech** | **Description** |
|----------|-------|
| [React](https://facebook.github.io/react/)  |   Fast, composable client-side components.    |
| [Redux](http://redux.js.org) |  Enforces unidirectional data flows and immutable, hot reloadable store. Supports time-travel debugging. Lean alternative to [Facebook's Flux](https://facebook.github.io/flux/docs/overview.html).|
| [React Router](https://github.com/reactjs/react-router) | A complete routing library for React |
| [Babel](http://babeljs.io) |  Compiles ES6 to ES5. Enjoy the new version of JavaScript today.     |
| [Webpack](http://webpack.github.io) | Bundles npm packages and our JS into a single file. Includes hot reloading via [react-transform-hmr](https://www.npmjs.com/package/react-transform-hmr). |
| [Jest](https://facebook.github.io/jest/) | Automated tests with built-in expect assertions and [Enzyme](https://github.com/airbnb/enzyme) for DOM testing without a browser using Node. |
| [ESLint](http://eslint.org/)| Lint JS. Reports syntax and style issues. Using [eslint-plugin-react](https://github.com/yannickcr/eslint-plugin-react) for additional React specific linting rules. |
| [SASS](http://sass-lang.com/) | Compiled CSS styles with variables, functions, and more. |
| [PostCSS](https://github.com/postcss/postcss) | Transform styles with JS plugins. Used to autoprefix CSS |
| [BackstopJS](https://github.com/garris/BackstopJS)| Automated visual regression testing |
| [Editor Config](http://editorconfig.org) | Enforce consistent editor settings (spaces vs tabs, etc). | 

## Package.json Scripts
| **Script** | **Description** |
|----------|-------|
| jest | Runs Jest testing with the `--watch` flag for testing while developing. |
| test | Runs the Jest testing and outputs a code coverage report. |
| visual:init | Initializes BackstopJS's reference images for visual regression testing. |
| visual:test | Tests the BackstopJS reference images against the current server and reports differences. |
| scaffold:pure | Generates a Pure/Functional component template in the `client-src/components/` directory. |
| scaffold:class | Generates a Stateful/Smart component template in the `client-src/components/` directory. |
| scaffold:page | Generates a page template in the `client-src/pages/` directory. |
| stats | Builds the project and generates a `stats.json` file in the main directory to be review through [Webpack Visualizer](https://chrisbateman.github.io/webpack-visualizer/). |
| prebuild | Runs the `test` script before building the `client-src` directory with Webpack. |
| build | Builds the `client-src` directory for production with Webpack. |
| start | Starts the `webpack-dev-server` at port `3000` with HMR (hot modules replacement) for development. |
| server | Starts the `server.js` to host the `client` directory at port `8080` (be sure to run `build` first). |


## Creating Components
Just use one of the following commands. `yarn scaffold:class` for a Stateful/Smart component or `yarn scaffold:pure` for a Pure/Functional component. These commands will create components under the directory `client-src/components/` with everything you need to start coding.

A caveat to this is that you'll still need to import the Sass/SCSS manually in the `client-src/styles/styles.scss` file. But this allows you to manage the specificity of the component which will help in the long run.

## Visual Regression Testing
1. Build the `client` directory with `yarn build`.
1. Start the server on port `8080` with the command `yarn server`.
1. Collect the base images with `yarn visual:init`.
1. After completing your changes build the `client` directory and serve the Node server with the commands in steps 1 & 2.
1. Finally run the test with `yarn visual:test`.

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

### Writing Tools
- [Webstorm](https://www.jetbrains.com/webstorm/) (Integrated Development Environment)
- [VS Code](https://code.visualstudio.com/) (Lightweight Desktop Editor)

### Git GUI
- [GitKraken](https://www.gitkraken.com/)

### Redux Middleware
- [Thunk](https://github.com/gaearon/redux-thunk) (REST Projects)
- [Saga](https://github.com/redux-saga/redux-saga) (REST Large Projects)
- [Apollo](http://dev.apollodata.com/react/redux.html) (GraphQL Projects)
- [Redux Offline](https://github.com/jevakallio/redux-offline) (Offline-First Redux)

### Chrome Extensions

#### Accessibility
- [Accessibility Developer Tools](https://chrome.google.com/webstore/detail/accessibility-developer-t/fpkknkljclfencbdbgkenhalefipecmb)
- [aXe - Accessibility Testing](https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd)
- [Caret Browsing](https://chrome.google.com/webstore/detail/caret-browsing/fklpgenihifpccgiifchnihilipmbffg)
- [ChromeVox](https://chrome.google.com/webstore/detail/chromevox/kgejglhpjiefppelpmljglcjbhoiplfn)
- [Color Contrast Analyzer](https://chrome.google.com/webstore/detail/color-contrast-analyzer/dagdlcijhfbmgkjokkjicnnfimlebcll/related)
- [I want to see like the colour blind](https://chrome.google.com/webstore/detail/i-want-to-see-like-the-co/jebeedfnielkcjlcokhiobodkjjpbjia)
- [NoCoffee - Vision Simulator](https://chrome.google.com/webstore/detail/nocoffee/jjeeggmbnhckmgdhmgdckeigabjfbddl)
- [WAVE Evaluation Tool](https://chrome.google.com/webstore/detail/wave-evaluation-tool/jbbplnpkjmmeebjpijfedlgcdilocofh)

#### React & Redux
- [React Developer Tools](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi)
- [Redux DevTools](https://chrome.google.com/webstore/detail/redux-devtools/lmhkpmbekcpmknklioeibfkpmmfibljd)

#### Misc Tools
- [Baseliner](https://chrome.google.com/webstore/detail/baseliner/agoopbiflnjadjfbhimhlmcbgmdgldld)
- [Dimensions](https://chrome.google.com/webstore/detail/dimensions/baocaagndhipibgklemoalmkljaimfdj)
- [DOMListener](https://chrome.google.com/webstore/detail/domlistener/jlfdgnlpibogjanomigieemaembjeolj)
- [JSON Formatter](https://chrome.google.com/webstore/detail/json-formatter/bcjindcccaagfpapjjmafapmmgkkhgoa)
- [Lighthouse](https://chrome.google.com/webstore/detail/lighthouse/blipmdconlkpinefehnmjammfjpmpbjk)
- [Refined GitHub](https://chrome.google.com/webstore/detail/refined-github/hlepfoohegkhhmjieoechaddaejaokhf)
- [Tape](https://chrome.google.com/webstore/detail/tape/jmfleijdbicilompnnombcbkcgidbefb)
- [The Great Suspender](https://chrome.google.com/webstore/detail/the-great-suspender/klbibkeccnjlkjkiokjodocebajanakg)
- [Whatruns](https://chrome.google.com/webstore/detail/whatruns/cmkdbmfndkfgebldhnkbfhlneefdaaip/related)

### Fish Shell
1. Download at [fishshell.com/](https://fishshell.com/) and install.
1. Then install oh-my-fish with curl `curl -L https://get.oh-my.fish | fish`.
1. Finally set your theme in a new terminal window with `omf install toaster` and then the command `omf theme toaster`.

### Node version management
- [n](https://github.com/tj/n)

### Dependency Management
- [Yarn](https://yarnpkg.com/en/)

### Docker
- [Docker CE](https://www.docker.com/community-edition)
- [Docker Toolbox](https://www.docker.com/products/docker-toolbox)

### Image Optimization
- [ImageOptim for OS X](https://imageoptim.com/mac)
- [svgo](https://github.com/svg/svgo)

## Integrations/Services

### SSL/TLS Certificates
- [Let's Encrypt](https://letsencrypt.org/)

### Static Hosting
- [Cloudflare](https://www.cloudflare.com/) ($20/month)
- [Netlify](https://www.netlify.com) ($9/month)
- [Surge](http://surge.sh/) ($13/month)

### Cloud Hosting (not necessary)
- [Amazon EC2](https://aws.amazon.com/ec2) (pay as you go)
- [DigitalOcean](https://www.digitalocean.com) ($5 - $10/month)

### Continuous Integration/Deployment Services
- [CircleCI - CI/CD](https://circleci.com) ($50/month)
- [Travis CI - CI/CD](https://travis-ci.com/) ($69 - $129/month)
- [Buddy Works - CI/CD](https://buddy.works) ($49 - $99/month)
- [DeployBot - CD](https://deploybot.com/) ($15 - $25/month)

### Recommended BaaS
- [Graph.cool - GraphQL](https://www.graph.cool/) ($9/month)
- [Scaphold - GraphQL](https://scaphold.io/) ($8/month)
- [Firebase - REST (Schemaless)](https://firebase.google.com/) ($25/month)
- [GraphCMS - GraphQL CMS](https://graphcms.com/) ($29/month)
- [Prismic.io - CMS](https://prismic.io/) ($7 - $15/month)

### Testing Services
- [Ghost Inspector](https://ghostinspector.com/) (71/month)

### Video Hosting
- [Vimeo](https://vimeo.com/) ($7/month)
