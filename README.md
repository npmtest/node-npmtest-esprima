# npmtest-esprima

#### basic test coverage for  [esprima (v3.1.3)](http://esprima.org)  [![npm package](https://img.shields.io/npm/v/npmtest-esprima.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-esprima) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-esprima.svg)](https://travis-ci.org/npmtest/node-npmtest-esprima)

#### ECMAScript parsing infrastructure for multipurpose analysis

[![NPM](https://nodei.co/npm/esprima.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/esprima)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-esprima/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-esprima/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-esprima/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-esprima/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-esprima/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-esprima/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-esprima/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-esprima/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-esprima/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-esprima/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-esprima/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-esprima/build/test-report.html](https://npmtest.github.io/node-npmtest-esprima/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-esprima/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-esprima/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-esprima/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-esprima/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-esprima/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-esprima/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-esprima/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-esprima/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Ariya Hidayat"
    },
    "bin": {
        "esparse": "./bin/esparse.js",
        "esvalidate": "./bin/esvalidate.js"
    },
    "bugs": {
        "url": "https://github.com/jquery/esprima/issues"
    },
    "dependencies": {},
    "description": "ECMAScript parsing infrastructure for multipurpose analysis",
    "devDependencies": {
        "codecov.io": "~0.1.6",
        "escomplex-js": "1.2.0",
        "everything.js": "~1.0.3",
        "glob": "~7.1.0",
        "istanbul": "~0.4.0",
        "json-diff": "~0.3.1",
        "karma": "~1.3.0",
        "karma-chrome-launcher": "~2.0.0",
        "karma-detect-browsers": "~2.1.0",
        "karma-firefox-launcher": "~1.0.0",
        "karma-ie-launcher": "~1.0.0",
        "karma-mocha": "~1.2.0",
        "karma-safari-launcher": "~1.0.0",
        "karma-sauce-launcher": "~1.0.0",
        "lodash": "~3.10.1",
        "mocha": "~3.1.0",
        "node-tick-processor": "~0.0.2",
        "regenerate": "~1.3.1",
        "temp": "~0.8.3",
        "tslint": "~3.15.1",
        "typescript": "~1.8.10",
        "typescript-formatter": "~2.3.0",
        "unicode-8.0.0": "~0.7.0",
        "webpack": "~1.13.2"
    },
    "directories": {},
    "dist": {
        "shasum": "fdca51cee6133895e3c88d535ce49dbff62a4633",
        "tarball": "https://registry.npmjs.org/esprima/-/esprima-3.1.3.tgz"
    },
    "engines": {
        "node": ">=4"
    },
    "files": [
        "bin",
        "dist/esprima.js"
    ],
    "gitHead": "cd5909280f363d503142cb79077ec532132d9749",
    "homepage": "http://esprima.org",
    "keywords": [
        "ast",
        "ecmascript",
        "esprima",
        "javascript",
        "parser",
        "syntax"
    ],
    "license": "BSD-2-Clause",
    "main": "dist/esprima.js",
    "maintainers": [
        {
            "name": "ariya"
        }
    ],
    "name": "esprima",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/jquery/esprima.git"
    },
    "scripts": {
        "all-tests": "npm run generate-fixtures && npm run unit-tests && npm run api-tests && npm run grammar-tests && npm run regression-tests && npm run hostile-env-tests",
        "analyze-coverage": "istanbul cover test/unit-tests.js",
        "api-tests": "mocha -R dot test/api-tests.js",
        "appveyor": "npm run compile && npm run all-tests && npm run browser-tests",
        "benchmark": "npm run benchmark-parser && npm run benchmark-tokenizer",
        "benchmark-parser": "node -expose_gc test/benchmark-parser.js",
        "benchmark-tokenizer": "node --expose_gc test/benchmark-tokenizer.js",
        "browser-tests": "npm run compile && npm run generate-fixtures && cd test && karma start --single-run",
        "check-coverage": "istanbul check-coverage --statement 100 --branch 100 --function 100",
        "check-version": "node test/check-version.js",
        "circleci": "npm test && npm run codecov && npm run downstream",
        "code-style": "tsfmt --verify src/*.ts && tsfmt --verify test/*.js",
        "codecov": "istanbul report cobertura && codecov < ./coverage/cobertura-coverage.xml",
        "compile": "tsc -p src/ && webpack && node tools/fixupbundle.js",
        "complexity": "node test/check-complexity.js",
        "downstream": "node test/downstream.js",
        "droneio": "npm run compile && npm run all-tests && npm run saucelabs",
        "dynamic-analysis": "npm run analyze-coverage && npm run check-coverage",
        "format-code": "tsfmt -r src/*.ts && tsfmt -r test/*.js",
        "generate-fixtures": "node tools/generate-fixtures.js",
        "generate-regex": "node tools/generate-identifier-regex.js",
        "generate-xhtml-entities": "node tools/generate-xhtml-entities.js",
        "grammar-tests": "node test/grammar-tests.js",
        "hostile-env-tests": "node test/hostile-environment-tests.js",
        "prepublish": "npm run compile",
        "profile": "node --prof test/profile.js && mv isolate*.log v8.log && node-tick-processor",
        "regression-tests": "node test/regression-tests.js",
        "saucelabs": "npm run saucelabs-evergreen && npm run saucelabs-ie && npm run saucelabs-safari",
        "saucelabs-evergreen": "cd test && karma start saucelabs-evergreen.conf.js",
        "saucelabs-ie": "cd test && karma start saucelabs-ie.conf.js",
        "saucelabs-safari": "cd test && karma start saucelabs-safari.conf.js",
        "static-analysis": "npm run check-version && npm run tslint && npm run code-style && npm run complexity",
        "test": "npm run compile && npm run all-tests && npm run static-analysis && npm run dynamic-analysis",
        "travis": "npm test",
        "tslint": "tslint src/*.ts",
        "unit-tests": "node test/unit-tests.js"
    },
    "version": "3.1.3"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
