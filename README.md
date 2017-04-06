# api documentation for  [db-migrate (v0.9.26)](https://github.com/kunklejr/node-db-migrate#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-db-migrate.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-db-migrate) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-db-migrate.svg)](https://travis-ci.org/npmdoc/node-npmdoc-db-migrate)
#### Database migration framework for node.js

[![NPM](https://nodei.co/npm/db-migrate.png?downloads=true)](https://www.npmjs.com/package/db-migrate)

[![apidoc](https://npmdoc.github.io/node-npmdoc-db-migrate/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-db-migrate_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-db-migrate/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-db-migrate/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-db-migrate/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Jeff Kunkle"
    },
    "bin": {
        "db-migrate": "./bin/db-migrate"
    },
    "bugs": {
        "url": "https://github.com/kunklejr/node-db-migrate/issues"
    },
    "dependencies": {
        "async": "~0.9.0",
        "dotenv": "~0.5.1",
        "final-fs": "^1.6.0",
        "mkdirp": "~0.5.0",
        "moment": "~2.9.0",
        "mongodb": "^1.4.30",
        "mysql": "^2.10.2",
        "optimist": "~0.6.1",
        "parse-database-url": "~0.2.2",
        "pg": "^4.5.5",
        "pkginfo": "~0.3.0",
        "semver": "~4.3.3",
        "sqlite3": "^3.1.4"
    },
    "description": "Database migration framework for node.js",
    "devDependencies": {
        "code": "^1.3.0",
        "db-meta": "~0.4.1",
        "lab": "^5.2.1",
        "rimraf": "~2.2.8",
        "vows": "0.8.0"
    },
    "directories": {},
    "dist": {
        "shasum": "f523e1e6d3a168587e2fddec74b0e41ea3f9794b",
        "tarball": "https://registry.npmjs.org/db-migrate/-/db-migrate-0.9.26.tgz"
    },
    "engines": {
        "node": ">=0.6.0"
    },
    "gitHead": "f34f43d515c804a5412e364fad6820a5851e8a88",
    "homepage": "https://github.com/kunklejr/node-db-migrate#readme",
    "keywords": [
        "database",
        "db",
        "migrate",
        "migration",
        "sqlite",
        "mysql"
    ],
    "license": "MIT",
    "maintainers": [
        {
            "name": "kunklejr",
            "email": "kunklejr@gmail.com"
        },
        {
            "name": "wzrdtales",
            "email": "magic@wizardtales.com"
        }
    ],
    "name": "db-migrate",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/kunklejr/node-db-migrate.git"
    },
    "scripts": {
        "test": "node node_modules/.bin/vows"
    },
    "version": "0.9.26"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module db-migrate](#apidoc.module.db-migrate)
1.  [function <span class="apidocSignatureSpan">db-migrate.</span>class ()](#apidoc.element.db-migrate.class)
1.  [function <span class="apidocSignatureSpan">db-migrate.</span>connect (config, callback)](#apidoc.element.db-migrate.connect)
1.  [function <span class="apidocSignatureSpan">db-migrate.</span>createMigration (migration, callback)](#apidoc.element.db-migrate.createMigration)
1.  [function <span class="apidocSignatureSpan">db-migrate.</span>driver (config, callback)](#apidoc.element.db-migrate.driver)
1.  [function <span class="apidocSignatureSpan">db-migrate.</span>migration ()](#apidoc.element.db-migrate.migration)
1.  [function <span class="apidocSignatureSpan">db-migrate.</span>migrator (driver, migrationsDir)](#apidoc.element.db-migrate.migrator)
1.  object <span class="apidocSignatureSpan">db-migrate.</span>config
1.  object <span class="apidocSignatureSpan">db-migrate.</span>dataType
1.  object <span class="apidocSignatureSpan">db-migrate.</span>inflection
1.  object <span class="apidocSignatureSpan">db-migrate.</span>migration.prototype
1.  object <span class="apidocSignatureSpan">db-migrate.</span>migrator.prototype
1.  object <span class="apidocSignatureSpan">db-migrate.</span>util

#### [module db-migrate.class](#apidoc.module.db-migrate.class)
1.  [function <span class="apidocSignatureSpan">db-migrate.</span>class ()](#apidoc.element.db-migrate.class.class)
1.  [function <span class="apidocSignatureSpan">db-migrate.class.</span>extend (prop)](#apidoc.element.db-migrate.class.extend)

#### [module db-migrate.config](#apidoc.module.db-migrate.config)
1.  [function <span class="apidocSignatureSpan">db-migrate.config.</span>load (fileName, currentEnv)](#apidoc.element.db-migrate.config.load)
1.  [function <span class="apidocSignatureSpan">db-migrate.config.</span>loadUrl (databaseUrl, currentEnv)](#apidoc.element.db-migrate.config.loadUrl)
1.  [function <span class="apidocSignatureSpan">db-migrate.config.</span>setCurrent (env)](#apidoc.element.db-migrate.config.setCurrent)

#### [module db-migrate.inflection](#apidoc.module.db-migrate.inflection)
1.  [function <span class="apidocSignatureSpan">db-migrate.inflection.</span>camelize (str, lowFirstLetter)](#apidoc.element.db-migrate.inflection.camelize)
1.  [function <span class="apidocSignatureSpan">db-migrate.inflection.</span>capitalize (str)](#apidoc.element.db-migrate.inflection.capitalize)
1.  [function <span class="apidocSignatureSpan">db-migrate.inflection.</span>classify (str)](#apidoc.element.db-migrate.inflection.classify)
1.  [function <span class="apidocSignatureSpan">db-migrate.inflection.</span>dasherize (str)](#apidoc.element.db-migrate.inflection.dasherize)
1.  [function <span class="apidocSignatureSpan">db-migrate.inflection.</span>demodulize (str)](#apidoc.element.db-migrate.inflection.demodulize)
1.  [function <span class="apidocSignatureSpan">db-migrate.inflection.</span>foreignKey (str, dropIdUbar)](#apidoc.element.db-migrate.inflection.foreignKey)
1.  [function <span class="apidocSignatureSpan">db-migrate.inflection.</span>humanize (str, lowFirstLetter)](#apidoc.element.db-migrate.inflection.humanize)
1.  [function <span class="apidocSignatureSpan">db-migrate.inflection.</span>indexOf (array, item, fromIndex, compareFunc)](#apidoc.element.db-migrate.inflection.indexOf)
1.  [function <span class="apidocSignatureSpan">db-migrate.inflection.</span>ordinalize (str)](#apidoc.element.db-migrate.inflection.ordinalize)
1.  [function <span class="apidocSignatureSpan">db-migrate.inflection.</span>pluralize (str, plural)](#apidoc.element.db-migrate.inflection.pluralize)
1.  [function <span class="apidocSignatureSpan">db-migrate.inflection.</span>singularize (str, singular)](#apidoc.element.db-migrate.inflection.singularize)
1.  [function <span class="apidocSignatureSpan">db-migrate.inflection.</span>tableize (str)](#apidoc.element.db-migrate.inflection.tableize)
1.  [function <span class="apidocSignatureSpan">db-migrate.inflection.</span>titleize (str)](#apidoc.element.db-migrate.inflection.titleize)
1.  [function <span class="apidocSignatureSpan">db-migrate.inflection.</span>underscore (str)](#apidoc.element.db-migrate.inflection.underscore)

#### [module db-migrate.migration](#apidoc.module.db-migrate.migration)
1.  [function <span class="apidocSignatureSpan">db-migrate.</span>migration ()](#apidoc.element.db-migrate.migration.migration)
1.  [function <span class="apidocSignatureSpan">db-migrate.migration.</span>loadFromDatabase (dir, driver, callback)](#apidoc.element.db-migrate.migration.loadFromDatabase)
1.  [function <span class="apidocSignatureSpan">db-migrate.migration.</span>loadFromFilesystem (dir, callback)](#apidoc.element.db-migrate.migration.loadFromFilesystem)
1.  [function <span class="apidocSignatureSpan">db-migrate.migration.</span>parseName (path)](#apidoc.element.db-migrate.migration.parseName)
1.  object <span class="apidocSignatureSpan">db-migrate.migration.</span>TemplateType

#### [module db-migrate.migration.prototype](#apidoc.module.db-migrate.migration.prototype)
1.  [function <span class="apidocSignatureSpan">db-migrate.migration.prototype.</span>_down ()](#apidoc.element.db-migrate.migration.prototype._down)
1.  [function <span class="apidocSignatureSpan">db-migrate.migration.prototype.</span>_up ()](#apidoc.element.db-migrate.migration.prototype._up)
1.  [function <span class="apidocSignatureSpan">db-migrate.migration.prototype.</span>defaultCoffeeTemplate ()](#apidoc.element.db-migrate.migration.prototype.defaultCoffeeTemplate)
1.  [function <span class="apidocSignatureSpan">db-migrate.migration.prototype.</span>defaultJsTemplate ()](#apidoc.element.db-migrate.migration.prototype.defaultJsTemplate)
1.  [function <span class="apidocSignatureSpan">db-migrate.migration.prototype.</span>defaultSqlTemplate ()](#apidoc.element.db-migrate.migration.prototype.defaultSqlTemplate)
1.  [function <span class="apidocSignatureSpan">db-migrate.migration.prototype.</span>down (db, callback)](#apidoc.element.db-migrate.migration.prototype.down)
1.  [function <span class="apidocSignatureSpan">db-migrate.migration.prototype.</span>getTemplate ()](#apidoc.element.db-migrate.migration.prototype.getTemplate)
1.  [function <span class="apidocSignatureSpan">db-migrate.migration.prototype.</span>sqlFileLoaderTemplate ()](#apidoc.element.db-migrate.migration.prototype.sqlFileLoaderTemplate)
1.  [function <span class="apidocSignatureSpan">db-migrate.migration.prototype.</span>up (db, callback)](#apidoc.element.db-migrate.migration.prototype.up)
1.  [function <span class="apidocSignatureSpan">db-migrate.migration.prototype.</span>write (callback)](#apidoc.element.db-migrate.migration.prototype.write)

#### [module db-migrate.migrator](#apidoc.module.db-migrate.migrator)
1.  [function <span class="apidocSignatureSpan">db-migrate.</span>migrator (driver, migrationsDir)](#apidoc.element.db-migrate.migrator.migrator)

#### [module db-migrate.migrator.prototype](#apidoc.module.db-migrate.migrator.prototype)
1.  [function <span class="apidocSignatureSpan">db-migrate.migrator.prototype.</span>createMigrationTable (callback)](#apidoc.element.db-migrate.migrator.prototype.createMigrationTable)
1.  [function <span class="apidocSignatureSpan">db-migrate.migrator.prototype.</span>deleteMigrationRecord (migration, callback)](#apidoc.element.db-migrate.migrator.prototype.deleteMigrationRecord)
1.  [function <span class="apidocSignatureSpan">db-migrate.migrator.prototype.</span>down (funcOrOpts, callback)](#apidoc.element.db-migrate.migrator.prototype.down)
1.  [function <span class="apidocSignatureSpan">db-migrate.migrator.prototype.</span>downToBy (count, callback)](#apidoc.element.db-migrate.migrator.prototype.downToBy)
1.  [function <span class="apidocSignatureSpan">db-migrate.migrator.prototype.</span>up (funcOrOpts, callback)](#apidoc.element.db-migrate.migrator.prototype.up)
1.  [function <span class="apidocSignatureSpan">db-migrate.migrator.prototype.</span>upToBy (partialName, count, callback)](#apidoc.element.db-migrate.migrator.prototype.upToBy)
1.  [function <span class="apidocSignatureSpan">db-migrate.migrator.prototype.</span>writeMigrationRecord (migration, callback)](#apidoc.element.db-migrate.migrator.prototype.writeMigrationRecord)

#### [module db-migrate.util](#apidoc.module.db-migrate.util)
1.  [function <span class="apidocSignatureSpan">db-migrate.util.</span>isArray (obj)](#apidoc.element.db-migrate.util.isArray)
1.  [function <span class="apidocSignatureSpan">db-migrate.util.</span>isFunction (obj)](#apidoc.element.db-migrate.util.isFunction)
1.  [function <span class="apidocSignatureSpan">db-migrate.util.</span>isString (obj)](#apidoc.element.db-migrate.util.isString)
1.  [function <span class="apidocSignatureSpan">db-migrate.util.</span>lpad (str, padChar, totalLength)](#apidoc.element.db-migrate.util.lpad)
1.  [function <span class="apidocSignatureSpan">db-migrate.util.</span>shallowCopy (obj)](#apidoc.element.db-migrate.util.shallowCopy)
1.  [function <span class="apidocSignatureSpan">db-migrate.util.</span>toArray (obj)](#apidoc.element.db-migrate.util.toArray)



# <a name="apidoc.module.db-migrate"></a>[module db-migrate](#apidoc.module.db-migrate)

#### <a name="apidoc.element.db-migrate.class"></a>[function <span class="apidocSignatureSpan">db-migrate.</span>class ()](#apidoc.element.db-migrate.class)
- description and source-code
```javascript
class = function (){}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.db-migrate.connect"></a>[function <span class="apidocSignatureSpan">db-migrate.</span>connect (config, callback)](#apidoc.element.db-migrate.connect)
- description and source-code
```javascript
connect = function (config, callback) {
  driver.connect(config, function(err, db) {
    if (err) { callback(err); return; }

    if(global.migrationMode)
    {
      var dirPath = path.resolve(config['migrations-dir'] || 'migrations');

      if(global.migrationMode !== 'all')
      {
        var switched = false,
            newConf;

        try {
          newConf = require(path.resolve(config['migrations-dir'] || 'migrations', global.migrationMode) + '/config.json');
          log.info('loaded extra config for migration subfolder: "' + global.migrationMode + '/config.json"');
          switched = true;
        } catch(e) {}

        if(switched) {

          db.switchDatabase(newConf, function()
          {
            global.locTitle = global.migrationMode;
            callback(null, new Migrator(db, config['migrations-dir']));
          });
        }
        else
        {
          global.locTitle = global.migrationMode;
          callback(null, new Migrator(db, config['migrations-dir']));
        }
      }
      else
      {
      recursive(dirPath, false, config['migrations-dir'] || 'migrations')
      .then(function(files) {
          var oldClose = db.close;

          files = files.filter(function (file) {
            return file !== 'migrations' && fs.statSync(file).isDirectory();
          });

          files.push('');

          db.close = function(cb) { migrationFiles(files, callback, config, db, oldClose, cb); };

          db.close();
        });
      }
    }
    else
      callback(null, new Migrator(db, config['migrations-dir']));

  });
}
```
- example usage
```shell
...
var log = require('./lib/log');
var Migrator = require('./lib/migrator');

exports.dataType = require('./lib/data_type');
exports.config = require('./lib/config');

exports.connect = function(config, callback) {
  driver.connect(config, function(err, db) {
    if (err) { callback(err); return; }

    if(global.migrationMode)
    {
var dirPath = path.resolve(config['migrations-dir'] || 'migrations');

if(global.migrationMode !== 'all')
...
```

#### <a name="apidoc.element.db-migrate.createMigration"></a>[function <span class="apidocSignatureSpan">db-migrate.</span>createMigration (migration, callback)](#apidoc.element.db-migrate.createMigration)
- description and source-code
```javascript
createMigration = function (migration, callback) {
  migration.write(function(err) {
  if (err) { callback(err); return; }
  callback(null, migration);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.db-migrate.driver"></a>[function <span class="apidocSignatureSpan">db-migrate.</span>driver (config, callback)](#apidoc.element.db-migrate.driver)
- description and source-code
```javascript
driver = function (config, callback) {

  driver.connect(config, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.db-migrate.migration"></a>[function <span class="apidocSignatureSpan">db-migrate.</span>migration ()](#apidoc.element.db-migrate.migration)
- description and source-code
```javascript
migration = function () {
  if (arguments.length >= 3) {
    this.title = arguments[0];
    this.date = arguments[2];
    this.name = formatName(this.title, this.date);
    this.path = formatPath(arguments[1], this.name);
    this.templateType = arguments[3];
  } else if (arguments.length == 1) {
    this.path = arguments[0];
    this.name = Migration.parseName(this.path);
    this.date = parseDate(this.name);
    this.title = parseTitle(this.name);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.db-migrate.migrator"></a>[function <span class="apidocSignatureSpan">db-migrate.</span>migrator (driver, migrationsDir)](#apidoc.element.db-migrate.migrator)
- description and source-code
```javascript
migrator = function (driver, migrationsDir) {
  this.driver = driver;
  this.migrationsDir = migrationsDir;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.db-migrate.class"></a>[module db-migrate.class](#apidoc.module.db-migrate.class)

#### <a name="apidoc.element.db-migrate.class.class"></a>[function <span class="apidocSignatureSpan">db-migrate.</span>class ()](#apidoc.element.db-migrate.class.class)
- description and source-code
```javascript
class = function (){}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.db-migrate.class.extend"></a>[function <span class="apidocSignatureSpan">db-migrate.class.</span>extend (prop)](#apidoc.element.db-migrate.class.extend)
- description and source-code
```javascript
extend = function (prop) {
  var _super = this.prototype;

  // Instantiate a base class (but only create the instance,
  // don't run the init constructor)
  initializing = true;
  var prototype = new this();
  initializing = false;

  // Copy the properties over onto the new prototype
  for (var name in prop) {
    // Check if we're overwriting an existing function
    prototype[name] = typeof prop[name] == "function" &&
      typeof _super[name] == "function" && fnTest.test(prop[name]) ?
      (function(name, fn){
        return function() {
          var tmp = this._super;

          // Add a new ._super() method that is the same method
          // but on the super-class
          this._super = _super[name];

          // The method only need to be bound temporarily, so we
          // remove it when we're done executing
          var ret = fn.apply(this, arguments);
          this._super = tmp;

          return ret;
        };
      })(name, prop[name]) :
      prop[name];
  }

  // The dummy class constructor
  function Class() {
    // All construction is actually done in the init method
    if ( !initializing && this.init )
      this.init.apply(this, arguments);
  }

  // Populate our constructed prototype object
  Class.prototype = prototype;

  // Enforce the constructor to be what we expect
  Class.prototype.constructor = Class;

  // And make this class extendable
  Class.extend = arguments.callee;

  return Class;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.db-migrate.config"></a>[module db-migrate.config](#apidoc.module.db-migrate.config)

#### <a name="apidoc.element.db-migrate.config.load"></a>[function <span class="apidocSignatureSpan">db-migrate.config.</span>load (fileName, currentEnv)](#apidoc.element.db-migrate.config.load)
- description and source-code
```javascript
load = function (fileName, currentEnv) {
  try {
    fs.statSync(fileName);
  } catch(e) {
    throw new Error("Could not find database config file '" + fileName + "'");
  }
  var config;

  try {
    config = require(fileName);
  } catch(e) {
    // distinguish broken files from missing ones
    if (e instanceof SyntaxError){
      throw e;
    }

    config = require(path.join(process.cwd(), fileName));
  }

  for (var env in config) {
    if (typeof(config[env]) == "string") {
      exports[env] = parseDatabaseUrl(config[env]);
    } else {
      //Check config entry's for ENV objects
      //which will tell us to grab configuration from the environment
      for (var configEntry in config[env]) {
        if (config[env][configEntry] && config[env][configEntry].ENV != null){
          config[env][configEntry] =  process.env[config[env][configEntry].ENV];
        }
      }
      exports[env] = config[env];
    }
  }

  if(currentEnv) {
    setCurrent(currentEnv);
  } else if(config['default']) {
    setCurrent(config['default']);
  } else if(config.env) {
    setCurrent(config.env);
  } else {
    setCurrent(['dev', 'development']);
  }

  delete exports.load;
  delete exports.loadUrl;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.db-migrate.config.loadUrl"></a>[function <span class="apidocSignatureSpan">db-migrate.config.</span>loadUrl (databaseUrl, currentEnv)](#apidoc.element.db-migrate.config.loadUrl)
- description and source-code
```javascript
loadUrl = function (databaseUrl, currentEnv) {
  var config = parseDatabaseUrl(databaseUrl);
  if (currentEnv) {
    exports[currentEnv] = config;
    setCurrent(currentEnv);
  } else {
    exports.urlConfig = config;
    setCurrent('urlConfig');
  }

  delete exports.load;
  delete exports.loadUrl;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.db-migrate.config.setCurrent"></a>[function <span class="apidocSignatureSpan">db-migrate.config.</span>setCurrent (env)](#apidoc.element.db-migrate.config.setCurrent)
- description and source-code
```javascript
setCurrent = function (env) {
  env = dbmUtil.isArray(env) ? env : [env];

  env.forEach(function (current) {
    if (dbmUtil.isString(current) && exports[current]) {
      exports.getCurrent = function () {
        return {
          env: current,
          settings: exports[current]
        };
      };
    }
  });

  if (!exports.getCurrent) {
    throw new Error("Environment(s) '" + env.join(', ') + "' not found.");
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.db-migrate.inflection"></a>[module db-migrate.inflection](#apidoc.module.db-migrate.inflection)

#### <a name="apidoc.element.db-migrate.inflection.camelize"></a>[function <span class="apidocSignatureSpan">db-migrate.inflection.</span>camelize (str, lowFirstLetter)](#apidoc.element.db-migrate.inflection.camelize)
- description and source-code
```javascript
camelize = function (str, lowFirstLetter) {
  str = str.toLowerCase();
  var str_path = str.split('/');
  for (var i = 0; i < str_path.length; i++) {
    var str_arr = str_path[i].split('_');
    var initX = ((lowFirstLetter && i + 1 === str_path.length) ? (1) : (0));
    for (var x = initX; x < str_arr.length; x++) {
      str_arr[x] = str_arr[x].charAt(0).toUpperCase() + str_arr[x].substring(1);
    }
    str_path[i] = str_arr.join('');
  }
  str = str_path.join('::');
  return str;
}
```
- example usage
```shell
...
    str - String - string to apply inflection on
    lowFirstLetter - boolean (optional) - default is to capitalize the first
      letter of the results... passing true will lowercase it
  Returns:
    String - lower case underscored words will be returned in camel case
      additionally '/' is translated to '::'
  Examples:
    "message_properties".camelize() == "MessageProperties"
    "message_properties".camelize(true) == "messageProperties"
*/
exports.camelize = function(str, lowFirstLetter) {
str = str.toLowerCase();
var str_path = str.split('/');
for (var i = 0; i < str_path.length; i++) {
  var str_arr = str_path[i].split('_');
...
```

#### <a name="apidoc.element.db-migrate.inflection.capitalize"></a>[function <span class="apidocSignatureSpan">db-migrate.inflection.</span>capitalize (str)](#apidoc.element.db-migrate.inflection.capitalize)
- description and source-code
```javascript
capitalize = function (str) {
  str = str.toLowerCase();
  str = str.substring(0, 1).toUpperCase() + str.substring(1);
  return str;
}
```
- example usage
```shell
...
    "message_properties".humanize(true) == "message properties"
*/
exports.humanize = function(str, lowFirstLetter) {
str = str.toLowerCase();
str = str.replace(idSuffix, '');
str = str.replace(dashOrUnderbar, ' ');
if (!lowFirstLetter) {
  str = exports.capitalize(str);
}
return str;
};

/*
This function adds capitalization support to every String object
  Signature:
...
```

#### <a name="apidoc.element.db-migrate.inflection.classify"></a>[function <span class="apidocSignatureSpan">db-migrate.inflection.</span>classify (str)](#apidoc.element.db-migrate.inflection.classify)
- description and source-code
```javascript
classify = function (str) {
  str = exports.camelize(str);
  str = exports.singularize(str);
  return str;
}
```
- example usage
```shell
...
    Signature:
      classify(str) == String
    Arguments:
      str - String - string to apply inflection on
    Returns:
      String - underscored plural nouns become the camel cased singular form
    Examples:
      "message_bus_properties".classify() == "MessageBusProperty"
*/
exports.classify = function(str) {
  str = exports.camelize(str);
  str = exports.singularize(str);
  return str;
};
...
```

#### <a name="apidoc.element.db-migrate.inflection.dasherize"></a>[function <span class="apidocSignatureSpan">db-migrate.inflection.</span>dasherize (str)](#apidoc.element.db-migrate.inflection.dasherize)
- description and source-code
```javascript
dasherize = function (str) {
  str = str.replace(spaceOrUnderbar, '-');
  return str;
}
```
- example usage
```shell
...
  lpad(date.getUTCHours(), '0', 2),
  lpad(date.getUTCMinutes(), '0', 2),
  lpad(date.getUTCSeconds(), '0', 2)
].join('');
}

function formatTitle(title) {
return inflection.dasherize(title);
}

function parseDate(name) {
var date = new Date();
var match = name.match(/(\d{4})(\d{2})(\d{2})(\d{2})(\d{2})(\d{2})-[^\.]+/);
date.setUTCFullYear(match[1]);
date.setUTCDate(match[3]);
...
```

#### <a name="apidoc.element.db-migrate.inflection.demodulize"></a>[function <span class="apidocSignatureSpan">db-migrate.inflection.</span>demodulize (str)](#apidoc.element.db-migrate.inflection.demodulize)
- description and source-code
```javascript
demodulize = function (str) {
  var str_arr = str.split('::');
  str = str_arr[str_arr.length - 1];
  return str;
}
```
- example usage
```shell
...
    Signature:
      demodulize(str) == String
    Arguments:
      str - String - string to apply inflection on
    Returns:
      String - removes module names leaving only class names (Ruby style)
    Examples:
      "Message::Bus::Properties".demodulize() == "Properties"
*/
exports.demodulize = function(str) {
  var str_arr = str.split('::');
  str = str_arr[str_arr.length - 1];
  return str;
};
...
```

#### <a name="apidoc.element.db-migrate.inflection.foreignKey"></a>[function <span class="apidocSignatureSpan">db-migrate.inflection.</span>foreignKey (str, dropIdUbar)](#apidoc.element.db-migrate.inflection.foreignKey)
- description and source-code
```javascript
foreignKey = function (str, dropIdUbar) {
  str = exports.demodulize(str);
  str = exports.underscore(str);
  str = str + ((dropIdUbar) ? ('') : ('_')) + 'id';
  return str;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.db-migrate.inflection.humanize"></a>[function <span class="apidocSignatureSpan">db-migrate.inflection.</span>humanize (str, lowFirstLetter)](#apidoc.element.db-migrate.inflection.humanize)
- description and source-code
```javascript
humanize = function (str, lowFirstLetter) {
  str = str.toLowerCase();
  str = str.replace(idSuffix, '');
  str = str.replace(dashOrUnderbar, ' ');
  if (!lowFirstLetter) {
    str = exports.capitalize(str);
  }
  return str;
}
```
- example usage
```shell
...
  Arguments:
    str - String - string to apply inflection on
    lowFirstLetter - boolean (optional) - default is to capitalize the first
      letter of the results... passing true will lowercase it
  Returns:
    String - lower case underscored words will be returned in humanized form
  Examples:
    "message_properties".humanize() == "Message properties"
    "message_properties".humanize(true) == "message properties"
*/
exports.humanize = function(str, lowFirstLetter) {
str = str.toLowerCase();
str = str.replace(idSuffix, '');
str = str.replace(dashOrUnderbar, ' ');
if (!lowFirstLetter) {
...
```

#### <a name="apidoc.element.db-migrate.inflection.indexOf"></a>[function <span class="apidocSignatureSpan">db-migrate.inflection.</span>indexOf (array, item, fromIndex, compareFunc)](#apidoc.element.db-migrate.inflection.indexOf)
- description and source-code
```javascript
indexOf = function (array, item, fromIndex, compareFunc) {
  if (!fromIndex) {
    fromIndex = -1;
  }
  var index = -1;
  for (var i = fromIndex; i < array.length; i++) {
    if (array[i] === item || compareFunc && compareFunc(array[i], item)) {
      index = i;
      break;
    }
  }
  return index;
}
```
- example usage
```shell
...
  log.info('loaded extra config for migration subfolder: "' + file + '/config.json"');
  switched = true;
} catch(e) {}
  }

  db.switchDatabase((switched) ? newConf : config.database, function()
  {
global.matching = file.substr(file.indexOf(config['migrations-dir'] || 'migrations') +
    (config['migrations-dir'] || 'migrations').length + 1);

if(global.matching.length === 0)
  global.matching = '';


global.locTitle = global.matching;
...
```

#### <a name="apidoc.element.db-migrate.inflection.ordinalize"></a>[function <span class="apidocSignatureSpan">db-migrate.inflection.</span>ordinalize (str)](#apidoc.element.db-migrate.inflection.ordinalize)
- description and source-code
```javascript
ordinalize = function (str) {
  var str_arr = str.split(' ');
  for (var x = 0; x < str_arr.length; x++) {
    var i = parseInt(str_arr[x], 10);
    if (isNan(i)) {
      var ltd = str_arr[x].substring(str_arr[x].length - 2);
      var ld = str_arr[x].substring(str_arr[x].length - 1);
      var suf = "th";
      if (ltd != "11" && ltd != "12" && ltd != "13") {
        if (ld === "1") {
          suf = "st";
        } else if (ld === "2") {
          suf = "nd";
        } else if (ld === "3") {
          suf = "rd";
        }
      }
      str_arr[x] += suf;
    }
  }
  str = str_arr.join(' ');
  return str;
}
```
- example usage
```shell
...
  Signature:
    ordinalize(str) == String
  Arguments:
    str - String - string to apply inflection on
  Returns:
    String - renders all found numbers their sequence like "22nd"
  Examples:
    "the 1 pitch".ordinalize() == "the 1st pitch"
*/
exports.ordinalize = function(str) {
var str_arr = str.split(' ');
for (var x = 0; x < str_arr.length; x++) {
  var i = parseInt(str_arr[x], 10);
  if (isNan(i)) {
    var ltd = str_arr[x].substring(str_arr[x].length - 2);
...
```

#### <a name="apidoc.element.db-migrate.inflection.pluralize"></a>[function <span class="apidocSignatureSpan">db-migrate.inflection.</span>pluralize (str, plural)](#apidoc.element.db-migrate.inflection.pluralize)
- description and source-code
```javascript
pluralize = function (str, plural) {
  return applyRules(str, pluralRules, uncountableWords, plural);
}
```
- example usage
```shell
...
      pluralize(str, plural) == String
    Arguments:
      str - String - string to apply inflection on
      plural - String (optional) - overrides normal output with said String
    Returns:
      String - singular English language nouns are returned in plural form
    Examples:
      "person".pluralize() == "people"
      "octopus".pluralize() == "octopi"
      "Hat".pluralize() == "Hats"
      "person".pluralize("guys") == "guys"
*/
exports.pluralize = function(str, plural) {
  return applyRules(str, pluralRules, uncountableWords, plural);
};
...
```

#### <a name="apidoc.element.db-migrate.inflection.singularize"></a>[function <span class="apidocSignatureSpan">db-migrate.inflection.</span>singularize (str, singular)](#apidoc.element.db-migrate.inflection.singularize)
- description and source-code
```javascript
singularize = function (str, singular) {
  return applyRules(str, singularRules, uncountableWords, singular);
}
```
- example usage
```shell
...
      singularize(str, singular) == String
    Arguments:
      str - String - string to apply inflection on
      singular - String (optional) - overrides normal output with said String
    Returns:
      String - plural English language nouns are returned in singular form
    Examples:
      "people".singularize() == "person"
      "octopi".singularize() == "octopus"
      "Hats".singularize() == "Hat"
      "guys".singularize("person") == "person"
*/
exports.singularize = function(str, singular) {
  return applyRules(str, singularRules, uncountableWords, singular);
};
...
```

#### <a name="apidoc.element.db-migrate.inflection.tableize"></a>[function <span class="apidocSignatureSpan">db-migrate.inflection.</span>tableize (str)](#apidoc.element.db-migrate.inflection.tableize)
- description and source-code
```javascript
tableize = function (str) {
  str = exports.underscore(str);
  str = exports.pluralize(str);
  return str;
}
```
- example usage
```shell
...
    Signature:
      tableize(str) == String
    Arguments:
      str - String - string to apply inflection on
    Returns:
      String - renders camel cased words into their underscored plural form
    Examples:
      "MessageBusProperty".tableize() == "message_bus_properties"
*/
exports.tableize = function(str) {
  str = exports.underscore(str);
  str = exports.pluralize(str);
  return str;
};
...
```

#### <a name="apidoc.element.db-migrate.inflection.titleize"></a>[function <span class="apidocSignatureSpan">db-migrate.inflection.</span>titleize (str)](#apidoc.element.db-migrate.inflection.titleize)
- description and source-code
```javascript
titleize = function (str) {
  str = str.toLowerCase();
  str = str.replace(underbar, ' ');
  var str_arr = str.split(' ');
  for (var x = 0; x < str_arr.length; x++) {
    var d = str_arr[x].split('-');
    for (var i = 0; i < d.length; i++) {
      if (nonTitlecasedWords.indexOf(d[i].toLowerCase()) < 0) {
        d[i] = exports.capitalize(d[i]);
      }
    }
    str_arr[x] = d.join('-');
  }
  str = str_arr.join(' ');
  str = str.substring(0, 1).toUpperCase() + str.substring(1);
  return str;
}
```
- example usage
```shell
...
  Signature:
    titleize(str) == String
  Arguments:
    str - String - string to apply inflection on
  Returns:
    String - capitalizes words as you would for a book title
  Examples:
    "message_properties".titleize() == "Message Properties"
    "message properties to keep".titleize() == "Message Properties to Keep"
*/
exports.titleize = function(str) {
str = str.toLowerCase();
str = str.replace(underbar, ' ');
var str_arr = str.split(' ');
for (var x = 0; x < str_arr.length; x++) {
...
```

#### <a name="apidoc.element.db-migrate.inflection.underscore"></a>[function <span class="apidocSignatureSpan">db-migrate.inflection.</span>underscore (str)](#apidoc.element.db-migrate.inflection.underscore)
- description and source-code
```javascript
underscore = function (str) {
  var str_path = str.split('::');
  for (var i = 0; i < str_path.length; i++) {
    str_path[i] = str_path[i].replace(uppercase, '_$1');
    str_path[i] = str_path[i].replace(underbarPrefix, '');
  }
  str = str_path.join('/').toLowerCase();
  return str;
}
```
- example usage
```shell
...
  Arguments:
    str - String - string to apply inflection on
  Returns:
    String - camel cased words are returned as lower cased and underscored
      additionally '::' is translated to '/'
  Examples:
    "MessageProperties".camelize() == "message_properties"
    "messageProperties".underscore() == "message_properties"
*/
exports.underscore = function(str) {
var str_path = str.split('::');
for (var i = 0; i < str_path.length; i++) {
  str_path[i] = str_path[i].replace(uppercase, '_$1');
  str_path[i] = str_path[i].replace(underbarPrefix, '');
}
...
```



# <a name="apidoc.module.db-migrate.migration"></a>[module db-migrate.migration](#apidoc.module.db-migrate.migration)

#### <a name="apidoc.element.db-migrate.migration.migration"></a>[function <span class="apidocSignatureSpan">db-migrate.</span>migration ()](#apidoc.element.db-migrate.migration.migration)
- description and source-code
```javascript
migration = function () {
  if (arguments.length >= 3) {
    this.title = arguments[0];
    this.date = arguments[2];
    this.name = formatName(this.title, this.date);
    this.path = formatPath(arguments[1], this.name);
    this.templateType = arguments[3];
  } else if (arguments.length == 1) {
    this.path = arguments[0];
    this.name = Migration.parseName(this.path);
    this.date = parseDate(this.name);
    this.title = parseTitle(this.name);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.db-migrate.migration.loadFromDatabase"></a>[function <span class="apidocSignatureSpan">db-migrate.migration.</span>loadFromDatabase (dir, driver, callback)](#apidoc.element.db-migrate.migration.loadFromDatabase)
- description and source-code
```javascript
loadFromDatabase = function (dir, driver, callback) {
  log.verbose('loading migrations from database');
  driver.allLoadedMigrations(function(err, dbResults) {
    if (err && !global.dryRun) { callback(err); return; }
    else if (err && global.dryRun) {
      dbResults = []
    }
    var migrations = dbResults.filter(function(result) {
      return result.name.substr(0,result.name.lastIndexOf('/')) === global.matching;
    }).map(function(result) {
      return new Migration(path.join(dir, result.name));
    });

    callback(null, migrations);
  });
}
```
- example usage
```shell
...
  },

  upToBy: function(partialName, count, callback) {
    var self = this;
    Migration.loadFromFilesystem(self.migrationsDir, function(err, allMigrations) {
      if (err) { callback(err); return; }

      Migration.loadFromDatabase(self.migrationsDir, self.driver, function(err, completedMigrations) {
if (err) { callback(err); return; }
var toRun = filterUp(allMigrations, completedMigrations, partialName, count);

if (toRun.length === 0) {
  log.info('No migrations to run');
  callback(null);
  return;
...
```

#### <a name="apidoc.element.db-migrate.migration.loadFromFilesystem"></a>[function <span class="apidocSignatureSpan">db-migrate.migration.</span>loadFromFilesystem (dir, callback)](#apidoc.element.db-migrate.migration.loadFromFilesystem)
- description and source-code
```javascript
loadFromFilesystem = function (dir, callback) {
  log.verbose('loading migrations from dir', dir);
  fs.readdir(dir, function(err, files) {
    if (err) { callback(err); return; }
    var coffeeWarn = true;
    files = files.filter(function(file) {
      if (coffeeWarn && !coffeeSupported && /\.coffee$/.test(file)) {
        log.warn('CoffeeScript not installed');
        coffeeWarn = false;
      }
      return filesRegEx.test(file);
    });
    var migrations = files.sort().map(function(file) {
      return new Migration(path.join(dir, file));
    });
    callback(null, migrations);
  });
}
```
- example usage
```shell
...
    } else {
      this.downToBy(funcOrOpts.count, callback);
    }
  },

  upToBy: function(partialName, count, callback) {
    var self = this;
    Migration.loadFromFilesystem(self.migrationsDir, function(err, allMigrations) {
      if (err) { callback(err); return; }

      Migration.loadFromDatabase(self.migrationsDir, self.driver, function(err, completedMigrations) {
if (err) { callback(err); return; }
var toRun = filterUp(allMigrations, completedMigrations, partialName, count);

if (toRun.length === 0) {
...
```

#### <a name="apidoc.element.db-migrate.migration.parseName"></a>[function <span class="apidocSignatureSpan">db-migrate.migration.</span>parseName (path)](#apidoc.element.db-migrate.migration.parseName)
- description and source-code
```javascript
parseName = function (path) {
  var match = path.match(/(\d{14}-[^.]+)(?:\.*?)?/);
  return match[1];
}
```
- example usage
```shell
...
  this.title = arguments[0];
  this.date = arguments[2];
  this.name = formatName(this.title, this.date);
  this.path = formatPath(arguments[1], this.name);
  this.templateType = arguments[3];
} else if (arguments.length == 1) {
  this.path = arguments[0];
  this.name = Migration.parseName(this.path);
  this.date = parseDate(this.name);
  this.title = parseTitle(this.name);
}
};

Migration.prototype.defaultCoffeeTemplate = function() {
return [
...
```



# <a name="apidoc.module.db-migrate.migration.prototype"></a>[module db-migrate.migration.prototype](#apidoc.module.db-migrate.migration.prototype)

#### <a name="apidoc.element.db-migrate.migration.prototype._down"></a>[function <span class="apidocSignatureSpan">db-migrate.migration.prototype.</span>_down ()](#apidoc.element.db-migrate.migration.prototype._down)
- description and source-code
```javascript
_down = function () {
  return require(this.path).down.apply(this, arguments);
}
```
- example usage
```shell
...
};

Migration.prototype.up = function(db, callback) {
  this._up(db, callback);
};

Migration.prototype.down = function(db, callback) {
  this._down(db, callback);
};

Migration.parseName = function(path) {
  var match = path.match(/(\d{14}-[^.]+)(?:\.*?)?/);
  return match[1];
};
...
```

#### <a name="apidoc.element.db-migrate.migration.prototype._up"></a>[function <span class="apidocSignatureSpan">db-migrate.migration.prototype.</span>_up ()](#apidoc.element.db-migrate.migration.prototype._up)
- description and source-code
```javascript
_up = function () {
  return require(this.path).up.apply(this, arguments);
}
```
- example usage
```shell
...
};

Migration.prototype.write = function(callback) {
  fs.writeFile(this.path, this.getTemplate(), callback);
};

Migration.prototype.up = function(db, callback) {
  this._up(db, callback);
};

Migration.prototype.down = function(db, callback) {
  this._down(db, callback);
};

Migration.parseName = function(path) {
...
```

#### <a name="apidoc.element.db-migrate.migration.prototype.defaultCoffeeTemplate"></a>[function <span class="apidocSignatureSpan">db-migrate.migration.prototype.</span>defaultCoffeeTemplate ()](#apidoc.element.db-migrate.migration.prototype.defaultCoffeeTemplate)
- description and source-code
```javascript
defaultCoffeeTemplate = function () {
  return [
    "var dbm = -> global.dbm or require 'db-migrate'",
    "type   = dbm.dataType",
    "",
    "exports.up = (db, callback) ->",
    "",
    "",
    "exports.down = (db, callback) ->",
    "",
    "",
    ""
  ].join("\n");
}
```
- example usage
```shell
...
Migration.prototype.getTemplate = function() {
  switch (this.templateType) {
    case Migration.TemplateType.DEFAULT_SQL:
      return this.defaultSqlTemplate();
    case Migration.TemplateType.SQL_FILE_LOADER:
      return this.sqlFileLoaderTemplate();
    case Migration.TemplateType.DEFAULT_COFFEE:
      return this.defaultCoffeeTemplate();
    case Migration.TemplateType.DEFAULT_JS:
    default:
      return this.defaultJsTemplate();
  }
};

Migration.prototype._up = function() {
...
```

#### <a name="apidoc.element.db-migrate.migration.prototype.defaultJsTemplate"></a>[function <span class="apidocSignatureSpan">db-migrate.migration.prototype.</span>defaultJsTemplate ()](#apidoc.element.db-migrate.migration.prototype.defaultJsTemplate)
- description and source-code
```javascript
defaultJsTemplate = function () {
  return [
    "var dbm = global.dbm || require('db-migrate');",
    "var type = dbm.dataType;",
    "",
    "exports.up = function(db, callback) {",
    "  callback();",
    "};",
    "",
    "exports.down = function(db, callback) {",
    "  callback();",
    "};",
    ""
  ].join("\n");
}
```
- example usage
```shell
...
      return this.defaultSqlTemplate();
    case Migration.TemplateType.SQL_FILE_LOADER:
      return this.sqlFileLoaderTemplate();
    case Migration.TemplateType.DEFAULT_COFFEE:
      return this.defaultCoffeeTemplate();
    case Migration.TemplateType.DEFAULT_JS:
    default:
      return this.defaultJsTemplate();
  }
};

Migration.prototype._up = function() {
  return require(this.path).up.apply(this, arguments);
};
...
```

#### <a name="apidoc.element.db-migrate.migration.prototype.defaultSqlTemplate"></a>[function <span class="apidocSignatureSpan">db-migrate.migration.prototype.</span>defaultSqlTemplate ()](#apidoc.element.db-migrate.migration.prototype.defaultSqlTemplate)
- description and source-code
```javascript
defaultSqlTemplate = function () {
  return "/* Replace with your SQL commands */";
}
```
- example usage
```shell
...
SQL_FILE_LOADER: 2,
DEFAULT_COFFEE: 3
};

Migration.prototype.getTemplate = function() {
switch (this.templateType) {
  case Migration.TemplateType.DEFAULT_SQL:
    return this.defaultSqlTemplate();
  case Migration.TemplateType.SQL_FILE_LOADER:
    return this.sqlFileLoaderTemplate();
  case Migration.TemplateType.DEFAULT_COFFEE:
    return this.defaultCoffeeTemplate();
  case Migration.TemplateType.DEFAULT_JS:
  default:
    return this.defaultJsTemplate();
...
```

#### <a name="apidoc.element.db-migrate.migration.prototype.down"></a>[function <span class="apidocSignatureSpan">db-migrate.migration.prototype.</span>down (db, callback)](#apidoc.element.db-migrate.migration.prototype.down)
- description and source-code
```javascript
down = function (db, callback) {
  this._down(db, callback);
}
```
- example usage
```shell
...
        log.info('No migrations to run');
        callback(null);
        return;
      }

      async.forEachSeries(toRun, function(migration, next) {
        log.verbose('preparing to run down migration:', migration.name);
        self.down(migration.down.bind(migration), function(err) {
          if (err) { callback(err); return; }
          self.deleteMigrationRecord(migration, next);
        });
      }, callback);
    });
  }
};
...
```

#### <a name="apidoc.element.db-migrate.migration.prototype.getTemplate"></a>[function <span class="apidocSignatureSpan">db-migrate.migration.prototype.</span>getTemplate ()](#apidoc.element.db-migrate.migration.prototype.getTemplate)
- description and source-code
```javascript
getTemplate = function () {
  switch (this.templateType) {
    case Migration.TemplateType.DEFAULT_SQL:
      return this.defaultSqlTemplate();
    case Migration.TemplateType.SQL_FILE_LOADER:
      return this.sqlFileLoaderTemplate();
    case Migration.TemplateType.DEFAULT_COFFEE:
      return this.defaultCoffeeTemplate();
    case Migration.TemplateType.DEFAULT_JS:
    default:
      return this.defaultJsTemplate();
  }
}
```
- example usage
```shell
...
};

Migration.prototype._down = function() {
  return require(this.path).down.apply(this, arguments);
};

Migration.prototype.write = function(callback) {
  fs.writeFile(this.path, this.getTemplate(), callback);
};

Migration.prototype.up = function(db, callback) {
  this._up(db, callback);
};

Migration.prototype.down = function(db, callback) {
...
```

#### <a name="apidoc.element.db-migrate.migration.prototype.sqlFileLoaderTemplate"></a>[function <span class="apidocSignatureSpan">db-migrate.migration.prototype.</span>sqlFileLoaderTemplate ()](#apidoc.element.db-migrate.migration.prototype.sqlFileLoaderTemplate)
- description and source-code
```javascript
sqlFileLoaderTemplate = function () {
  return [
    "var dbm = global.dbm || require('db-migrate');",
    "var type = dbm.dataType;",
    "var fs = require('fs');",
    "var path = require('path');",
    "",
    "exports.up = function(db, callback) {",
    "  var filePath = path.join(__dirname + '/sqls/"+this.name.replace('.js', '')+"-up.sql');",
    "  fs.readFile(filePath, {encoding: 'utf-8'}, function(err,data){",
    "    if (err) return callback(err);",
    "      console.log('received data: ' + data);",
    "",
    "    db.runSql(data, function(err) {",
    "      if (err) return callback(err);",
    "      callback();",
    "    });",
    "  });",
    "};",
    "",
    "exports.down = function(db, callback) {",
    "  var filePath = path.join(__dirname + '/sqls/"+this.name.replace('.js', '')+"-down.sql');",
    "  fs.readFile(filePath, {encoding: 'utf-8'}, function(err,data){",
    "    if (err) return callback(err);",
    "      console.log('received data: ' + data);",
    "",
    "    db.runSql(data, function(err) {",
    "      if (err) return callback(err);",
    "      callback();",
    "    });",
    "  });",
    "};",
    ""
  ].join("\n");
}
```
- example usage
```shell
...
};

Migration.prototype.getTemplate = function() {
  switch (this.templateType) {
    case Migration.TemplateType.DEFAULT_SQL:
      return this.defaultSqlTemplate();
    case Migration.TemplateType.SQL_FILE_LOADER:
      return this.sqlFileLoaderTemplate();
    case Migration.TemplateType.DEFAULT_COFFEE:
      return this.defaultCoffeeTemplate();
    case Migration.TemplateType.DEFAULT_JS:
    default:
      return this.defaultJsTemplate();
  }
};
...
```

#### <a name="apidoc.element.db-migrate.migration.prototype.up"></a>[function <span class="apidocSignatureSpan">db-migrate.migration.prototype.</span>up (db, callback)](#apidoc.element.db-migrate.migration.prototype.up)
- description and source-code
```javascript
up = function (db, callback) {
  this._up(db, callback);
}
```
- example usage
```shell
...
      callback(null);
      return;
    }

    async.forEachSeries(toRun, function(migration, next) {
      log.verbose('preparing to run up migration:', migration.name);
      self.driver.startMigration(function() {
        self.up(migration.up.bind(migration), function(err) {
          if (err) { callback(err); return; }
          self.writeMigrationRecord(migration, function() { self.driver.endMigration(next); });
        });
      });
    }, callback);
  });
});
...
```

#### <a name="apidoc.element.db-migrate.migration.prototype.write"></a>[function <span class="apidocSignatureSpan">db-migrate.migration.prototype.</span>write (callback)](#apidoc.element.db-migrate.migration.prototype.write)
- description and source-code
```javascript
write = function (callback) {
  fs.writeFile(this.path, this.getTemplate(), callback);
}
```
- example usage
```shell
...
    if(typeof(cb) === 'function')
      cb();

  });
}

exports.createMigration = function(migration, callback) {
  migration.write(function(err) {
  if (err) { callback(err); return; }
  callback(null, migration);
  });
};
...
```



# <a name="apidoc.module.db-migrate.migrator"></a>[module db-migrate.migrator](#apidoc.module.db-migrate.migrator)

#### <a name="apidoc.element.db-migrate.migrator.migrator"></a>[function <span class="apidocSignatureSpan">db-migrate.</span>migrator (driver, migrationsDir)](#apidoc.element.db-migrate.migrator.migrator)
- description and source-code
```javascript
migrator = function (driver, migrationsDir) {
  this.driver = driver;
  this.migrationsDir = migrationsDir;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.db-migrate.migrator.prototype"></a>[module db-migrate.migrator.prototype](#apidoc.module.db-migrate.migrator.prototype)

#### <a name="apidoc.element.db-migrate.migrator.prototype.createMigrationTable"></a>[function <span class="apidocSignatureSpan">db-migrate.migrator.prototype.</span>createMigrationTable (callback)](#apidoc.element.db-migrate.migrator.prototype.createMigrationTable)
- description and source-code
```javascript
createMigrationTable = function (callback) {
  this.driver.createMigrationTable(callback);
}
```
- example usage
```shell
...
Migrator = function(driver, migrationsDir) {
this.driver = driver;
this.migrationsDir = migrationsDir;
};

Migrator.prototype = {
createMigrationTable: function(callback) {
  this.driver.createMigrationTable(callback);
},

writeMigrationRecord: function(migration, callback) {
  function onComplete(err) {
    if (err) {
      log.error(migration.name, err);
    } else {
...
```

#### <a name="apidoc.element.db-migrate.migrator.prototype.deleteMigrationRecord"></a>[function <span class="apidocSignatureSpan">db-migrate.migrator.prototype.</span>deleteMigrationRecord (migration, callback)](#apidoc.element.db-migrate.migrator.prototype.deleteMigrationRecord)
- description and source-code
```javascript
deleteMigrationRecord = function (migration, callback) {
  function onComplete(err) {
    if (err) {
      log.error(migration.name, err);
    } else {
      log.info('Processed migration', migration.name);
    }
    callback(err);
  }
  this.driver.deleteMigration(global.matching + '/' + migration.name, function(err) {

    if(!global.matching) {

      this.driver.deleteMigration(migration.name, onComplete);
    }
    else {

      onComplete.apply(err);
    }
  }.bind(this));
}
```
- example usage
```shell
...
        return;
      }

      async.forEachSeries(toRun, function(migration, next) {
        log.verbose('preparing to run down migration:', migration.name);
        self.down(migration.down.bind(migration), function(err) {
          if (err) { callback(err); return; }
          self.deleteMigrationRecord(migration, next);
        });
      }, callback);
    });
  }
};

module.exports = Migrator;
...
```

#### <a name="apidoc.element.db-migrate.migrator.prototype.down"></a>[function <span class="apidocSignatureSpan">db-migrate.migrator.prototype.</span>down (funcOrOpts, callback)](#apidoc.element.db-migrate.migrator.prototype.down)
- description and source-code
```javascript
down = function (funcOrOpts, callback) {
  if (dbmUtil.isFunction(funcOrOpts)) {
    funcOrOpts(this.driver, callback);
  } else {
    this.downToBy(funcOrOpts.count, callback);
  }
}
```
- example usage
```shell
...
        log.info('No migrations to run');
        callback(null);
        return;
      }

      async.forEachSeries(toRun, function(migration, next) {
        log.verbose('preparing to run down migration:', migration.name);
        self.down(migration.down.bind(migration), function(err) {
          if (err) { callback(err); return; }
          self.deleteMigrationRecord(migration, next);
        });
      }, callback);
    });
  }
};
...
```

#### <a name="apidoc.element.db-migrate.migrator.prototype.downToBy"></a>[function <span class="apidocSignatureSpan">db-migrate.migrator.prototype.</span>downToBy (count, callback)](#apidoc.element.db-migrate.migrator.prototype.downToBy)
- description and source-code
```javascript
downToBy = function (count, callback) {
  var self = this;
  Migration.loadFromDatabase(self.migrationsDir, self.driver, function(err, completedMigrations) {
    if (err) { return callback(err); }

    var toRun = filterDown(completedMigrations, count);

    if (toRun.length === 0) {
      log.info('No migrations to run');
      callback(null);
      return;
    }

    async.forEachSeries(toRun, function(migration, next) {
      log.verbose('preparing to run down migration:', migration.name);
      self.down(migration.down.bind(migration), function(err) {
        if (err) { callback(err); return; }
        self.deleteMigrationRecord(migration, next);
      });
    }, callback);
  });
}
```
- example usage
```shell
...
  }
},

down: function(funcOrOpts, callback) {
  if (dbmUtil.isFunction(funcOrOpts)) {
    funcOrOpts(this.driver, callback);
  } else {
    this.downToBy(funcOrOpts.count, callback);
  }
},

upToBy: function(partialName, count, callback) {
  var self = this;
  Migration.loadFromFilesystem(self.migrationsDir, function(err, allMigrations) {
    if (err) { callback(err); return; }
...
```

#### <a name="apidoc.element.db-migrate.migrator.prototype.up"></a>[function <span class="apidocSignatureSpan">db-migrate.migrator.prototype.</span>up (funcOrOpts, callback)](#apidoc.element.db-migrate.migrator.prototype.up)
- description and source-code
```javascript
up = function (funcOrOpts, callback) {
  if (dbmUtil.isFunction(funcOrOpts)) {
    funcOrOpts(this.driver, callback);
  } else {
    this.upToBy(funcOrOpts.destination, funcOrOpts.count, callback);
  }
}
```
- example usage
```shell
...
      callback(null);
      return;
    }

    async.forEachSeries(toRun, function(migration, next) {
      log.verbose('preparing to run up migration:', migration.name);
      self.driver.startMigration(function() {
        self.up(migration.up.bind(migration), function(err) {
          if (err) { callback(err); return; }
          self.writeMigrationRecord(migration, function() { self.driver.endMigration(next); });
        });
      });
    }, callback);
  });
});
...
```

#### <a name="apidoc.element.db-migrate.migrator.prototype.upToBy"></a>[function <span class="apidocSignatureSpan">db-migrate.migrator.prototype.</span>upToBy (partialName, count, callback)](#apidoc.element.db-migrate.migrator.prototype.upToBy)
- description and source-code
```javascript
upToBy = function (partialName, count, callback) {
  var self = this;
  Migration.loadFromFilesystem(self.migrationsDir, function(err, allMigrations) {
    if (err) { callback(err); return; }

    Migration.loadFromDatabase(self.migrationsDir, self.driver, function(err, completedMigrations) {
      if (err) { callback(err); return; }
      var toRun = filterUp(allMigrations, completedMigrations, partialName, count);

      if (toRun.length === 0) {
        log.info('No migrations to run');
        callback(null);
        return;
      }

      async.forEachSeries(toRun, function(migration, next) {
        log.verbose('preparing to run up migration:', migration.name);
        self.driver.startMigration(function() {
          self.up(migration.up.bind(migration), function(err) {
            if (err) { callback(err); return; }
            self.writeMigrationRecord(migration, function() { self.driver.endMigration(next); });
          });
        });
      }, callback);
    });
  });
}
```
- example usage
```shell
...
  }.bind(this));
},

up: function(funcOrOpts, callback) {
  if (dbmUtil.isFunction(funcOrOpts)) {
    funcOrOpts(this.driver, callback);
  } else {
    this.upToBy(funcOrOpts.destination, funcOrOpts.count, callback);
  }
},

down: function(funcOrOpts, callback) {
  if (dbmUtil.isFunction(funcOrOpts)) {
    funcOrOpts(this.driver, callback);
  } else {
...
```

#### <a name="apidoc.element.db-migrate.migrator.prototype.writeMigrationRecord"></a>[function <span class="apidocSignatureSpan">db-migrate.migrator.prototype.</span>writeMigrationRecord (migration, callback)](#apidoc.element.db-migrate.migrator.prototype.writeMigrationRecord)
- description and source-code
```javascript
writeMigrationRecord = function (migration, callback) {
  function onComplete(err) {
    if (err) {
      log.error(migration.name, err);
    } else {
      log.info('Processed migration', migration.name);
    }
    callback(err);
  }
  this.driver.addMigrationRecord(global.matching + '/' + migration.name, onComplete);
}
```
- example usage
```shell
...
      }

      async.forEachSeries(toRun, function(migration, next) {
        log.verbose('preparing to run up migration:', migration.name);
        self.driver.startMigration(function() {
          self.up(migration.up.bind(migration), function(err) {
            if (err) { callback(err); return; }
            self.writeMigrationRecord(migration, function() { self.driver.endMigration(next); });
          });
        });
      }, callback);
    });
  });
},
...
```



# <a name="apidoc.module.db-migrate.util"></a>[module db-migrate.util](#apidoc.module.db-migrate.util)

#### <a name="apidoc.element.db-migrate.util.isArray"></a>[function <span class="apidocSignatureSpan">db-migrate.util.</span>isArray (obj)](#apidoc.element.db-migrate.util.isArray)
- description and source-code
```javascript
isArray = function (obj) {
  return Object.prototype.toString.call(obj) == '[object Array]';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.db-migrate.util.isFunction"></a>[function <span class="apidocSignatureSpan">db-migrate.util.</span>isFunction (obj)](#apidoc.element.db-migrate.util.isFunction)
- description and source-code
```javascript
isFunction = function (obj) {
  return typeof(obj) == 'function';
}
```
- example usage
```shell
...

      onComplete.apply(err);
    }
  }.bind(this));
},

up: function(funcOrOpts, callback) {
  if (dbmUtil.isFunction(funcOrOpts)) {
    funcOrOpts(this.driver, callback);
  } else {
    this.upToBy(funcOrOpts.destination, funcOrOpts.count, callback);
  }
},

down: function(funcOrOpts, callback) {
...
```

#### <a name="apidoc.element.db-migrate.util.isString"></a>[function <span class="apidocSignatureSpan">db-migrate.util.</span>isString (obj)](#apidoc.element.db-migrate.util.isString)
- description and source-code
```javascript
isString = function (obj) {
  return typeof(obj) == 'string';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.db-migrate.util.lpad"></a>[function <span class="apidocSignatureSpan">db-migrate.util.</span>lpad (str, padChar, totalLength)](#apidoc.element.db-migrate.util.lpad)
- description and source-code
```javascript
lpad = function (str, padChar, totalLength) {
  str = str.toString();
  var neededPadding = totalLength - str.length;
  for (var i = 0; i < neededPadding; i++) {
    str = padChar + str;
  }
  return str;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.db-migrate.util.shallowCopy"></a>[function <span class="apidocSignatureSpan">db-migrate.util.</span>shallowCopy (obj)](#apidoc.element.db-migrate.util.shallowCopy)
- description and source-code
```javascript
shallowCopy = function (obj) {
  var newObj = {};
  for (var prop in obj) {
    newObj[prop] = obj[prop];
  }
  return newObj;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.db-migrate.util.toArray"></a>[function <span class="apidocSignatureSpan">db-migrate.util.</span>toArray (obj)](#apidoc.element.db-migrate.util.toArray)
- description and source-code
```javascript
toArray = function (obj) {
  var arr = [];
  for (var prop in obj) {
    arr[prop] = obj[prop];
  }
  return arr;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
