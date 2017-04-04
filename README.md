# api documentation for  [idb (v2.0.1)](https://github.com/jakearchibald/indexeddb-promised#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-idb.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-idb) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-idb.svg)](https://travis-ci.org/npmdoc/node-npmdoc-idb)
#### IndexedDB but with promises

[![NPM](https://nodei.co/npm/idb.png?downloads=true)](https://www.npmjs.com/package/idb)

[![apidoc](https://npmdoc.github.io/node-npmdoc-idb/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-idb_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-idb/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-idb/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-idb/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Jake Archibald"
    },
    "browser": "lib/idb.js",
    "bugs": {
        "url": "https://github.com/jakearchibald/indexeddb-promised/issues"
    },
    "dependencies": {},
    "description": "IndexedDB but with promises",
    "devDependencies": {
        "babelify": "^6.1.3",
        "browser-sync": "^2.8.2",
        "browserify": "^11.0.1",
        "del": "^1.2.0",
        "es6-promise": "^3.0.2",
        "gulp": "^3.9.0",
        "gulp-load-plugins": "^0.10.0",
        "gulp-size": "^1.2.3",
        "gulp-sourcemaps": "^1.5.2",
        "gulp-util": "^3.0.6",
        "merge-stream": "^0.1.8",
        "mocha": "^2.2.5",
        "run-sequence": "^1.1.2",
        "uglifyify": "^3.0.1",
        "vinyl-buffer": "^1.0.0",
        "vinyl-source-stream": "^1.1.0",
        "watchify": "^3.3.1"
    },
    "directories": {},
    "dist": {
        "shasum": "93359f84b932cff87d847530844f58444f49afa2",
        "tarball": "https://registry.npmjs.org/idb/-/idb-2.0.1.tgz"
    },
    "gitHead": "547f091a09304ec19e3e6cafb9a671f0210ce8f2",
    "homepage": "https://github.com/jakearchibald/indexeddb-promised#readme",
    "license": "ISC",
    "main": "lib/node.js",
    "maintainers": [
        {
            "name": "jaffathecake",
            "email": "jaffathecake@gmail.com"
        }
    ],
    "name": "idb",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/jakearchibald/indexeddb-promised.git"
    },
    "scripts": {
        "serve": "gulp serve",
        "test": "echo \"Error: no test specified\" && exit 1"
    },
    "typings": "lib/idb.d.ts",
    "version": "2.0.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module idb](#apidoc.module.idb)
1.  [function <span class="apidocSignatureSpan">idb.</span>delete ()](#apidoc.element.idb.delete)
1.  [function <span class="apidocSignatureSpan">idb.</span>open ()](#apidoc.element.idb.open)



# <a name="apidoc.module.idb"></a>[module idb](#apidoc.module.idb)

#### <a name="apidoc.element.idb.delete"></a>[function <span class="apidocSignatureSpan">idb.</span>delete ()](#apidoc.element.idb.delete)
- description and source-code
```javascript
delete = function () {
  return Promise.reject('IDB requires a browser environment');
}
```
- example usage
```shell
...
    tx.objectStore('keyval').put(val, key);
    return tx.complete;
  });
},
delete(key) {
  return dbPromise.then(db => {
    const tx = db.transaction('keyval', 'readwrite');
    tx.objectStore('keyval').delete(key);
    return tx.complete;
  });
},
clear() {
  return dbPromise.then(db => {
    const tx = db.transaction('keyval', 'readwrite');
    tx.objectStore('keyval').clear();
...
```

#### <a name="apidoc.element.idb.open"></a>[function <span class="apidocSignatureSpan">idb.</span>open ()](#apidoc.element.idb.open)
- description and source-code
```javascript
open = function () {
  return Promise.reject('IDB requires a browser environment');
}
```
- example usage
```shell
...
# Examples

## Keyval Store

This is very similar to 'localStorage', but async. If this is *all* you need, you may be interested in [idb-keyval](https://www.
npmjs.com/package/idb-keyval), you can always upgrade to this library later.

'''js
const dbPromise = idb.open('keyval-store', 1, upgradeDB => {
upgradeDB.createObjectStore('keyval');
});

const idbKeyval = {
get(key) {
  return dbPromise.then(db => {
    return db.transaction('keyval')
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
