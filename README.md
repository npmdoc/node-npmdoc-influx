# api documentation for  [influx (v5.0.6)](https://github.com/node-influx/node-influx#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-influx.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-influx) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-influx.svg)](https://travis-ci.org/npmdoc/node-npmdoc-influx)
#### InfluxDB Client

[![NPM](https://nodei.co/npm/influx.png?downloads=true)](https://www.npmjs.com/package/influx)

[![apidoc](https://npmdoc.github.io/node-npmdoc-influx/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-influx_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-influx/build/apidoc.html)

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
            "email": "ben@bensbit.co.uk",
            "url": "http://bensbit.co.uk"
        },
        {
            "name": "Connor Peet",
            "email": "connor@peet.io"
        },
        {
            "name": "Steffen Konerow",
            "email": "steffen@nrg-media.de",
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
        "tslint-microsoft-contrib": "^4.0.0",
        "typescript": "^2.2.1",
        "webpack": "^2.2.1"
    },
    "directories": {},
    "dist": {
        "shasum": "0173df1723a8056cf2e0e788a498236cba4b5a47",
        "tarball": "https://registry.npmjs.org/influx/-/influx-5.0.6.tgz"
    },
    "gitHead": "5572be20bd8d6625b07e00822026af7416848a91",
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
            "name": "bencevans",
            "email": "ben@bensbit.co.uk"
        },
        {
            "name": "connor.peet",
            "email": "connor@peet.io"
        },
        {
            "name": "nichdiekuh",
            "email": "steffen@nrg-media.de"
        }
    ],
    "name": "influx",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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
    "version": "5.0.6"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module influx](#apidoc.module.influx)
1.  [function <span class="apidocSignatureSpan">influx.</span>Expression ()](#apidoc.element.influx.Expression)
1.  [function <span class="apidocSignatureSpan">influx.</span>InfluxDB (options)](#apidoc.element.influx.InfluxDB)
1.  [function <span class="apidocSignatureSpan">influx.</span>Measurement ()](#apidoc.element.influx.Measurement)
1.  [function <span class="apidocSignatureSpan">influx.</span>Raw (value)](#apidoc.element.influx.Raw)
1.  [function <span class="apidocSignatureSpan">influx.</span>ResultError (message)](#apidoc.element.influx.ResultError)
1.  [function <span class="apidocSignatureSpan">influx.</span>parseMeasurement (q)](#apidoc.element.influx.parseMeasurement)
1.  [function <span class="apidocSignatureSpan">influx.</span>parseWhere (q)](#apidoc.element.influx.parseWhere)
1.  [function <span class="apidocSignatureSpan">influx.</span>toNanoDate (timestamp)](#apidoc.element.influx.toNanoDate)
1.  object <span class="apidocSignatureSpan">influx.</span>Expression.prototype
1.  object <span class="apidocSignatureSpan">influx.</span>FieldType
1.  object <span class="apidocSignatureSpan">influx.</span>InfluxDB.prototype
1.  object <span class="apidocSignatureSpan">influx.</span>Measurement.prototype
1.  object <span class="apidocSignatureSpan">influx.</span>Precision
1.  object <span class="apidocSignatureSpan">influx.</span>Raw.prototype
1.  object <span class="apidocSignatureSpan">influx.</span>ResultError.prototype
1.  object <span class="apidocSignatureSpan">influx.</span>escape

#### [module influx.Expression](#apidoc.module.influx.Expression)
1.  [function <span class="apidocSignatureSpan">influx.</span>Expression ()](#apidoc.element.influx.Expression.Expression)

#### [module influx.Expression.prototype](#apidoc.module.influx.Expression.prototype)
1.  [function <span class="apidocSignatureSpan">influx.Expression.prototype.</span>exp (fn)](#apidoc.element.influx.Expression.prototype.exp)
1.  [function <span class="apidocSignatureSpan">influx.Expression.prototype.</span>field (name)](#apidoc.element.influx.Expression.prototype.field)
1.  [function <span class="apidocSignatureSpan">influx.Expression.prototype.</span>tag (name)](#apidoc.element.influx.Expression.prototype.tag)
1.  [function <span class="apidocSignatureSpan">influx.Expression.prototype.</span>toString ()](#apidoc.element.influx.Expression.prototype.toString)
1.  [function <span class="apidocSignatureSpan">influx.Expression.prototype.</span>value (value)](#apidoc.element.influx.Expression.prototype.value)

#### [module influx.InfluxDB](#apidoc.module.influx.InfluxDB)
1.  [function <span class="apidocSignatureSpan">influx.</span>InfluxDB (options)](#apidoc.element.influx.InfluxDB.InfluxDB)

#### [module influx.InfluxDB.prototype](#apidoc.module.influx.InfluxDB.prototype)
1.  [function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>alterRetentionPolicy (name, options)](#apidoc.element.influx.InfluxDB.prototype.alterRetentionPolicy)
1.  [function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>createContinuousQuery (name, query, database)](#apidoc.element.influx.InfluxDB.prototype.createContinuousQuery)
1.  [function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>createDatabase (databaseName)](#apidoc.element.influx.InfluxDB.prototype.createDatabase)
1.  [function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>createRetentionPolicy (name, options)](#apidoc.element.influx.InfluxDB.prototype.createRetentionPolicy)
1.  [function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>createUser (username, password, admin)](#apidoc.element.influx.InfluxDB.prototype.createUser)
1.  [function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>defaultDB ()](#apidoc.element.influx.InfluxDB.prototype.defaultDB)
1.  [function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>dropContinuousQuery (name, database)](#apidoc.element.influx.InfluxDB.prototype.dropContinuousQuery)
1.  [function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>dropDatabase (databaseName)](#apidoc.element.influx.InfluxDB.prototype.dropDatabase)
1.  [function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>dropMeasurement (measurement, database)](#apidoc.element.influx.InfluxDB.prototype.dropMeasurement)
1.  [function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>dropRetentionPolicy (name, database)](#apidoc.element.influx.InfluxDB.prototype.dropRetentionPolicy)
1.  [function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>dropSeries (options)](#apidoc.element.influx.InfluxDB.prototype.dropSeries)
1.  [function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>dropUser (username)](#apidoc.element.influx.InfluxDB.prototype.dropUser)
1.  [function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>getDatabaseNames ()](#apidoc.element.influx.InfluxDB.prototype.getDatabaseNames)
1.  [function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>getMeasurements (database)](#apidoc.element.influx.InfluxDB.prototype.getMeasurements)
1.  [function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>getQueryOpts (params, method)](#apidoc.element.influx.InfluxDB.prototype.getQueryOpts)
1.  [function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>getSeries (options)](#apidoc.element.influx.InfluxDB.prototype.getSeries)
1.  [function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>getUsers ()](#apidoc.element.influx.InfluxDB.prototype.getUsers)
1.  [function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>grantAdminPrivilege (username)](#apidoc.element.influx.InfluxDB.prototype.grantAdminPrivilege)
1.  [function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>grantPrivilege (username, privilege, database)](#apidoc.element.influx.InfluxDB.prototype.grantPrivilege)
1.  [function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>ping (timeout)](#apidoc.element.influx.InfluxDB.prototype.ping)
1.  [function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>query (query, options)](#apidoc.element.influx.InfluxDB.prototype.query)
1.  [function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>queryRaw (query, options)](#apidoc.element.influx.InfluxDB.prototype.queryRaw)
1.  [function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>revokeAdminPrivilege (username)](#apidoc.element.influx.InfluxDB.prototype.revokeAdminPrivilege)
1.  [function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>revokePrivilege (username, privilege, database)](#apidoc.element.influx.InfluxDB.prototype.revokePrivilege)
1.  [function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>setPassword (username, password)](#apidoc.element.influx.InfluxDB.prototype.setPassword)
1.  [function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>showContinousQueries (database)](#apidoc.element.influx.InfluxDB.prototype.showContinousQueries)
1.  [function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>showRetentionPolicies (database)](#apidoc.element.influx.InfluxDB.prototype.showRetentionPolicies)
1.  [function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>writeMeasurement (measurement, points, options)](#apidoc.element.influx.InfluxDB.prototype.writeMeasurement)
1.  [function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>writePoints (points, options)](#apidoc.element.influx.InfluxDB.prototype.writePoints)

#### [module influx.Measurement](#apidoc.module.influx.Measurement)
1.  [function <span class="apidocSignatureSpan">influx.</span>Measurement ()](#apidoc.element.influx.Measurement.Measurement)

#### [module influx.Measurement.prototype](#apidoc.module.influx.Measurement.prototype)
1.  [function <span class="apidocSignatureSpan">influx.Measurement.prototype.</span>db (db)](#apidoc.element.influx.Measurement.prototype.db)
1.  [function <span class="apidocSignatureSpan">influx.Measurement.prototype.</span>name (name)](#apidoc.element.influx.Measurement.prototype.name)
1.  [function <span class="apidocSignatureSpan">influx.Measurement.prototype.</span>policy (retentionPolicy)](#apidoc.element.influx.Measurement.prototype.policy)
1.  [function <span class="apidocSignatureSpan">influx.Measurement.prototype.</span>toString ()](#apidoc.element.influx.Measurement.prototype.toString)

#### [module influx.Raw](#apidoc.module.influx.Raw)
1.  [function <span class="apidocSignatureSpan">influx.</span>Raw (value)](#apidoc.element.influx.Raw.Raw)

#### [module influx.Raw.prototype](#apidoc.module.influx.Raw.prototype)
1.  [function <span class="apidocSignatureSpan">influx.Raw.prototype.</span>getValue ()](#apidoc.element.influx.Raw.prototype.getValue)

#### [module influx.ResultError](#apidoc.module.influx.ResultError)
1.  [function <span class="apidocSignatureSpan">influx.</span>ResultError (message)](#apidoc.element.influx.ResultError.ResultError)

#### [module influx.ResultError.prototype](#apidoc.module.influx.ResultError.prototype)
1.  [function <span class="apidocSignatureSpan">influx.ResultError.prototype.</span>constructor (message)](#apidoc.element.influx.ResultError.prototype.constructor)

#### [module influx.escape](#apidoc.module.influx.escape)
1.  [function <span class="apidocSignatureSpan">influx.escape.</span>measurement ()](#apidoc.element.influx.escape.measurement)
1.  [function <span class="apidocSignatureSpan">influx.escape.</span>quoted ()](#apidoc.element.influx.escape.quoted)
1.  [function <span class="apidocSignatureSpan">influx.escape.</span>stringLit ()](#apidoc.element.influx.escape.stringLit)
1.  [function <span class="apidocSignatureSpan">influx.escape.</span>tag ()](#apidoc.element.influx.escape.tag)



# <a name="apidoc.module.influx"></a>[module influx](#apidoc.module.influx)

#### <a name="apidoc.element.influx.Expression"></a>[function <span class="apidocSignatureSpan">influx.</span>Expression ()](#apidoc.element.influx.Expression)
- description and source-code
```javascript
function Expression() {
    this.query = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.InfluxDB"></a>[function <span class="apidocSignatureSpan">influx.</span>InfluxDB (options)](#apidoc.element.influx.InfluxDB)
- description and source-code
```javascript
function InfluxDB(options) {
    var _this = this;
<span class="apidocCodeCommentSpan">    /**
     * Map of Schema instances defining measurements in Influx.
     * @private
     */
</span>    this.schema = Object.create(null);
    // Figure out how to parse whatever we were passed in into a IClusterConfig.
    if (typeof options === 'string') {
        options = parseOptionsUrl(options);
    }
    else if (!options) {
        options = defaultHost;
    }
    if (!options.hasOwnProperty('hosts')) {
        options = {
            database: options.database,
            hosts: [options],
            password: options.password,
            pool: options.pool,
            schema: options.schema,
            username: options.username,
        };
    }
    var resolved = options;
    resolved.hosts = resolved.hosts.map(function (host) {
        return defaults({
            host: host.host,
            port: host.port,
            protocol: host.protocol,
            options: host.options,
        }, defaultHost);
    });
    this.pool = new pool_1.Pool(resolved.pool);
    this.options = defaults(resolved, defaultOptions);
    resolved.hosts.forEach(function (host) {
        _this.pool.addHost(host.protocol + "://" + host.host + ":" + host.port, host.options);
    });
    this.options.schema.forEach(function (schema) {
        var db = schema.database = schema.database || _this.options.database;
        if (!db) {
            throw new Error("Schema " + schema.measurement + " doesn't have a database specified," +
                'and no default database is provided!');
        }
        if (!_this.schema[db]) {
            _this.schema[db] = Object.create(null);
        }
        _this.schema[db][schema.measurement] = new schema_1.Schema(schema);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.Measurement"></a>[function <span class="apidocSignatureSpan">influx.</span>Measurement ()](#apidoc.element.influx.Measurement)
- description and source-code
```javascript
function Measurement() {
    this.parts = [null, null, null];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.Raw"></a>[function <span class="apidocSignatureSpan">influx.</span>Raw (value)](#apidoc.element.influx.Raw)
- description and source-code
```javascript
function Raw(value) {
    this.value = value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.ResultError"></a>[function <span class="apidocSignatureSpan">influx.</span>ResultError (message)](#apidoc.element.influx.ResultError)
- description and source-code
```javascript
function ResultError(message) {
    var _this = _super.call(this) || this;
    _this.message = "Error from InfluxDB: " + message;
    return _this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.parseMeasurement"></a>[function <span class="apidocSignatureSpan">influx.</span>parseMeasurement (q)](#apidoc.element.influx.parseMeasurement)
- description and source-code
```javascript
function parseMeasurement(q) {
    if (typeof q.measurement === 'function') {
        return q.measurement(new Measurement()).toString();
    }
    return q.measurement;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.parseWhere"></a>[function <span class="apidocSignatureSpan">influx.</span>parseWhere (q)](#apidoc.element.influx.parseWhere)
- description and source-code
```javascript
function parseWhere(q) {
    if (typeof q.where === 'function') {
        return q.where(new Expression()).toString();
    }
    return q.where;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.toNanoDate"></a>[function <span class="apidocSignatureSpan">influx.</span>toNanoDate (timestamp)](#apidoc.element.influx.toNanoDate)
- description and source-code
```javascript
function toNanoDate(timestamp) {
    var date = new Date(Math.floor(Number(timestamp) / nsPer.ms));
    date._nanoTime = timestamp;
    date.getNanoTime = nanoDateMethods.getNanoTimeFromStamp;
    date.toNanoISOString = nanoDateMethods.toNanoISOStringFromStamp;
    return date;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.influx.Expression"></a>[module influx.Expression](#apidoc.module.influx.Expression)

#### <a name="apidoc.element.influx.Expression.Expression"></a>[function <span class="apidocSignatureSpan">influx.</span>Expression ()](#apidoc.element.influx.Expression.Expression)
- description and source-code
```javascript
function Expression() {
    this.query = [];
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.influx.Expression.prototype"></a>[module influx.Expression.prototype](#apidoc.module.influx.Expression.prototype)

#### <a name="apidoc.element.influx.Expression.prototype.exp"></a>[function <span class="apidocSignatureSpan">influx.Expression.prototype.</span>exp (fn)](#apidoc.element.influx.Expression.prototype.exp)
- description and source-code
```javascript
exp = function (fn) {
    this.query.push('(' + fn(new Expression()).toString() + ')');
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.Expression.prototype.field"></a>[function <span class="apidocSignatureSpan">influx.Expression.prototype.</span>field (name)](#apidoc.element.influx.Expression.prototype.field)
- description and source-code
```javascript
field = function (name) {
    this.query.push(grammar_1.escape.quoted(name));
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.Expression.prototype.tag"></a>[function <span class="apidocSignatureSpan">influx.Expression.prototype.</span>tag (name)](#apidoc.element.influx.Expression.prototype.tag)
- description and source-code
```javascript
tag = function (name) {
    this.field(name);
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.Expression.prototype.toString"></a>[function <span class="apidocSignatureSpan">influx.Expression.prototype.</span>toString ()](#apidoc.element.influx.Expression.prototype.toString)
- description and source-code
```javascript
toString = function () {
    return this.query.join(' ');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.Expression.prototype.value"></a>[function <span class="apidocSignatureSpan">influx.Expression.prototype.</span>value (value)](#apidoc.element.influx.Expression.prototype.value)
- description and source-code
```javascript
value = function (value) {
    switch (typeof value) {
        case 'number':
            this.query.push(value);
            return this;
        case 'string':
            this.query.push(grammar_1.escape.stringLit(value));
            return this;
        case 'boolean':
            this.query.push(value ? 'TRUE' : 'FALSE');
            return this;
        default:
            if (value instanceof Date) {
                this.query.push(grammar_1.formatDate(value));
                return this;
            }
            if (value instanceof RegExp) {
                if (regexHasFlags(value)) {
                    throw new Error('Attempted to query using a regex with flags, ' +
                        'but Influx doesn\'t support flags in queries.');
                }
                this.query.push('/' + value.source + '/');
                return this;
            }
            if (value && typeof value.toString === 'function') {
                this.query.push(value.toString());
                return this;
            }
            throw new Error("node-influx doesn't know how to encode the provided value into a " +
                'query. If you think this is a bug, open an issue here: https://git.io/influx-err');
    }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.influx.InfluxDB"></a>[module influx.InfluxDB](#apidoc.module.influx.InfluxDB)

#### <a name="apidoc.element.influx.InfluxDB.InfluxDB"></a>[function <span class="apidocSignatureSpan">influx.</span>InfluxDB (options)](#apidoc.element.influx.InfluxDB.InfluxDB)
- description and source-code
```javascript
function InfluxDB(options) {
    var _this = this;
<span class="apidocCodeCommentSpan">    /**
     * Map of Schema instances defining measurements in Influx.
     * @private
     */
</span>    this.schema = Object.create(null);
    // Figure out how to parse whatever we were passed in into a IClusterConfig.
    if (typeof options === 'string') {
        options = parseOptionsUrl(options);
    }
    else if (!options) {
        options = defaultHost;
    }
    if (!options.hasOwnProperty('hosts')) {
        options = {
            database: options.database,
            hosts: [options],
            password: options.password,
            pool: options.pool,
            schema: options.schema,
            username: options.username,
        };
    }
    var resolved = options;
    resolved.hosts = resolved.hosts.map(function (host) {
        return defaults({
            host: host.host,
            port: host.port,
            protocol: host.protocol,
            options: host.options,
        }, defaultHost);
    });
    this.pool = new pool_1.Pool(resolved.pool);
    this.options = defaults(resolved, defaultOptions);
    resolved.hosts.forEach(function (host) {
        _this.pool.addHost(host.protocol + "://" + host.host + ":" + host.port, host.options);
    });
    this.options.schema.forEach(function (schema) {
        var db = schema.database = schema.database || _this.options.database;
        if (!db) {
            throw new Error("Schema " + schema.measurement + " doesn't have a database specified," +
                'and no default database is provided!');
        }
        if (!_this.schema[db]) {
            _this.schema[db] = Object.create(null);
        }
        _this.schema[db][schema.measurement] = new schema_1.Schema(schema);
    });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.influx.InfluxDB.prototype"></a>[module influx.InfluxDB.prototype](#apidoc.module.influx.InfluxDB.prototype)

#### <a name="apidoc.element.influx.InfluxDB.prototype.alterRetentionPolicy"></a>[function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>alterRetentionPolicy (name, options)](#apidoc.element.influx.InfluxDB.prototype.alterRetentionPolicy)
- description and source-code
```javascript
alterRetentionPolicy = function (name, options) {
    var q = "alter retention policy " + grammar.escape.quoted(name) + " on "
        + grammar.escape.quoted(options.database || this.defaultDB())
        + (" duration " + options.duration + " replication " + options.replication)
        + (options.isDefault ? ' default' : '');
    return this.pool.json(this.getQueryOpts({ q: q }, 'POST')).then(results_1.assertNoErrors);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.InfluxDB.prototype.createContinuousQuery"></a>[function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>createContinuousQuery (name, query, database)](#apidoc.element.influx.InfluxDB.prototype.createContinuousQuery)
- description and source-code
```javascript
createContinuousQuery = function (name, query, database) {
    if (database === void 0) { database = this.defaultDB(); }
    return this.pool.json(this.getQueryOpts({
        q: "create continuous query " + grammar.escape.quoted(name)
            + (" on " + grammar.escape.quoted(database) + " begin " + query + " end"),
    }, 'POST')).then(results_1.assertNoErrors);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.InfluxDB.prototype.createDatabase"></a>[function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>createDatabase (databaseName)](#apidoc.element.influx.InfluxDB.prototype.createDatabase)
- description and source-code
```javascript
createDatabase = function (databaseName) {
    return this.pool.json(this.getQueryOpts({
        q: "create database " + grammar.escape.quoted(databaseName),
    }, 'POST')).then(results_1.assertNoErrors);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.InfluxDB.prototype.createRetentionPolicy"></a>[function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>createRetentionPolicy (name, options)](#apidoc.element.influx.InfluxDB.prototype.createRetentionPolicy)
- description and source-code
```javascript
createRetentionPolicy = function (name, options) {
    var q = "create retention policy " + grammar.escape.quoted(name) + " on "
        + grammar.escape.quoted(options.database || this.defaultDB())
        + (" duration " + options.duration + " replication " + options.replication)
        + (options.isDefault ? ' default' : '');
    return this.pool.json(this.getQueryOpts({ q: q }, 'POST')).then(results_1.assertNoErrors);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.InfluxDB.prototype.createUser"></a>[function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>createUser (username, password, admin)](#apidoc.element.influx.InfluxDB.prototype.createUser)
- description and source-code
```javascript
createUser = function (username, password, admin) {
    if (admin === void 0) { admin = false; }
    return this.pool.json(this.getQueryOpts({
        q: "create user " + grammar.escape.quoted(username) + " with password "
            + grammar.escape.stringLit(password)
            + (admin ? ' with all privileges' : ''),
    }, 'POST')).then(results_1.assertNoErrors);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.InfluxDB.prototype.defaultDB"></a>[function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>defaultDB ()](#apidoc.element.influx.InfluxDB.prototype.defaultDB)
- description and source-code
```javascript
defaultDB = function () {
    if (!this.options.database) {
        throw new Error('Attempted to run an influx query without a default'
            + ' database specified or an explicit database provided.');
    }
    return this.options.database;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.InfluxDB.prototype.dropContinuousQuery"></a>[function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>dropContinuousQuery (name, database)](#apidoc.element.influx.InfluxDB.prototype.dropContinuousQuery)
- description and source-code
```javascript
dropContinuousQuery = function (name, database) {
    if (database === void 0) { database = this.defaultDB(); }
    return this.pool.json(this.getQueryOpts({
        q: "drop continuous query " + grammar.escape.quoted(name)
            + (" on " + grammar.escape.quoted(database)),
    }, 'POST')).then(results_1.assertNoErrors);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.InfluxDB.prototype.dropDatabase"></a>[function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>dropDatabase (databaseName)](#apidoc.element.influx.InfluxDB.prototype.dropDatabase)
- description and source-code
```javascript
dropDatabase = function (databaseName) {
    return this.pool.json(this.getQueryOpts({
        q: "drop database " + grammar.escape.quoted(databaseName),
    }, 'POST')).then(results_1.assertNoErrors);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.InfluxDB.prototype.dropMeasurement"></a>[function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>dropMeasurement (measurement, database)](#apidoc.element.influx.InfluxDB.prototype.dropMeasurement)
- description and source-code
```javascript
dropMeasurement = function (measurement, database) {
    if (database === void 0) { database = this.defaultDB(); }
    return this.pool.json(this.getQueryOpts({
        db: database,
        q: "drop measurement " + grammar.escape.quoted(measurement),
    }, 'POST')).then(results_1.assertNoErrors);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.InfluxDB.prototype.dropRetentionPolicy"></a>[function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>dropRetentionPolicy (name, database)](#apidoc.element.influx.InfluxDB.prototype.dropRetentionPolicy)
- description and source-code
```javascript
dropRetentionPolicy = function (name, database) {
    if (database === void 0) { database = this.defaultDB(); }
    return this.pool.json(this.getQueryOpts({
        q: "drop retention policy " + grammar.escape.quoted(name) + " "
            + ("on " + grammar.escape.quoted(database)),
    }, 'POST')).then(results_1.assertNoErrors);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.InfluxDB.prototype.dropSeries"></a>[function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>dropSeries (options)](#apidoc.element.influx.InfluxDB.prototype.dropSeries)
- description and source-code
```javascript
dropSeries = function (options) {
    var db = 'database' in options ? options.database : this.defaultDB();
    var q = 'drop series';
    if ('measurement' in options) {
        q += ' from ' + b.parseMeasurement(options);
    }
    if ('where' in options) {
        q += ' where ' + b.parseWhere(options);
    }
    return this.pool.json(this.getQueryOpts({ db: db, q: q }, 'POST')).then(results_1.assertNoErrors);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.InfluxDB.prototype.dropUser"></a>[function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>dropUser (username)](#apidoc.element.influx.InfluxDB.prototype.dropUser)
- description and source-code
```javascript
dropUser = function (username) {
    return this.pool.json(this.getQueryOpts({
        q: "drop user " + grammar.escape.quoted(username),
    }, 'POST')).then(results_1.assertNoErrors);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.InfluxDB.prototype.getDatabaseNames"></a>[function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>getDatabaseNames ()](#apidoc.element.influx.InfluxDB.prototype.getDatabaseNames)
- description and source-code
```javascript
getDatabaseNames = function () {
    return this.pool.json(this.getQueryOpts({ q: 'show databases' }))
        .then(function (res) { return results_1.parseSingle(res).map(function (r) { return r.name; }); });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.InfluxDB.prototype.getMeasurements"></a>[function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>getMeasurements (database)](#apidoc.element.influx.InfluxDB.prototype.getMeasurements)
- description and source-code
```javascript
getMeasurements = function (database) {
    if (database === void 0) { database = this.defaultDB(); }
    return this.pool.json(this.getQueryOpts({
        db: database,
        q: 'show measurements',
    })).then(function (res) { return results_1.parseSingle(res).map(function (r) { return r.name; }); });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.InfluxDB.prototype.getQueryOpts"></a>[function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>getQueryOpts (params, method)](#apidoc.element.influx.InfluxDB.prototype.getQueryOpts)
- description and source-code
```javascript
getQueryOpts = function (params, method) {
    if (method === void 0) { method = 'GET'; }
    return {
        method: method,
        path: '/query',
        query: Object.assign({
            p: this.options.password,
            u: this.options.username,
        }, params),
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.InfluxDB.prototype.getSeries"></a>[function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>getSeries (options)](#apidoc.element.influx.InfluxDB.prototype.getSeries)
- description and source-code
```javascript
getSeries = function (options) {
    if (options === void 0) { options = {}; }
    var _a = options.database, database = _a === void 0 ? this.defaultDB() : _a, measurement = options.measurement;
    var query = 'show series';
    if (measurement) {
        query += " from " + grammar.escape.quoted(measurement);
    }
    return this.pool.json(this.getQueryOpts({
        db: database,
        q: query,
    })).then(function (res) { return results_1.parseSingle(res).map(function (r) { return r.key; }); });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.InfluxDB.prototype.getUsers"></a>[function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>getUsers ()](#apidoc.element.influx.InfluxDB.prototype.getUsers)
- description and source-code
```javascript
getUsers = function () {
    return this.pool.json(this.getQueryOpts({ q: 'show users' })).then(results_1.parseSingle);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.InfluxDB.prototype.grantAdminPrivilege"></a>[function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>grantAdminPrivilege (username)](#apidoc.element.influx.InfluxDB.prototype.grantAdminPrivilege)
- description and source-code
```javascript
grantAdminPrivilege = function (username) {
    return this.pool.json(this.getQueryOpts({
        q: "grant all to " + grammar.escape.quoted(username),
    }, 'POST')).then(results_1.assertNoErrors);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.InfluxDB.prototype.grantPrivilege"></a>[function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>grantPrivilege (username, privilege, database)](#apidoc.element.influx.InfluxDB.prototype.grantPrivilege)
- description and source-code
```javascript
grantPrivilege = function (username, privilege, database) {
    if (database === void 0) { database = this.defaultDB(); }
    return this.pool.json(this.getQueryOpts({
        q: "grant " + privilege + " on " + grammar.escape.quoted(database) + " "
            + ("to " + grammar.escape.quoted(username)),
    }, 'POST')).then(results_1.assertNoErrors);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.InfluxDB.prototype.ping"></a>[function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>ping (timeout)](#apidoc.element.influx.InfluxDB.prototype.ping)
- description and source-code
```javascript
ping = function (timeout) {
    return this.pool.ping(timeout);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.InfluxDB.prototype.query"></a>[function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>query (query, options)](#apidoc.element.influx.InfluxDB.prototype.query)
- description and source-code
```javascript
query = function (query, options) {
    if (options === void 0) { options = {}; }
    if (Array.isArray(query)) {
        query = query.join(';');
    }
    // If the consumer asked explicitly for nanosecond precision parsing,
    // remove that to cause Influx to give us ISO dates that
    // we can parse correctly.
    if (options.precision === 'n') {
        options = Object.assign({}, options); // avoid mutating
        delete options.precision;
    }
    return this.queryRaw(query, options).then(function (res) { return results_1.parse(res, options.precision); });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.InfluxDB.prototype.queryRaw"></a>[function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>queryRaw (query, options)](#apidoc.element.influx.InfluxDB.prototype.queryRaw)
- description and source-code
```javascript
queryRaw = function (query, options) {
    if (options === void 0) { options = {}; }
    var _a = options.database, database = _a === void 0 ? this.defaultDB() : _a, retentionPolicy = options.retentionPolicy;
    if (query instanceof Array) {
        query = query.join(';');
    }
    return this.pool.json(this.getQueryOpts({
        db: database,
        epoch: options.precision,
        q: query,
        rp: retentionPolicy,
    }));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.InfluxDB.prototype.revokeAdminPrivilege"></a>[function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>revokeAdminPrivilege (username)](#apidoc.element.influx.InfluxDB.prototype.revokeAdminPrivilege)
- description and source-code
```javascript
revokeAdminPrivilege = function (username) {
    return this.pool.json(this.getQueryOpts({
        q: "revoke all from " + grammar.escape.quoted(username),
    }, 'POST')).then(results_1.assertNoErrors);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.InfluxDB.prototype.revokePrivilege"></a>[function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>revokePrivilege (username, privilege, database)](#apidoc.element.influx.InfluxDB.prototype.revokePrivilege)
- description and source-code
```javascript
revokePrivilege = function (username, privilege, database) {
    if (database === void 0) { database = this.defaultDB(); }
    return this.pool.json(this.getQueryOpts({
        q: "revoke " + privilege + " from " + grammar.escape.quoted(username) + " on "
            + grammar.escape.quoted(database),
    }, 'POST')).then(results_1.assertNoErrors);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.InfluxDB.prototype.setPassword"></a>[function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>setPassword (username, password)](#apidoc.element.influx.InfluxDB.prototype.setPassword)
- description and source-code
```javascript
setPassword = function (username, password) {
    return this.pool.json(this.getQueryOpts({
        q: "set password for " + grammar.escape.quoted(username) + " = "
            + grammar.escape.stringLit(password),
    }, 'POST')).then(results_1.assertNoErrors);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.InfluxDB.prototype.showContinousQueries"></a>[function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>showContinousQueries (database)](#apidoc.element.influx.InfluxDB.prototype.showContinousQueries)
- description and source-code
```javascript
showContinousQueries = function (database) {
    if (database === void 0) { database = this.defaultDB(); }
    return this.pool.json(this.getQueryOpts({
        db: database,
        q: 'show continuous queries',
    })).then(results_1.parseSingle);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.InfluxDB.prototype.showRetentionPolicies"></a>[function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>showRetentionPolicies (database)](#apidoc.element.influx.InfluxDB.prototype.showRetentionPolicies)
- description and source-code
```javascript
showRetentionPolicies = function (database) {
    if (database === void 0) { database = this.defaultDB(); }
    return this.pool.json(this.getQueryOpts({
        q: "show retention policies on " + grammar.escape.quoted(database),
    }, 'GET')).then(results_1.parseSingle);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.InfluxDB.prototype.writeMeasurement"></a>[function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>writeMeasurement (measurement, points, options)](#apidoc.element.influx.InfluxDB.prototype.writeMeasurement)
- description and source-code
```javascript
writeMeasurement = function (measurement, points, options) {
    if (options === void 0) { options = {}; }
    points = points.map(function (p) { return Object.assign({ measurement: measurement }, p); });
    return this.writePoints(points, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.InfluxDB.prototype.writePoints"></a>[function <span class="apidocSignatureSpan">influx.InfluxDB.prototype.</span>writePoints (points, options)](#apidoc.element.influx.InfluxDB.prototype.writePoints)
- description and source-code
```javascript
writePoints = function (points, options) {
    var _this = this;
    if (options === void 0) { options = {}; }
    var _a = options.database, database = _a === void 0 ? this.defaultDB() : _a, _b = options.precision, precision = _b === void
 0 ? 'n' : _b, retentionPolicy = options.retentionPolicy;
    var payload = '';
    points.forEach(function (point) {
        var _a = point.fields, fields = _a === void 0 ? {} : _a, _b = point.tags, tags = _b === void 0 ? {} : _b, measurement =
point.measurement, timestamp = point.timestamp;
        var schema = _this.schema[database] && _this.schema[database][measurement];
        var fieldsPairs = schema ? schema.coerceFields(fields) : schema_1.coerceBadly(fields);
        var tagsNames = schema ? schema.checkTags(tags) : Object.keys(tags);
        payload += (payload.length > 0 ? '\n' : '') + measurement;
        for (var i = 0; i < tagsNames.length; i += 1) {
            payload += ','
                + grammar.escape.tag(tagsNames[i])
                + '='
                + grammar.escape.tag(tags[tagsNames[i]]);
        }
        for (var i = 0; i < fieldsPairs.length; i += 1) {
            payload += (i === 0 ? ' ' : ',')
                + grammar.escape.tag(fieldsPairs[i][0])
                + '='
                + fieldsPairs[i][1];
        }
        if (timestamp !== undefined) {
            payload += ' ' + grammar.castTimestamp(timestamp, precision);
        }
    });
    return this.pool.discard({
        body: payload,
        method: 'POST',
        path: '/write',
        query: Object.assign({
            db: database,
            p: this.options.password,
            precision: precision,
            rp: retentionPolicy,
            u: this.options.username,
        }),
    });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.influx.Measurement"></a>[module influx.Measurement](#apidoc.module.influx.Measurement)

#### <a name="apidoc.element.influx.Measurement.Measurement"></a>[function <span class="apidocSignatureSpan">influx.</span>Measurement ()](#apidoc.element.influx.Measurement.Measurement)
- description and source-code
```javascript
function Measurement() {
    this.parts = [null, null, null];
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.influx.Measurement.prototype"></a>[module influx.Measurement.prototype](#apidoc.module.influx.Measurement.prototype)

#### <a name="apidoc.element.influx.Measurement.prototype.db"></a>[function <span class="apidocSignatureSpan">influx.Measurement.prototype.</span>db (db)](#apidoc.element.influx.Measurement.prototype.db)
- description and source-code
```javascript
db = function (db) {
    this.parts[0] = db;
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.Measurement.prototype.name"></a>[function <span class="apidocSignatureSpan">influx.Measurement.prototype.</span>name (name)](#apidoc.element.influx.Measurement.prototype.name)
- description and source-code
```javascript
name = function (name) {
    this.parts[2] = name;
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.Measurement.prototype.policy"></a>[function <span class="apidocSignatureSpan">influx.Measurement.prototype.</span>policy (retentionPolicy)](#apidoc.element.influx.Measurement.prototype.policy)
- description and source-code
```javascript
policy = function (retentionPolicy) {
    this.parts[1] = retentionPolicy;
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.Measurement.prototype.toString"></a>[function <span class="apidocSignatureSpan">influx.Measurement.prototype.</span>toString ()](#apidoc.element.influx.Measurement.prototype.toString)
- description and source-code
```javascript
toString = function () {
    if (!this.parts[2]) {
        throw new Error("You must specify a measurement name to query! Got '" + this.parts[2] + "'");
    }
    return this.parts.filter(function (p) { return !!p; })
        .map(function (p) { return grammar_1.escape.quoted(p); })
        .join('.');
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.influx.Raw"></a>[module influx.Raw](#apidoc.module.influx.Raw)

#### <a name="apidoc.element.influx.Raw.Raw"></a>[function <span class="apidocSignatureSpan">influx.</span>Raw (value)](#apidoc.element.influx.Raw.Raw)
- description and source-code
```javascript
function Raw(value) {
    this.value = value;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.influx.Raw.prototype"></a>[module influx.Raw.prototype](#apidoc.module.influx.Raw.prototype)

#### <a name="apidoc.element.influx.Raw.prototype.getValue"></a>[function <span class="apidocSignatureSpan">influx.Raw.prototype.</span>getValue ()](#apidoc.element.influx.Raw.prototype.getValue)
- description and source-code
```javascript
getValue = function () {
    return this.value;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.influx.ResultError"></a>[module influx.ResultError](#apidoc.module.influx.ResultError)

#### <a name="apidoc.element.influx.ResultError.ResultError"></a>[function <span class="apidocSignatureSpan">influx.</span>ResultError (message)](#apidoc.element.influx.ResultError.ResultError)
- description and source-code
```javascript
function ResultError(message) {
    var _this = _super.call(this) || this;
    _this.message = "Error from InfluxDB: " + message;
    return _this;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.influx.ResultError.prototype"></a>[module influx.ResultError.prototype](#apidoc.module.influx.ResultError.prototype)

#### <a name="apidoc.element.influx.ResultError.prototype.constructor"></a>[function <span class="apidocSignatureSpan">influx.ResultError.prototype.</span>constructor (message)](#apidoc.element.influx.ResultError.prototype.constructor)
- description and source-code
```javascript
function ResultError(message) {
    var _this = _super.call(this) || this;
    _this.message = "Error from InfluxDB: " + message;
    return _this;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.influx.escape"></a>[module influx.escape](#apidoc.module.influx.escape)

#### <a name="apidoc.element.influx.escape.measurement"></a>[function <span class="apidocSignatureSpan">influx.escape.</span>measurement ()](#apidoc.element.influx.escape.measurement)
- description and source-code
```javascript
measurement = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.escape.quoted"></a>[function <span class="apidocSignatureSpan">influx.escape.</span>quoted ()](#apidoc.element.influx.escape.quoted)
- description and source-code
```javascript
quoted = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.escape.stringLit"></a>[function <span class="apidocSignatureSpan">influx.escape.</span>stringLit ()](#apidoc.element.influx.escape.stringLit)
- description and source-code
```javascript
stringLit = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.influx.escape.tag"></a>[function <span class="apidocSignatureSpan">influx.escape.</span>tag ()](#apidoc.element.influx.escape.tag)
- description and source-code
```javascript
tag = function () { [native code] }
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
