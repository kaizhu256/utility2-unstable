utility2 [![NPM](https://img.shields.io/npm/v/utility2.svg?style=flat-square)](https://www.npmjs.org/package/utility2)
========
lightweight nodejs module for testing and covering browser-side code



## demo server
[![heroku.com test server](https://kaizhu256.github.io/node-utility2/build.travis-ci.org/beta/test-report.screenshot.localNpmTest.phantomjs.png)](https://hrku01-utility2-beta.herokuapp.com/?modeTest=1)



## build status [![travis.ci-org build status](https://api.travis-ci.org/kaizhu256/node-utility2.svg)](https://travis-ci.org/kaizhu256/node-utility2)

[![build commit status](https://kaizhu256.github.io/node-utility2/build.badge.svg)](https://travis-ci.org/kaizhu256/node-utility2)

 git branch | test server | test report | coverage report | build artifact
:----------:|:-----------:|:-----------:|:---------------:|:--------------:
[master](https://github.com/kaizhu256/node-utility2/tree/master) | [![heroku.com test server](https://kaizhu256.github.io/node-utility2/heroku-logo.75x25.png)](https://hrku01-utility2-master.herokuapp.com/?modeTest=1) | [![test-report](https://kaizhu256.github.io/node-utility2/build.travis-ci.org/master/test-report.badge.svg)](https://kaizhu256.github.io/node-utility2/build.travis-ci.org/master/test-report.html) | [![istanbul coverage report](https://kaizhu256.github.io/node-utility2/build.travis-ci.org/master/coverage-report.badge.svg)](https://kaizhu256.github.io/node-utility2/build.travis-ci.org/master/coverage-report.html/node-utility2/index.html) | [![build artifacts](https://kaizhu256.github.io/node-utility2/glyphicons_144_folder_open.png)](https://github.com/kaizhu256/node-utility2/tree/gh-pages/build.travis-ci.org/master)
[beta](https://github.com/kaizhu256/node-utility2/tree/beta) | [![heroku.com test server](https://kaizhu256.github.io/node-utility2/heroku-logo.75x25.png)](https://hrku01-utility2-beta.herokuapp.com/?modeTest=1) | [![test-report](https://kaizhu256.github.io/node-utility2/build.travis-ci.org/beta/test-report.badge.svg)](https://kaizhu256.github.io/node-utility2/build.travis-ci.org/beta/test-report.html) | [![istanbul coverage report](https://kaizhu256.github.io/node-utility2/build.travis-ci.org/beta/coverage-report.badge.svg)](https://kaizhu256.github.io/node-utility2/build.travis-ci.org/beta/coverage-report.html/node-utility2/index.html) | [![build artifacts](https://kaizhu256.github.io/node-utility2/glyphicons_144_folder_open.png)](https://github.com/kaizhu256/node-utility2/tree/gh-pages/build.travis-ci.org/beta)
[alpha](https://github.com/kaizhu256/node-utility2/tree/alpha) | [![heroku.com test server](https://kaizhu256.github.io/node-utility2/heroku-logo.75x25.png)](https://hrku01-utility2-alpha.herokuapp.com/?modeTest=1) | [![test-report](https://kaizhu256.github.io/node-utility2/build.travis-ci.org/alpha/test-report.badge.svg)](https://kaizhu256.github.io/node-utility2/build.travis-ci.org/alpha/test-report.html) | [![istanbul coverage report](https://kaizhu256.github.io/node-utility2/build.travis-ci.org/alpha/coverage-report.badge.svg)](https://kaizhu256.github.io/node-utility2/build.travis-ci.org/alpha/coverage-report.html/node-utility2/index.html) | [![build artifacts](https://kaizhu256.github.io/node-utility2/glyphicons_144_folder_open.png)](https://github.com/kaizhu256/node-utility2/tree/gh-pages/build.travis-ci.org/alpha)



## installation and quickstart
```
# install
npm install utility2
# run server and browser tests on self with code-coverage
cd node_modules/utility2 && npm install && npm test
# start example test server on port 8080
npm start --server-port=8080
```



## library usage example
- see included ./example.js



## package content
- .build/
  - auto-created directory where tests and coverages are stored
- .gitignore
  - git ignore file
- .travis.yml
  - travis-ci config file
- Procfile
  - heroku deploy script
- README.md
  - readme file
- cli.sh
  - shell build script used by travis-ci to do the following:
    - run local phantomjs and slimerjs browser tests on local server
    - deploy to heroku after passing local browser tests
    - upload tests, coverages, screenshots, and other build artifacts to github
- example.data
  - example data file containing embedded resources for testing this app
- example.js
  - example nodejs script demonstrating how to use this app
- git-ssh.sh
  - ssh authentication hook used for heroku git deployment
- index.data
  - data file containing embedded resources for testing this app
- index.js
  - nodejs build script
- package.json
  - npm config file



## todo
- inline library usage example
- add grep in repl debugger
- add profiling
- add process.cwd to githubFilePut
- add server stress test using phantomjs
- minify /assets/utility2.js



## changelog
#### 2014.10.31
- add jsonCopy
- revamp server
- revamp phantomjs test
- revamp ajax
- add csslint
- emphasize low-level helper functions over high-level ones
- revert from saucelabs testing to phantomjs / slimerjs



#### 2014.9.22
- near 100% code-coverage during travis-ci build
- integrate codeship.io ci
- rename exports to mainApp
- remove global, exports, required, state, stateRestore from browser window
- add better error stack for browser ajax
- integrate code-coverage for browser initializations into _init_browser_test
- integrate code-coverage for nodejs initializations into _init_nodejs_test
- significantly increase code coverage
- add ajax timeout testing
- auto-detect slimerjs testing
- add url query-param feature modeErrorIgnore=1 to ignore test-simulated errors
- move main.* and utility2.* assets to /public/cache path
- fix code-coverage for failed tests
- remove global dependencies in nodejs env
- create ./build/test-report.xml for jenkins
- merge phantomjs and slimerjs dependencies into headless-browser package
- remove coverage.json when pushing build artifact to github

#### 2014.7.29
- add github basic auth for building private repo
- revamp ajax redirect in nodejs code
- integrate browser tests into main page
- add offline mode for shBuild
- add dummy failed tests in npm test for code-coverage
- add file update feature for data files
- add test flag in heroku Procfile
- add caching for scripts
- migrate from unstable -> master workflow to alpha -> beta -> master workflow
- add build commit badge in README.md
- merge node-utility2-data gh-pages repo into node-utility2
- add exportBrowserScript
- replace serving msin.data.js and main.js with {{name}}.data.js and {{name}}.js
- exit build on decrypt error
- add magic to auto-config state.repoGithub and state.repoHeroku
- enable testReportUpload only through command-line

#### 2014.7.18
- add description of files in README.md
- add code-coverage for saucelabs test routine
- automatically capture browser screenshots via phantomjs / slimerjs / saucelabs
- add basic auth for test-report upload
- rename exports.initLocal to exports.initSubmodule

#### 2014.7.12
- automate saucelabs testing in build

#### 2014.7.11
- add browser-side code-coverage
- automate phantomjs and slimerjs headless browser testing
- implement browser-side ajax
- update browser test-report status every 1000 ms until finished
- redirect main page to test.html
- watch and auto-jslint main.js and utility2.js

#### 2014.7.3
- initial commit
