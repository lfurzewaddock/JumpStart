
<div align="center">
  <!-- PR's Welcome -->
  <a href="http://makeapullrequest.com">
    <img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square"
      alt="PR's Welcome" />
  </a>
</div>

<h1 align="center">JumpStart</h1>

<div align="center">
  <strong>Write Code, Not Config</strong>
</div>
<div align="center">
  An ES6 module starter kit with everything you need, and nothing you don't.
</div>

## Table of Contents
- [Features](#features)
- [Philosophy](#philosophy)
- [Usage](#usage)
- [Installation](#installation)
- [Support](#support)

## Features
- __testable:__ built for TDD with hot-reloading, code coverage, and testing with [Mocha](https://mochajs.org/), [Chai](http://chaijs.com/), [Sinon](http://sinonjs.org), and [Istanbul](https://github.com/gotwarlost/istanbul)
- __isomorphic__: supports testing in both node and browsers with [jsdom](https://github.com/tmpvar/jsdom) for DOM emulation in tests
- __compatible__: write cutting-edge javascript and [Babel](https://babeljs.io/) will compile it for browsers
- __consistent__: uses [ESLint](https://eslint.org/) to detect syntax or style errors in your code
- __extendable__: built on [webpack](https://webpack.js.org/) and ready to be tailored to your needs

## Philosophy

JumpStart is built on the concept of [TDD](https://en.wikipedia.org/wiki/Test-driven_development). 
Writing tests should be easy, and you should be able to run them in any environment. 
Write a test, see it fail, write the code to make it pass, then rinse and repeat.

Are you at terminal warrior? JumpStart has you covered. Even if you are testing DOM functionality, you'll never have to leave the command line.

Do you want to verify your tests work in the browser? That's also supported out of the box.  

ESLint is configured as a Webpack loader ([eslint-loader](https://github.com/webpack-contrib/eslint-loader) accepts [ESLint CLIEngine](https://eslint.org/docs/developer-guide/nodejs-api#cliengine) options), so when Webpack runs, the source code is linted before Webpack will bundle it, forcing you to fix any issues, rather than ignoring them.


The provided `npm` commands will watch your source and automatically reload your tests so feedback is __automatic__ and __fast__, just like it should be.

## Usage

- `npm run tdd` 

    - runs mocha tests in `watch` mode so your tests get re-run when the source or tests change.
    - uses [mocha-webpack](https://www.npmjs.com/package/mocha-webpack), so only the tests that are affected by file changes will get run
    
    <p align="center">
      <img src="https://media.giphy.com/media/3ohs82WbHWookAhx16/giphy.gif">
    </p>

- `npm run tdd:web`

    - builds and opens webpage via `webpack-dev-server` that runs mocha tests in browser
    - rebuilds and re-runs tests if any relevant files change
    
    <p align="center">
      <img width="400px" src="https://i.imgur.com/vyWp0t5.png">
    </p>

- `npm test`

    - runs mocha tests, code coverage and outputs the results. 
    - Doesn't watch files or hot-reload.

- `npm run build`
    
    - builds your app bundle for production with both ugilification and minification

- `npm start`

    - builds your app in development mode and automatically serves it using `webpack-dev-server` and the template in `src/templates/index.html`

## Installation

1. Clone the repository into your "new-module" directory

    ```bash
    git clone https://github.com/lfurzewaddock/JumpStart.git new-module && cd new-module
    ```

2. Remove the git repository, and then initialize a new one

    ```bash
    rm -rf .git && git init
    ```

3. Remove README and replace with your own

    ```bash
    rm README.md && touch README.md
    ```

4. Update `package.json` and install dependencies

    ```bash
    npm init && npm install
    ```
    
    Don't forget to update the description any URL's in the `package.json` file.

5. Start coding!

## Support

If you find any problems or bugs, please open a new [issue](https://github.com/lfurzewaddock/JumpStart/issues).
