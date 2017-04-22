# npmdoc-influx

#### api documentation for  [influx (v5.0.7)](https://github.com/node-influx/node-influx#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-influx.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-influx) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-influx.svg)](https://travis-ci.org/npmdoc/node-npmdoc-influx)

#### InfluxDB Client

[![NPM](https://nodei.co/npm/influx.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/influx)

- [https://npmdoc.github.io/node-npmdoc-influx/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-influx/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-influx/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-influx/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-influx/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-influx/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "bugs": {
        "url": "https://github.com/node-influx/node-influx/issues"
    },
    "contributors": [
        {
            "name": "Ben Evans",
            "url": "http://bensbit.co.uk"
        },
        {
            "name": "Connor Peet"
        },
        {
            "name": "Steffen Konerow",
            "url": "http://www.nrg-media.de"
        }
    ],
    "dependencies": {},
    "description": "InfluxDB Client",
    "devDependencies": {
        "@types/chai": "^3.4.34",
        "@types/mocha": "^2.2.32",
        "@types/node": "^6.0.45",
        "@types/sinon": "^1.16.31",
        "@types/sinon-chai": "^2.7.27",
        "awesome-typescript-loader": "^3.0.8",
        "chai": "^3.5.0",
        "coveralls": "^2.11.1",
        "esdoc": "^0.4.8",
        "istanbul": "^0.4.3",
        "json-loader": "^0.5.4",
        "karma": "^1.3.0",
        "karma-chrome-launcher": "^2.0.0",
        "karma-mocha": "^1.2.0",
        "karma-mocha-reporter": "^2.2.0",
        "karma-sauce-launcher": "^1.0.0",
        "karma-sourcemap-loader": "^0.3.7",
        "karma-webpack": "^2.0.2",
        "lodash": "^4.16.2",
        "mocha": "^3.1.0",
        "node-fetch": "^1.6.3",
        "npm-run-all": "^4.0.2",
        "opn-cli": "^3.1.0",
        "sinon": "^2.0.0-pre.3",
        "sinon-chai": "^2.8.0",
        "stream-http": "github:node-influx/stream-http",
        "ts-node": "^2.1.0",
        "tslint": "^4.5.1",
        "tslint-microsoft-contrib": "4.0.0",
        "typescript": "^2.2.1",
        "webpack": "^2.2.1"
    },
    "directories": {},
    "dist": {
        "shasum": "35e65f6bf13cbaa1763108b5596a806a727a529a",
        "tarball": "https://registry.npmjs.org/influx/-/influx-5.0.7.tgz"
    },
    "gitHead": "6f9e957262c392631e4570dfd25001e007f0927f",
    "homepage": "https://github.com/node-influx/node-influx#readme",
    "keywords": [
        "influx",
        "influxdb",
        "time",
        "series",
        "client",
        "db"
    ],
    "license": "MIT",
    "main": "./lib/src/index.js",
    "maintainers": [
        {
            "name": "bencevans"
        },
        {
            "name": "connor.peet"
        },
        {
            "name": "nichdiekuh"
        }
    ],
    "name": "influx",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/node-influx/node-influx.git"
    },
    "scripts": {
        "build:dist": "npm run clean && tsc && cp -R test/fixture lib/test",
        "build:doc": "npm run clean && tsc -m es2015 -t es6 --moduleResolution node && esdoc -c esdoc.json",
        "clean": "rm -rf coverage doc lib",
        "prepublish": "npm run clean && tsc -d",
        "test": "npm-run-all --parallel test:lint test:unit test:integrate",
        "test:browser": "karma start test/karma.conf.js",
        "test:cover": "npm run build:dist && istanbul cover _mocha -- lib/test/unit/*.test.js && opn coverage/lcov-report/index.html",
        "test:integrate": "mocha --compilers ts:ts-node/register --timeout 20000 test/integrate/*.test.ts",
        "test:lint": "tslint --type-check --project tsconfig.json '{src,test}/**/*.ts'",
        "test:sauce": "SAUCE=1 karma start test/karma.conf.js",
        "test:travis": "npm-run-all clean test:lint test:sauce test:integrate build:dist && istanbul cover _mocha --report lcovonly -- lib/test/unit/*.test.js",
        "test:unit": "mocha --compilers ts:ts-node/register test/unit/*.test.ts",
        "test:watch": "mocha -R min --watch --compilers ts:ts-node/register test/unit/*.test.ts"
    },
    "typings": "./lib/src/index",
    "version": "5.0.7",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
