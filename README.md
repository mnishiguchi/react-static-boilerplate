# React Static Boilerplate

Built on [React Static Boilerplate](https://github.com/koistya/react-static-boilerplate) by koistya, static website starter kit powered by [React.js](http://facebook.github.io/react/) and [Webpack](http://webpack.github.io/)


### Directory Layout

```shell
.
├── /build/                     # The folder for compiled output
├── /node_modules/              # 3rd-party libraries and utilities
├── /components/                # Shared/generic UI components
│   ├── /layout/                # Layout component
│   ├── /button/                # Button component
│   └── /...                    # etc.
├── /core/                      # Core framework
│   ├── /app.js                 # Application entry point (bootstrap)
│   ├── /store.js               # Application state manager (Redux)
│   └── /...                    # etc.
├── /routes/                    # View/screen UI components + routing information
│   ├── /about/                 # About page
│   ├── /error/                 # Error page
│   ├── /home/                  # Home page
│   └── /...                    # etc.
├── /static/                    # Static files such as favicon.ico etc.
├── /test/                      # Unit and integration tests
├── /tools/                     # Build automation scripts and utilities
│── LICENSE.txt                 # Licensing information
│── package.json                # The list of project dependencies and NPM scripts
└── README.md                   # Project overview / getting started guide
```


### Getting Started

Just clone the repo, install Node.js modules and run `npm start`:

```shell
$ git clone -o react-static-boilerplate -b master --single-branch \
      https://github.com/koistya/react-static-boilerplate.git MyApp
$ cd MyApp
$ npm install           # Install project dependencies listed in package.json
$ npm start             # Build and launch the app, same as "node tools/start.js"
```

**NODE**: Make sure that you have [Node.js](https://nodejs.org/) v6 installed on your local machine.

### How to Test

The unit tests are powered by [chai](http://chaijs.com/) and [mocha](http://mochajs.org/).

```shell
$ npm test
```


### How to Deploy

#### A: to GitHub Pages
- Great for a simple app without router.

```shell
$ npm run deploy-gh
```

#### B: to Surge
- [Surge](https://surge.sh/)
- [Routing doesn't work for github project pages](https://github.com/koistya/react-static-boilerplate/issues/58)


```bash
# Install surge
$ npm install --global surge
```

```bash
$ cd path/to/project
$ surge
```

```js
# package.json
...
  "scripts": {
    ...
    "deploy-surge": "npm build && surge -p build --domain <name-provided-by-surge>.surge.sh",
    ...
  }
...
```

```shell
$ npm run deploy-surge
```


Alternatively, you can build a production release to manually deploy to S3, Firebase, Netlify, and other static hosts. Simply run the command below and copy the generated `build` folder to your static host.

```shell
$ npm run build release         # Build production release
```


### How to Update

You can always fetch and merge the recent changes from this repo back into your own project:

```shell
$ git checkout master
$ git fetch react-static-boilerplate
$ git merge react-static-boilerplate/master
$ npm install
```

### Related Projects

* [React Starter Kit](https://github.com/kriasoft/react-starter-kit) — Isomorphic web app boilerplate (Node.js, React, GraphQL, Webpack, CSS Modules)
* [Babel Starter Kit](https://github.com/kriasoft/babel-starter-kit) — JavaScript library boilerplate (ES2015, Babel, Rollup, Mocha, Chai, Sinon, Rewire)
* [React App](https://github.com/kriasoft/react-app) — Bootstrap React app with routing, navigation, context variables and title/meta management
* [Universal Router](https://github.com/kriasoft/universal-router) — Isomorphic router for web and single-page applications (SPA)
* [History](https://github.com/mjackson/history) — HTML5 History API wrapper library
* [Membership Database](https://github.com/membership/membership.db) — SQL schema boilerplate for user accounts, roles and auth tokens


### Learn More

* [Getting Started with React.js](http://facebook.github.io/react/)
* [Getting Started with GraphQL and Relay](https://quip.com/oLxzA1gTsJsE)
* [React.js Questions on StackOverflow](http://stackoverflow.com/questions/tagged/reactjs)
* [React.js Discussion Board](https://discuss.reactjs.org/)
* [Learn ES6](https://babeljs.io/docs/learn-es6/), [ES6 Features](https://github.com/lukehoban/es6features#readme)


### License

Copyright © 2015-2016 Konstantin Tarkus. This source code is licensed under the MIT license found in the
[LICENSE.txt](https://github.com/koistya/react-static-boilerplate/blob/master/LICENSE.txt) file.
