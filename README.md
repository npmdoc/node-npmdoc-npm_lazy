# api documentation for  [npm_lazy (v1.14.0)](https://github.com/mixu/npm_lazy#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-npm_lazy.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-npm_lazy) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-npm_lazy.svg)](https://travis-ci.org/npmdoc/node-npmdoc-npm_lazy)
#### Lazy local npm cache server

[![NPM](https://nodei.co/npm/npm_lazy.png?downloads=true)](https://www.npmjs.com/package/npm_lazy)

[![apidoc](https://npmdoc.github.io/node-npmdoc-npm_lazy/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-npm_lazy_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-npm_lazy/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-npm_lazy/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-npm_lazy/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "bin": {
        "npm_lazy": "./bin/npm_lazy"
    },
    "bugs": {
        "url": "https://github.com/mixu/npm_lazy/issues"
    },
    "dependencies": {
        "bytes": "~2.4.0",
        "file-fixture": "0.0.2",
        "microee": "0.0.6",
        "minilog": "~3.1.0",
        "mixu_minimal": "0.0.1",
        "mkdirp": "~0.5.1",
        "request": "~2.79.0",
        "yargs": "~6.6.0"
    },
    "description": "Lazy local npm cache server",
    "devDependencies": {
        "mocha": "*"
    },
    "directories": {},
    "dist": {
        "shasum": "feda1a7ab3a6b1da87a80234f151a46d79dc24e2",
        "tarball": "https://registry.npmjs.org/npm_lazy/-/npm_lazy-1.14.0.tgz"
    },
    "gitHead": "0291f72d4d0f0818189751675f8f0fe8de0f05d0",
    "homepage": "https://github.com/mixu/npm_lazy#readme",
    "keywords": [
        "mirror",
        "npm",
        "registry"
    ],
    "license": "BSD-3-Clause",
    "main": "./server.js",
    "maintainers": [
        {
            "name": "cl0sey",
            "email": "christopher.close@gmail.com"
        },
        {
            "name": "mixu",
            "email": "mixu@mixu.net"
        }
    ],
    "name": "npm_lazy",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/mixu/npm_lazy.git"
    },
    "scripts": {
        "start": "node server.js"
    },
    "version": "1.14.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module npm_lazy](#apidoc.module.npm_lazy)
1.  [function <span class="apidocSignatureSpan">npm_lazy.</span>cache (opts)](#apidoc.element.npm_lazy.cache)
1.  [function <span class="apidocSignatureSpan">npm_lazy.</span>lifecycle ()](#apidoc.element.npm_lazy.lifecycle)
1.  [function <span class="apidocSignatureSpan">npm_lazy.</span>package ()](#apidoc.element.npm_lazy.package)
1.  [function <span class="apidocSignatureSpan">npm_lazy.</span>resource (url, auth)](#apidoc.element.npm_lazy.resource)
1.  object <span class="apidocSignatureSpan">npm_lazy.</span>api
1.  object <span class="apidocSignatureSpan">npm_lazy.</span>cache.prototype
1.  object <span class="apidocSignatureSpan">npm_lazy.</span>etag
1.  object <span class="apidocSignatureSpan">npm_lazy.</span>lifecycle.prototype
1.  object <span class="apidocSignatureSpan">npm_lazy.</span>resource.prototype
1.  object <span class="apidocSignatureSpan">npm_lazy.</span>verify

#### [module npm_lazy.api](#apidoc.module.npm_lazy.api)
1.  [function <span class="apidocSignatureSpan">npm_lazy.api.</span>configure (config)](#apidoc.element.npm_lazy.api.configure)
1.  object <span class="apidocSignatureSpan">npm_lazy.api.</span>routes

#### [module npm_lazy.cache](#apidoc.module.npm_lazy.cache)
1.  [function <span class="apidocSignatureSpan">npm_lazy.</span>cache (opts)](#apidoc.element.npm_lazy.cache.cache)
1.  [function <span class="apidocSignatureSpan">npm_lazy.cache.</span>hash (method, str)](#apidoc.element.npm_lazy.cache.hash)

#### [module npm_lazy.cache.prototype](#apidoc.module.npm_lazy.cache.prototype)
1.  [function <span class="apidocSignatureSpan">npm_lazy.cache.prototype.</span>clear ()](#apidoc.element.npm_lazy.cache.prototype.clear)
1.  [function <span class="apidocSignatureSpan">npm_lazy.cache.prototype.</span>complete (itemHash, taskHash, cacheFilePath, etag)](#apidoc.element.npm_lazy.cache.prototype.complete)
1.  [function <span class="apidocSignatureSpan">npm_lazy.cache.prototype.</span>filename ()](#apidoc.element.npm_lazy.cache.prototype.filename)
1.  [function <span class="apidocSignatureSpan">npm_lazy.cache.prototype.</span>hash (method, str)](#apidoc.element.npm_lazy.cache.prototype.hash)
1.  [function <span class="apidocSignatureSpan">npm_lazy.cache.prototype.</span>junk (itemHash)](#apidoc.element.npm_lazy.cache.prototype.junk)
1.  [function <span class="apidocSignatureSpan">npm_lazy.cache.prototype.</span>lookup (itemHash, taskHash)](#apidoc.element.npm_lazy.cache.prototype.lookup)
1.  [function <span class="apidocSignatureSpan">npm_lazy.cache.prototype.</span>save ()](#apidoc.element.npm_lazy.cache.prototype.save)

#### [module npm_lazy.etag](#apidoc.module.npm_lazy.etag)
1.  [function <span class="apidocSignatureSpan">npm_lazy.etag.</span>handle304 (req, res, etag)](#apidoc.element.npm_lazy.etag.handle304)

#### [module npm_lazy.lifecycle](#apidoc.module.npm_lazy.lifecycle)
1.  [function <span class="apidocSignatureSpan">npm_lazy.</span>lifecycle ()](#apidoc.element.npm_lazy.lifecycle.lifecycle)

#### [module npm_lazy.lifecycle.prototype](#apidoc.module.npm_lazy.lifecycle.prototype)
1.  [function <span class="apidocSignatureSpan">npm_lazy.lifecycle.prototype.</span>block (resource)](#apidoc.element.npm_lazy.lifecycle.prototype.block)
1.  [function <span class="apidocSignatureSpan">npm_lazy.lifecycle.prototype.</span>emit (ev)](#apidoc.element.npm_lazy.lifecycle.prototype.emit)
1.  [function <span class="apidocSignatureSpan">npm_lazy.lifecycle.prototype.</span>isBlocking (resource)](#apidoc.element.npm_lazy.lifecycle.prototype.isBlocking)
1.  [function <span class="apidocSignatureSpan">npm_lazy.lifecycle.prototype.</span>listeners (ev)](#apidoc.element.npm_lazy.lifecycle.prototype.listeners)
1.  [function <span class="apidocSignatureSpan">npm_lazy.lifecycle.prototype.</span>on (ev, cb)](#apidoc.element.npm_lazy.lifecycle.prototype.on)
1.  [function <span class="apidocSignatureSpan">npm_lazy.lifecycle.prototype.</span>onRelease (resource, callback)](#apidoc.element.npm_lazy.lifecycle.prototype.onRelease)
1.  [function <span class="apidocSignatureSpan">npm_lazy.lifecycle.prototype.</span>once (ev, cb, when)](#apidoc.element.npm_lazy.lifecycle.prototype.once)
1.  [function <span class="apidocSignatureSpan">npm_lazy.lifecycle.prototype.</span>release (resource)](#apidoc.element.npm_lazy.lifecycle.prototype.release)
1.  [function <span class="apidocSignatureSpan">npm_lazy.lifecycle.prototype.</span>removeAllListeners (ev)](#apidoc.element.npm_lazy.lifecycle.prototype.removeAllListeners)
1.  [function <span class="apidocSignatureSpan">npm_lazy.lifecycle.prototype.</span>removeListener (ev, cb)](#apidoc.element.npm_lazy.lifecycle.prototype.removeListener)
1.  [function <span class="apidocSignatureSpan">npm_lazy.lifecycle.prototype.</span>when (ev, cb)](#apidoc.element.npm_lazy.lifecycle.prototype.when)

#### [module npm_lazy.package](#apidoc.module.npm_lazy.package)
1.  [function <span class="apidocSignatureSpan">npm_lazy.</span>package ()](#apidoc.element.npm_lazy.package.package)
1.  [function <span class="apidocSignatureSpan">npm_lazy.package.</span>_rewriteLocation (meta)](#apidoc.element.npm_lazy.package._rewriteLocation)
1.  [function <span class="apidocSignatureSpan">npm_lazy.package.</span>configure (opts)](#apidoc.element.npm_lazy.package.configure)
1.  [function <span class="apidocSignatureSpan">npm_lazy.package.</span>getIndex (pname, auth, onDone)](#apidoc.element.npm_lazy.package.getIndex)
1.  [function <span class="apidocSignatureSpan">npm_lazy.package.</span>getVersion (pname, version, onDone)](#apidoc.element.npm_lazy.package.getVersion)
1.  [function <span class="apidocSignatureSpan">npm_lazy.package.</span>proxy (req, res, message)](#apidoc.element.npm_lazy.package.proxy)

#### [module npm_lazy.resource](#apidoc.module.npm_lazy.resource)
1.  [function <span class="apidocSignatureSpan">npm_lazy.</span>resource (url, auth)](#apidoc.element.npm_lazy.resource.resource)
1.  [function <span class="apidocSignatureSpan">npm_lazy.resource.</span>configure (opts)](#apidoc.element.npm_lazy.resource.configure)
1.  [function <span class="apidocSignatureSpan">npm_lazy.resource.</span>get (url, auth)](#apidoc.element.npm_lazy.resource.get)
1.  [function <span class="apidocSignatureSpan">npm_lazy.resource.</span>removeFile (filepath)](#apidoc.element.npm_lazy.resource.removeFile)

#### [module npm_lazy.resource.prototype](#apidoc.module.npm_lazy.resource.prototype)
1.  [function <span class="apidocSignatureSpan">npm_lazy.resource.prototype.</span>_afterFetch (err, readableStream)](#apidoc.element.npm_lazy.resource.prototype._afterFetch)
1.  [function <span class="apidocSignatureSpan">npm_lazy.resource.prototype.</span>_fetchTask (onDone)](#apidoc.element.npm_lazy.resource.prototype._fetchTask)
1.  [function <span class="apidocSignatureSpan">npm_lazy.resource.prototype.</span>emit (ev)](#apidoc.element.npm_lazy.resource.prototype.emit)
1.  [function <span class="apidocSignatureSpan">npm_lazy.resource.prototype.</span>exists ()](#apidoc.element.npm_lazy.resource.prototype.exists)
1.  [function <span class="apidocSignatureSpan">npm_lazy.resource.prototype.</span>getPackageName ()](#apidoc.element.npm_lazy.resource.prototype.getPackageName)
1.  [function <span class="apidocSignatureSpan">npm_lazy.resource.prototype.</span>getReadablePath (onDone)](#apidoc.element.npm_lazy.resource.prototype.getReadablePath)
1.  [function <span class="apidocSignatureSpan">npm_lazy.resource.prototype.</span>isUpToDate ()](#apidoc.element.npm_lazy.resource.prototype.isUpToDate)
1.  [function <span class="apidocSignatureSpan">npm_lazy.resource.prototype.</span>listeners (ev)](#apidoc.element.npm_lazy.resource.prototype.listeners)
1.  [function <span class="apidocSignatureSpan">npm_lazy.resource.prototype.</span>lookup ()](#apidoc.element.npm_lazy.resource.prototype.lookup)
1.  [function <span class="apidocSignatureSpan">npm_lazy.resource.prototype.</span>on (ev, cb)](#apidoc.element.npm_lazy.resource.prototype.on)
1.  [function <span class="apidocSignatureSpan">npm_lazy.resource.prototype.</span>once (ev, cb, when)](#apidoc.element.npm_lazy.resource.prototype.once)
1.  [function <span class="apidocSignatureSpan">npm_lazy.resource.prototype.</span>removeAllListeners (ev)](#apidoc.element.npm_lazy.resource.prototype.removeAllListeners)
1.  [function <span class="apidocSignatureSpan">npm_lazy.resource.prototype.</span>removeListener (ev, cb)](#apidoc.element.npm_lazy.resource.prototype.removeListener)
1.  [function <span class="apidocSignatureSpan">npm_lazy.resource.prototype.</span>retry ()](#apidoc.element.npm_lazy.resource.prototype.retry)
1.  [function <span class="apidocSignatureSpan">npm_lazy.resource.prototype.</span>when (ev, cb)](#apidoc.element.npm_lazy.resource.prototype.when)

#### [module npm_lazy.verify](#apidoc.module.npm_lazy.verify)
1.  [function <span class="apidocSignatureSpan">npm_lazy.verify.</span>check (filename, cb)](#apidoc.element.npm_lazy.verify.check)
1.  [function <span class="apidocSignatureSpan">npm_lazy.verify.</span>getSha (tarBaseName, json)](#apidoc.element.npm_lazy.verify.getSha)



# <a name="apidoc.module.npm_lazy"></a>[module npm_lazy](#apidoc.module.npm_lazy)

#### <a name="apidoc.element.npm_lazy.cache"></a>[function <span class="apidocSignatureSpan">npm_lazy.</span>cache (opts)](#apidoc.element.npm_lazy.cache)
- description and source-code
```javascript
function Cache(opts) {
  this.opts = opts;
  this.data = null;
  this.path = opts.path;

  // can either set the path, or set 'appHash'
  if (opts.path) {
    this.metaPath = opts.path + '/meta.json';
    this.data = (fs.existsSync(this.metaPath) ? require(this.metaPath) : {});

    // need to do this early on, since if the path is missing,
    // writes to the cache dir will fail
    if (!fs.existsSync(this.opts.path)) {
      mkdirp.sync(this.opts.path);
    }
  } else {
    throw new Error('Must set the cache path');
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npm_lazy.lifecycle"></a>[function <span class="apidocSignatureSpan">npm_lazy.</span>lifecycle ()](#apidoc.element.npm_lazy.lifecycle)
- description and source-code
```javascript
function Lifecycle() {
  this.blocked = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npm_lazy.package"></a>[function <span class="apidocSignatureSpan">npm_lazy.</span>package ()](#apidoc.element.npm_lazy.package)
- description and source-code
```javascript
function Package() { }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npm_lazy.resource"></a>[function <span class="apidocSignatureSpan">npm_lazy.</span>resource (url, auth)](#apidoc.element.npm_lazy.resource)
- description and source-code
```javascript
function Resource(url, auth) {
  this.url = url;
  this.auth = auth;

  this.retries = 0;

  var parts = coreUrl.parse(url);
  if (path.extname(parts.pathname) == '.tgz') {
    this.type = 'tar';
    this.basename = path.basename(parts.pathname);
  } else {
    this.type = 'index';
  }

  this.err = null;
  this.fetchTimer = null;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.npm_lazy.api"></a>[module npm_lazy.api](#apidoc.module.npm_lazy.api)

#### <a name="apidoc.element.npm_lazy.api.configure"></a>[function <span class="apidocSignatureSpan">npm_lazy.api.</span>configure (config)](#apidoc.element.npm_lazy.api.configure)
- description and source-code
```javascript
configure = function (config) {
  if (typeof config.remoteUrl !== 'undefined') {
    remoteUrl = config.remoteUrl;
  }
  if (typeof config.logger !== 'undefined') {
    logger = config.logger;
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.npm_lazy.cache"></a>[module npm_lazy.cache](#apidoc.module.npm_lazy.cache)

#### <a name="apidoc.element.npm_lazy.cache.cache"></a>[function <span class="apidocSignatureSpan">npm_lazy.</span>cache (opts)](#apidoc.element.npm_lazy.cache.cache)
- description and source-code
```javascript
function Cache(opts) {
  this.opts = opts;
  this.data = null;
  this.path = opts.path;

  // can either set the path, or set 'appHash'
  if (opts.path) {
    this.metaPath = opts.path + '/meta.json';
    this.data = (fs.existsSync(this.metaPath) ? require(this.metaPath) : {});

    // need to do this early on, since if the path is missing,
    // writes to the cache dir will fail
    if (!fs.existsSync(this.opts.path)) {
      mkdirp.sync(this.opts.path);
    }
  } else {
    throw new Error('Must set the cache path');
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npm_lazy.cache.hash"></a>[function <span class="apidocSignatureSpan">npm_lazy.cache.</span>hash (method, str)](#apidoc.element.npm_lazy.cache.hash)
- description and source-code
```javascript
hash = function (method, str) {
  // method is optional, defaults to md5
  if (arguments.length === 1) {
    str = method;
    method = 'md5';
  }
  return crypto.createHash(method).update(str).digest('hex');
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.npm_lazy.cache.prototype"></a>[module npm_lazy.cache.prototype](#apidoc.module.npm_lazy.cache.prototype)

#### <a name="apidoc.element.npm_lazy.cache.prototype.clear"></a>[function <span class="apidocSignatureSpan">npm_lazy.cache.prototype.</span>clear ()](#apidoc.element.npm_lazy.cache.prototype.clear)
- description and source-code
```javascript
clear = function () {
  var self = this;
  // delete any lingering files
  Object.keys(this.data).forEach(function(inputFilePath) {
    self.junk(inputFilePath);
  });
  this.data = {};
  this.save();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npm_lazy.cache.prototype.complete"></a>[function <span class="apidocSignatureSpan">npm_lazy.cache.prototype.</span>complete (itemHash, taskHash, cacheFilePath, etag)](#apidoc.element.npm_lazy.cache.prototype.complete)
- description and source-code
```javascript
complete = function (itemHash, taskHash, cacheFilePath, etag) {
  if (arguments.length < 3) {
    throw new Error('Invalid call to Cache.complete()');
  }

  if (!this.data[itemHash]) {
    this.data[itemHash] = { taskResults: {} };
  }
  if (!this.data[itemHash].taskResults) {
    this.data[itemHash].taskResults = {};
  }

  // make pluggable: update the cache with the INPUT item stats

  this.data[itemHash].taskResults[taskHash] = { path: cacheFilePath, etag: etag };
  // console.log('Complete', itemHash, taskHash);
  this.save();
}
```
- example usage
```shell
...
  );
} while (fs.existsSync(cacheName));
return cacheName;
};

Cache.prototype.complete = function(itemHash, taskHash, cacheFilePath, etag) {
if (arguments.length < 3) {
  throw new Error('Invalid call to Cache.complete()');
}

if (!this.data[itemHash]) {
  this.data[itemHash] = { taskResults: {} };
}
if (!this.data[itemHash].taskResults) {
  this.data[itemHash].taskResults = {};
...
```

#### <a name="apidoc.element.npm_lazy.cache.prototype.filename"></a>[function <span class="apidocSignatureSpan">npm_lazy.cache.prototype.</span>filename ()](#apidoc.element.npm_lazy.cache.prototype.filename)
- description and source-code
```javascript
filename = function () {
  var cacheName;
  // generate a new file name
  do {
    cacheName = path.normalize(
      this.path + '/' + Math.random().toString(36).substring(2)
    );
  } while (fs.existsSync(cacheName));
  return cacheName;
}
```
- example usage
```shell
...

// resource fetch OK:
if (readableStream.headers) {
  self.etag = readableStream.headers.etag;
}

// write to disk
var cachename = Cache.filename(),
    out = fs.createWriteStream(cachename, {flags: 'w'});

// 0.8.x: "close"
// 0.10.x: "finish"
var emittedDone = false;
function emitDone() {
  if (!emittedDone) {
...
```

#### <a name="apidoc.element.npm_lazy.cache.prototype.hash"></a>[function <span class="apidocSignatureSpan">npm_lazy.cache.prototype.</span>hash (method, str)](#apidoc.element.npm_lazy.cache.prototype.hash)
- description and source-code
```javascript
hash = function (method, str) {
  // method is optional, defaults to md5
  if (arguments.length === 1) {
    str = method;
    method = 'md5';
  }
  return crypto.createHash(method).update(str).digest('hex');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npm_lazy.cache.prototype.junk"></a>[function <span class="apidocSignatureSpan">npm_lazy.cache.prototype.</span>junk (itemHash)](#apidoc.element.npm_lazy.cache.prototype.junk)
- description and source-code
```javascript
junk = function (itemHash) {
  var self = this;
  if (!this.data[itemHash]) {
    return; // nothing to do
  }
  // for each .taskResults
  Object.keys(this.data[itemHash].taskResults).forEach(function(taskHash) {
    // .taskResults[hash] = { path: '...' }
    var cacheFile = self.data[itemHash].taskResults[taskHash].path;
    if (fs.existsSync(cacheFile)) {
      fs.unlink(cacheFile);
    }
  });
  delete this.data[itemHash];
}
```
- example usage
```shell
...
delete this.data[itemHash];
};

Cache.prototype.clear = function() {
var self = this;
// delete any lingering files
Object.keys(this.data).forEach(function(inputFilePath) {
  self.junk(inputFilePath);
});
this.data = {};
this.save();
};

Cache.prototype.filename = function() {
var cacheName;
...
```

#### <a name="apidoc.element.npm_lazy.cache.prototype.lookup"></a>[function <span class="apidocSignatureSpan">npm_lazy.cache.prototype.</span>lookup (itemHash, taskHash)](#apidoc.element.npm_lazy.cache.prototype.lookup)
- description and source-code
```javascript
lookup = function (itemHash, taskHash) {
  // console.log('Lookup', itemHash, taskHash, this.data[itemHash]);
  var cacheMeta = this.data[itemHash];
  // {
  //   itemHash: {
  //     stat: (expected stat meta)
  //     md5: (expected hash meta)
  //
  //     taskResults: {
  //       taskHash: {
  //         path: (path in cache for this task)
  //       }
  //     }
  //   }
  // }

  // make pluggable: verification that the looked up item is OK

  // now, search for a cached file that corresponds to the current task hash
  if (!cacheMeta ||
      !cacheMeta.taskResults ||
      !cacheMeta.taskResults[taskHash] ||
      !cacheMeta.taskResults[taskHash].path) {
    return false;
  }
  return cacheMeta.taskResults[taskHash];
}
```
- example usage
```shell
...
  }
  if (typeof opts.proxy !== 'undefined') {
    proxy = opts.proxy;
  }
};

Resource.prototype.exists = function() {
  // logger.log('exists', this.url, 'GET', Cache.lookup(this.url, 'GET'));
  return this.lookup().path;
};

Resource.prototype.lookup = function() {
  return Cache.lookup(this.url, 'GET');
};
...
```

#### <a name="apidoc.element.npm_lazy.cache.prototype.save"></a>[function <span class="apidocSignatureSpan">npm_lazy.cache.prototype.</span>save ()](#apidoc.element.npm_lazy.cache.prototype.save)
- description and source-code
```javascript
save = function () {
  // just in case
  if (!fs.existsSync(this.opts.path)) {
    mkdirp.sync(this.opts.path);
  }
  fs.writeFileSync(this.metaPath, JSON.stringify(this.data, null, 2));
}
```
- example usage
```shell
...
Cache.prototype.clear = function() {
var self = this;
// delete any lingering files
Object.keys(this.data).forEach(function(inputFilePath) {
  self.junk(inputFilePath);
});
this.data = {};
this.save();
};

Cache.prototype.filename = function() {
var cacheName;
// generate a new file name
do {
  cacheName = path.normalize(
...
```



# <a name="apidoc.module.npm_lazy.etag"></a>[module npm_lazy.etag](#apidoc.module.npm_lazy.etag)

#### <a name="apidoc.element.npm_lazy.etag.handle304"></a>[function <span class="apidocSignatureSpan">npm_lazy.etag.</span>handle304 (req, res, etag)](#apidoc.element.npm_lazy.etag.handle304)
- description and source-code
```javascript
handle304 = function (req, res, etag) {
  if (etag) {
    if (req.headers['if-none-match'] === etag) {
      res.statusCode = 304;
      res.end();
      return;
    }
    res.setHeader('ETag', etag);
  }
}
```
- example usage
```shell
...
      if (err.content) {
        res.write(err.content);
      }
      res.end();
      return;
    }

    if (ETag.handle304(req, res, etag)) {
      return;
    }

    res.end(JSON.stringify(fullpath));
  });
});
...
```



# <a name="apidoc.module.npm_lazy.lifecycle"></a>[module npm_lazy.lifecycle](#apidoc.module.npm_lazy.lifecycle)

#### <a name="apidoc.element.npm_lazy.lifecycle.lifecycle"></a>[function <span class="apidocSignatureSpan">npm_lazy.</span>lifecycle ()](#apidoc.element.npm_lazy.lifecycle.lifecycle)
- description and source-code
```javascript
function Lifecycle() {
  this.blocked = {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.npm_lazy.lifecycle.prototype"></a>[module npm_lazy.lifecycle.prototype](#apidoc.module.npm_lazy.lifecycle.prototype)

#### <a name="apidoc.element.npm_lazy.lifecycle.prototype.block"></a>[function <span class="apidocSignatureSpan">npm_lazy.lifecycle.prototype.</span>block (resource)](#apidoc.element.npm_lazy.lifecycle.prototype.block)
- description and source-code
```javascript
block = function (resource) {
  // console.log('Blocking', resource);
  this.blocked[resource] = true;
}
```
- example usage
```shell
...
// are we blocking? => nothing more to do so return
if (guard.isBlocking(self.url)) {
  logger.log('Request is pending, blocking ' + self.url);
  return;
}

// else: queue a get
guard.block(self.url);
this.retries = 0;
this.err = null;
this.retry();
};

Resource.prototype.retry = function() {
var self = this;
...
```

#### <a name="apidoc.element.npm_lazy.lifecycle.prototype.emit"></a>[function <span class="apidocSignatureSpan">npm_lazy.lifecycle.prototype.</span>emit (ev)](#apidoc.element.npm_lazy.lifecycle.prototype.emit)
- description and source-code
```javascript
emit = function (ev) {
  this._events || (this._events = {});
  var args = Array.prototype.slice.call(arguments, 1), i, e = this._events[ev] || [];
  for(i = e.length-1; i >= 0 && e[i]; i--){
    e[i].apply(this, args);
  }
  return this;
}
```
- example usage
```shell
...
};

Lifecycle.prototype.release = function(resource) {
  // console.log('Releasing', resource);
  if (this.isBlocking(resource)) {
    delete this.blocked[resource];
    // console.log('Released: '+resource+' - run callbacks');
    this.emit('resource', resource);
  }
};

Lifecycle.prototype.isBlocking = function(resource) {
  return this.blocked.hasOwnProperty(resource);
};
...
```

#### <a name="apidoc.element.npm_lazy.lifecycle.prototype.isBlocking"></a>[function <span class="apidocSignatureSpan">npm_lazy.lifecycle.prototype.</span>isBlocking (resource)](#apidoc.element.npm_lazy.lifecycle.prototype.isBlocking)
- description and source-code
```javascript
isBlocking = function (resource) {
  return this.blocked.hasOwnProperty(resource);
}
```
- example usage
```shell
...
Lifecycle.prototype.block = function(resource) {
  // console.log('Blocking', resource);
  this.blocked[resource] = true;
};

Lifecycle.prototype.release = function(resource) {
  // console.log('Releasing', resource);
  if (this.isBlocking(resource)) {
    delete this.blocked[resource];
    // console.log('Released: '+resource+' - run callbacks');
    this.emit('resource', resource);
  }
};

Lifecycle.prototype.isBlocking = function(resource) {
...
```

#### <a name="apidoc.element.npm_lazy.lifecycle.prototype.listeners"></a>[function <span class="apidocSignatureSpan">npm_lazy.lifecycle.prototype.</span>listeners (ev)](#apidoc.element.npm_lazy.lifecycle.prototype.listeners)
- description and source-code
```javascript
listeners = function (ev) {
  return (this._events ? this._events[ev] || [] : []);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npm_lazy.lifecycle.prototype.on"></a>[function <span class="apidocSignatureSpan">npm_lazy.lifecycle.prototype.</span>on (ev, cb)](#apidoc.element.npm_lazy.lifecycle.prototype.on)
- description and source-code
```javascript
on = function (ev, cb) {
  this._events || (this._events = {});
  var e = this._events;
  (e[ev] || (e[ev] = [])).push(cb);
  return this;
}
```
- example usage
```shell
...
};

Package.getIndex = function(pname, auth, onDone) {
// package index
var uri = remoteUrl + pname,
    r = Resource.get(uri, auth);

r.on('fetch-error', function(err, current, max) {
  logger.log('Fetch failed (' + current + '/' + max + '): ' + uri, err);
});

r.on('fetch-cached', function() {
  logger.log('[OK] Reusing cached result for ' + uri);
});
...
```

#### <a name="apidoc.element.npm_lazy.lifecycle.prototype.onRelease"></a>[function <span class="apidocSignatureSpan">npm_lazy.lifecycle.prototype.</span>onRelease (resource, callback)](#apidoc.element.npm_lazy.lifecycle.prototype.onRelease)
- description and source-code
```javascript
onRelease = function (resource, callback) {
  // console.log('Blocked: '+resource+' - setting callback for release');
  this.when('resource', function(name) {
    var isMatch = (name == resource);
    if (isMatch) {
      callback();
    }
    return isMatch;
  });
}
```
- example usage
```shell
...
    });
  }
}

var removeAtEnd = self.exists();

// queue the callback
guard.onRelease(this.url, function() {
  // attempt to remove the old file at the end
  // but do not do this if we fail and decide to reuse an old index
  if (self.exists() && removeAtEnd && removeAtEnd != self.exists()) {
    Resource.removeFile(removeAtEnd);
  }
  if (self.err && !self.exists()) {
    return onDone(self.err, null, null);
...
```

#### <a name="apidoc.element.npm_lazy.lifecycle.prototype.once"></a>[function <span class="apidocSignatureSpan">npm_lazy.lifecycle.prototype.</span>once (ev, cb, when)](#apidoc.element.npm_lazy.lifecycle.prototype.once)
- description and source-code
```javascript
once = function (ev, cb, when) {
  if(!cb) return this;
  function c() {
    if(!when) this.removeListener(ev, c);
    if(cb.apply(this, arguments) && when) this.removeListener(ev, c);
  }
  c.cb = cb;
  this.on(ev, c);
  return this;
}
```
- example usage
```shell
...
  });
  // write statuscode
  res.writeHead(pres.statusCode);
  // write response
  pres.pipe(res);
});

req.pipe(outgoing).once('error', function(e) {
  logger.log('Ignoring query error (not cached):', e);
  res.statusCode = 500;
  res.end('{}');
});

// logger.log(req.headers);
// req.pipe(process.stdout);
...
```

#### <a name="apidoc.element.npm_lazy.lifecycle.prototype.release"></a>[function <span class="apidocSignatureSpan">npm_lazy.lifecycle.prototype.</span>release (resource)](#apidoc.element.npm_lazy.lifecycle.prototype.release)
- description and source-code
```javascript
release = function (resource) {
  // console.log('Releasing', resource);
  if (this.isBlocking(resource)) {
    delete this.blocked[resource];
    // console.log('Released: '+resource+' - run callbacks');
    this.emit('resource', resource);
  }
}
```
- example usage
```shell
...
  if (self.retries > maxRetries || (self.err && self.err.statusCode === 404)) {
// if the second fetch fails, and we're fetching an index,
// and we have (any) cached version then use that
// logger.log(self.retries, self.type, self.exists());
if (self.type == 'index' && self.exists()) {
  self.emit('fetch-cached');
  Cache.save();
  return guard.release(self.url);
}

// for non-index files, and index files that we don't have,
// if we exhaust the number of retries then 500
// did we exceed the max retries? => throw
if (!self.err) {
  self.err = new Error();
...
```

#### <a name="apidoc.element.npm_lazy.lifecycle.prototype.removeAllListeners"></a>[function <span class="apidocSignatureSpan">npm_lazy.lifecycle.prototype.</span>removeAllListeners (ev)](#apidoc.element.npm_lazy.lifecycle.prototype.removeAllListeners)
- description and source-code
```javascript
removeAllListeners = function (ev) {
  if(!ev) { this._events = {}; }
  else { this._events[ev] && (this._events[ev] = []); }
}
```
- example usage
```shell
...
  });

  r.getReadablePath(function(err, data, etag) {
    if (err) {
      return onDone(err);
    }

    r.removeAllListeners('fetch-error');
    r.removeAllListeners('fetch-cached');

    return onDone(err, Package._rewriteLocation(JSON.parse(fs.readFileSync(data))), etag);
  });
};

Package.getVersion = function(pname, version, onDone) {
...
```

#### <a name="apidoc.element.npm_lazy.lifecycle.prototype.removeListener"></a>[function <span class="apidocSignatureSpan">npm_lazy.lifecycle.prototype.</span>removeListener (ev, cb)](#apidoc.element.npm_lazy.lifecycle.prototype.removeListener)
- description and source-code
```javascript
removeListener = function (ev, cb) {
  var e = this._events[ev] || [], i;
  for(i = e.length-1; i >= 0 && e[i]; i--){
    if(e[i] === cb || e[i].cb === cb) { e.splice(i, 1); }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npm_lazy.lifecycle.prototype.when"></a>[function <span class="apidocSignatureSpan">npm_lazy.lifecycle.prototype.</span>when (ev, cb)](#apidoc.element.npm_lazy.lifecycle.prototype.when)
- description and source-code
```javascript
when = function (ev, cb) {
  return this.once(ev, cb, true);
}
```
- example usage
```shell
...

Lifecycle.prototype.isBlocking = function(resource) {
  return this.blocked.hasOwnProperty(resource);
};

Lifecycle.prototype.onRelease = function(resource, callback) {
  // console.log('Blocked: '+resource+' - setting callback for release');
  this.when('resource', function(name) {
    var isMatch = (name == resource);
    if (isMatch) {
      callback();
    }
    return isMatch;
  });
};
...
```



# <a name="apidoc.module.npm_lazy.package"></a>[module npm_lazy.package](#apidoc.module.npm_lazy.package)

#### <a name="apidoc.element.npm_lazy.package.package"></a>[function <span class="apidocSignatureSpan">npm_lazy.</span>package ()](#apidoc.element.npm_lazy.package.package)
- description and source-code
```javascript
function Package() { }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npm_lazy.package._rewriteLocation"></a>[function <span class="apidocSignatureSpan">npm_lazy.package.</span>_rewriteLocation (meta)](#apidoc.element.npm_lazy.package._rewriteLocation)
- description and source-code
```javascript
_rewriteLocation = function (meta) {
  if (!meta) {
    return meta;
  }

  if (meta.versions) {
    // if a full index, apply to all versions
    Object.keys(meta.versions).forEach(function(version) {
      meta.versions[version] = Package._rewriteLocation(meta.versions[version]);
    });
  }

  if (meta.dist && meta.dist.tarball) {
    var parts = url.parse(meta.dist.tarball);
    meta.dist.tarball = externalUrl + parts.pathname;
  }
  return meta;
}
```
- example usage
```shell
...
  if (err) {
    return onDone(err);
  }

  r.removeAllListeners('fetch-error');
  r.removeAllListeners('fetch-cached');

  return onDone(err, Package._rewriteLocation(JSON.parse(fs.readFileSync(data))), etag);
});
};

Package.getVersion = function(pname, version, onDone) {
// package index
var uri = remoteUrl + pname,
    r = Resource.get(uri);
...
```

#### <a name="apidoc.element.npm_lazy.package.configure"></a>[function <span class="apidocSignatureSpan">npm_lazy.package.</span>configure (opts)](#apidoc.element.npm_lazy.package.configure)
- description and source-code
```javascript
configure = function (opts) {
  if (typeof opts.externalUrl !== 'undefined') {
    externalUrl = opts.externalUrl;
  }
  if (typeof opts.remoteUrl !== 'undefined') {
    remoteUrl = opts.remoteUrl;
    remoteIsHttps = (url.parse(remoteUrl).protocol == 'https:');
  }
  if (typeof opts.rejectUnauthorized !== 'undefined') {
    rejectUnauthorized = opts.rejectUnauthorized;
  }
  if (typeof opts.logger !== 'undefined') {
    logger = opts.logger;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npm_lazy.package.getIndex"></a>[function <span class="apidocSignatureSpan">npm_lazy.package.</span>getIndex (pname, auth, onDone)](#apidoc.element.npm_lazy.package.getIndex)
- description and source-code
```javascript
getIndex = function (pname, auth, onDone) {
  // package index
  var uri = remoteUrl + pname,
      r = Resource.get(uri, auth);

  r.on('fetch-error', function(err, current, max) {
    logger.log('Fetch failed (' + current + '/' + max + '): ' + uri, err);
  });

  r.on('fetch-cached', function() {
    logger.log('[OK] Reusing cached result for ' + uri);
  });

  r.getReadablePath(function(err, data, etag) {
    if (err) {
      return onDone(err);
    }

    r.removeAllListeners('fetch-error');
    r.removeAllListeners('fetch-cached');

    return onDone(err, Package._rewriteLocation(JSON.parse(fs.readFileSync(data))), etag);
  });
}
```
- example usage
```shell
...
};

// GET /package
api.get(new RegExp('^/([^/]+)$'), function(req, res, match) {
var name = match[1];
var auth = req.headers.authorization;

Package.getIndex(name, auth, function(err, fullpath, etag) {
  if (err) {
    res.statusCode = err.statusCode || 500;
    logger.error('[' + res.statusCode + '] Error: ', err);
    if (err.content) {
      res.write(err.content);
    }
    res.end();
...
```

#### <a name="apidoc.element.npm_lazy.package.getVersion"></a>[function <span class="apidocSignatureSpan">npm_lazy.package.</span>getVersion (pname, version, onDone)](#apidoc.element.npm_lazy.package.getVersion)
- description and source-code
```javascript
getVersion = function (pname, version, onDone) {
  // package index
  var uri = remoteUrl + pname,
      r = Resource.get(uri);

  r.on('fetch-error', function() {
    logger.log('Fetch failed: ' + uri);
  });

  r.on('fetch-cached', function() {
    logger.log('[OK] Reusing cached result for ' + uri);
  });


  r.getReadablePath(function(err, fullpath, etag) {
    if (err) {
      return onDone(err);
    }

    r.removeAllListeners('fetch-error');
    r.removeAllListeners('fetch-cached');

    // according to the NPM source, the version specific JSON is
    // directly from the index document (e.g. just take doc.versions[ver])
    var doc = JSON.parse(fs.readFileSync(fullpath));

    // from NPM: if not a valid version, then treat as a tag.
    if (!(version in doc.versions) && (version in doc['dist-tags'])) {
      version = doc['dist-tags'][version];
    }
    if (doc.versions[version]) {
      return onDone(undefined, Package._rewriteLocation(doc.versions[version]), etag);
    }
    return onDone(new Error('[done] Could not find version', fullpath, version));
  });
}
```
- example usage
```shell
...

// GET /package/version
api.get(new RegExp('^/([^/]+)/([^/]+)$'), function(req, res, match) {
var name = match[1],
    version = match[2],
    self = this;

Package.getVersion(name, version, function(err, fullpath, etag) {
  if (err) {
    res.statusCode = err.statusCode || 500;
    logger.error('[' + res.statusCode + '] Error: ', err);
    if (err.content) {
      res.write(err.content);
    }
    res.end();
...
```

#### <a name="apidoc.element.npm_lazy.package.proxy"></a>[function <span class="apidocSignatureSpan">npm_lazy.package.</span>proxy (req, res, message)](#apidoc.element.npm_lazy.package.proxy)
- description and source-code
```javascript
proxy = function (req, res, message) {
  // sadly, the simple req.pipe(http.request).pipe(res) type approach
  // does not quite work, in particular the method and headers will be wrong

  var parsed = url.parse(remoteUrl),
      opts = {
        host: parsed.host,
        port: (parsed.port !== null) ? parsed.port : (remoteIsHttps ? 443 : 80),
        path: req.url,
        headers: req.headers,
        method: req.method
      };
  opts.headers.host = parsed.host;

  if (!rejectUnauthorized && parsed.protocol == 'https:') {
    opts.rejectUnauthorized = false;
    opts.agent = new https.Agent(opts);
  }

  message = message || 'not cached';
  logger.log('Querying the registry (' + message + '):', remoteUrl + req.url.substr(1));

  var outgoing = (remoteIsHttps ? https : http).request(opts, function(pres) {
    // write headers
    Object.keys(pres.headers).forEach(function(key) {
      res.setHeader(key, pres.headers[key]);
    });
    // write statuscode
    res.writeHead(pres.statusCode);
    // write response
    pres.pipe(res);
  });

  req.pipe(outgoing).once('error', function(e) {
    logger.log('Ignoring query error (not cached):', e);
    res.statusCode = 500;
    res.end('{}');
  });

  // logger.log(req.headers);
  // req.pipe(process.stdout);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.npm_lazy.resource"></a>[module npm_lazy.resource](#apidoc.module.npm_lazy.resource)

#### <a name="apidoc.element.npm_lazy.resource.resource"></a>[function <span class="apidocSignatureSpan">npm_lazy.</span>resource (url, auth)](#apidoc.element.npm_lazy.resource.resource)
- description and source-code
```javascript
function Resource(url, auth) {
  this.url = url;
  this.auth = auth;

  this.retries = 0;

  var parts = coreUrl.parse(url);
  if (path.extname(parts.pathname) == '.tgz') {
    this.type = 'tar';
    this.basename = path.basename(parts.pathname);
  } else {
    this.type = 'index';
  }

  this.err = null;
  this.fetchTimer = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npm_lazy.resource.configure"></a>[function <span class="apidocSignatureSpan">npm_lazy.resource.</span>configure (opts)](#apidoc.element.npm_lazy.resource.configure)
- description and source-code
```javascript
configure = function (opts) {
  if (typeof opts.cache !== 'undefined') {
    Cache = opts.cache;
  }
  if (typeof opts.cacheAge !== 'undefined') {
    cacheAge = opts.cacheAge;
  }
  if (typeof opts.maxRetries !== 'undefined') {
    maxRetries = opts.maxRetries;
  }
  if (typeof opts.timeout !== 'undefined') {
    timeout = opts.timeout;
  }
  if (typeof opts.rejectUnauthorized !== 'undefined') {
    rejectUnauthorized = opts.rejectUnauthorized;
  }
  if (typeof opts.logger !== 'undefined') {
    logger = opts.logger;
  }
  if (typeof opts.proxy !== 'undefined') {
    proxy = opts.proxy;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npm_lazy.resource.get"></a>[function <span class="apidocSignatureSpan">npm_lazy.resource.</span>get (url, auth)](#apidoc.element.npm_lazy.resource.get)
- description and source-code
```javascript
get = function (url, auth) {
  if (!resourceCache[url]) {
    resourceCache[url] = new Resource(url, auth);
  }
  return resourceCache[url];
}
```
- example usage
```shell
...
}
if (typeof config.logger !== 'undefined') {
  logger = config.logger;
}
};

// GET /package
api.get(new RegExp('^/([^/]+)$'), function(req, res, match) {
var name = match[1];
var auth = req.headers.authorization;

Package.getIndex(name, auth, function(err, fullpath, etag) {
  if (err) {
    res.statusCode = err.statusCode || 500;
    logger.error('[' + res.statusCode + '] Error: ', err);
...
```

#### <a name="apidoc.element.npm_lazy.resource.removeFile"></a>[function <span class="apidocSignatureSpan">npm_lazy.resource.</span>removeFile (filepath)](#apidoc.element.npm_lazy.resource.removeFile)
- description and source-code
```javascript
removeFile = function (filepath) {
  if (fs.existsSync(filepath)) {
    try {
      fs.unlinkSync(filepath);
    } catch (e) { }
  }
}
```
- example usage
```shell
...
var removeAtEnd = self.exists();

// queue the callback
guard.onRelease(this.url, function() {
  // attempt to remove the old file at the end
  // but do not do this if we fail and decide to reuse an old index
  if (self.exists() && removeAtEnd && removeAtEnd != self.exists()) {
    Resource.removeFile(removeAtEnd);
  }
  if (self.err && !self.exists()) {
    return onDone(self.err, null, null);
  }
  // return readable path
  onDone(null, self.exists(), self.lookup().etag);
});
...
```



# <a name="apidoc.module.npm_lazy.resource.prototype"></a>[module npm_lazy.resource.prototype](#apidoc.module.npm_lazy.resource.prototype)

#### <a name="apidoc.element.npm_lazy.resource.prototype._afterFetch"></a>[function <span class="apidocSignatureSpan">npm_lazy.resource.prototype.</span>_afterFetch (err, readableStream)](#apidoc.element.npm_lazy.resource.prototype._afterFetch)
- description and source-code
```javascript
_afterFetch = function (err, readableStream) {
  var self = this;

  clearTimeout(self.fetchTimer);
  // queue returned:

  // did the request fail?
  if (err) {
    err.contentStream = readableStream;
    self.emit('fetch-error', err, self.retries, maxRetries);
    // RETRY
    return self.retry();
  }

  // resource fetch not modified:
  if (readableStream.statusCode === 304) {
    // We can rely on the data already in the cache.
    // No more operations required.
    logger.log('[304] ' + self.url);
    lastUpdated[self.url] = new Date();
    guard.release(self.url);
    return;
  }

  // resource fetch not successful:
  if (readableStream.statusCode !== 200) {
    self.err = new Error(readableStream.statusCode + ' getting from upstream: ' + self.url);
    self.err.statusCode = readableStream.statusCode;
    self.err.contentStream = readableStream;
    self.emit('fetch-error-response', self.err, self.retries, maxRetries);
    logger.log('[' + readableStream.statusCode + '] ' + self.url);

    // RETRY
    return self.retry();
  }

  // resource fetch OK:
  if (readableStream.headers) {
    self.etag = readableStream.headers.etag;
  }

  // write to disk
  var cachename = Cache.filename(),
      out = fs.createWriteStream(cachename, {flags: 'w'});

  // 0.8.x: "close"
  // 0.10.x: "finish"
  var emittedDone = false;
  function emitDone() {
    if (!emittedDone) {
      emittedDone = true;

      // now validate it

      if (self.type == 'index') {
        // is this a indexfile?
        try {
          // check that it's JSON => store => release
          JSON.parse(fs.readFileSync(cachename).toString());
        } catch (e) {
          // delete
          Resource.removeFile(cachename);
          // RETRY
          return self.retry();
        }
        // mark as OK, return all pending callback
        Cache.complete(self.url, 'GET', cachename, self.etag);
        // set last updated
        lastUpdated[self.url] = new Date();
        guard.release(self.url);
        return;
      }

      if (self.type == 'tar') {
        // is this a tarfile?
        // read the expected checksum
        var Package = require('./package.js');

        Package.getIndex(self.getPackageName(), self.auth, function(err, data) {
          if (err) {
            self.err = err;
            return guard.release(self.url);
          }

          // logger.log('PACKAGE INDEX', data);

          // check that the checksum matches => store => release
          try {
            var expected = verify.getSha(self.basename, data);
          } catch (error) {
            self.err = error;
            return guard.release(self.url);
          }
          verify.check(cachename, function(err, actual) {
            if (err || actual !== expected) {
              logger.error('SHASUM - ' + self.url +
                ' - expected: ' + expected +
                ', actual: ' + actual);
              logger.error('ERROR: npm SHASUM mismatch for ' + self.basename);
              // delete
              Resource.removeFile(cachename);
              // RETRY
              return self.retry();
            } else {
              // must be OK
              logger.log('[done][SHASUM OK] added to cache',
                self.url, self.basename, cachename);
              // mark as OK, return all pending callback
              Cache.complete(self.url, 'GET', cachename);
              guard.release(self.url);
              return;
            }
          });

        });
      }
    }
  }
  out.once('close', emitDone);
  out.once('finish', emitDone);

  readableStream.pipe(out);
}
```
- example usage
```shell
...
    if (self.err.contentStream) {
      return readToEnd(self.err.contentStream, done);
    }
    return done('{ "error": "Unknown error" }');
  }

  this.fetchTimer = setTimeout(function() {
    self._afterFetch(new Error('Request timed out (' + timeout + 'ms)'));
  }, timeout);

  this._fetchTask(function(err, readableStream) {
    self._afterFetch(err, readableStream);
  });
};
...
```

#### <a name="apidoc.element.npm_lazy.resource.prototype._fetchTask"></a>[function <span class="apidocSignatureSpan">npm_lazy.resource.prototype.</span>_fetchTask (onDone)](#apidoc.element.npm_lazy.resource.prototype._fetchTask)
- description and source-code
```javascript
_fetchTask = function (onDone) {
  var self = this;
  var opts = {
        url: coreUrl.parse(this.url),
        method: 'GET',
        headers: {}
      },
      req,
      isHttps = (opts.url.protocol == 'https:'),
      proxyConfig = proxy[(isHttps ? 'https' : 'http')];

  if (proxyConfig && proxyConfig.hostname) {
      opts.proxy = proxyConfig;
  }

  if (!rejectUnauthorized && isHttps) {
    opts.strictSSL = false;
  }

  if (self.lookup() && self.lookup().etag) {
    opts.headers['if-none-match'] = self.lookup().etag;
  }

  if (self.auth) {
    opts.headers['authorization'] = self.auth;
  }

  logger.log('[GET] ' + this.url);

  req = request.get(opts);
  req.on('error', function(err) {
    onDone(err);
  });

  req.on('response', function(res) {
    onDone(null, res);
  });
}
```
- example usage
```shell
...
  return done('{ "error": "Unknown error" }');
}

this.fetchTimer = setTimeout(function() {
  self._afterFetch(new Error('Request timed out (' + timeout + 'ms)'));
}, timeout);

this._fetchTask(function(err, readableStream) {
  self._afterFetch(err, readableStream);
});
};

Resource.prototype._afterFetch = function(err, readableStream) {
var self = this;
...
```

#### <a name="apidoc.element.npm_lazy.resource.prototype.emit"></a>[function <span class="apidocSignatureSpan">npm_lazy.resource.prototype.</span>emit (ev)](#apidoc.element.npm_lazy.resource.prototype.emit)
- description and source-code
```javascript
emit = function (ev) {
  this._events || (this._events = {});
  var args = Array.prototype.slice.call(arguments, 1), i, e = this._events[ev] || [];
  for(i = e.length-1; i >= 0 && e[i]; i--){
    e[i].apply(this, args);
  }
  return this;
}
```
- example usage
```shell
...
};

Lifecycle.prototype.release = function(resource) {
  // console.log('Releasing', resource);
  if (this.isBlocking(resource)) {
    delete this.blocked[resource];
    // console.log('Released: '+resource+' - run callbacks');
    this.emit('resource', resource);
  }
};

Lifecycle.prototype.isBlocking = function(resource) {
  return this.blocked.hasOwnProperty(resource);
};
...
```

#### <a name="apidoc.element.npm_lazy.resource.prototype.exists"></a>[function <span class="apidocSignatureSpan">npm_lazy.resource.prototype.</span>exists ()](#apidoc.element.npm_lazy.resource.prototype.exists)
- description and source-code
```javascript
exists = function () {
  // logger.log('exists', this.url, 'GET', Cache.lookup(this.url, 'GET'));
  return this.lookup().path;
}
```
- example usage
```shell
...
};

// one API
Resource.prototype.getReadablePath = function(onDone) {
var self = this;
// try to find a shortcut
if (!guard.isBlocking(self.url)) {
  if (self.type == 'index' && self.exists()) {
    // is this a index file?
    if (self.isUpToDate()) {
      self.emit('fetch-cached');
      // is the index up to date?
      // yes: return readable stream
      return onDone(null, self.exists(), self.lookup().etag);
    }
...
```

#### <a name="apidoc.element.npm_lazy.resource.prototype.getPackageName"></a>[function <span class="apidocSignatureSpan">npm_lazy.resource.prototype.</span>getPackageName ()](#apidoc.element.npm_lazy.resource.prototype.getPackageName)
- description and source-code
```javascript
getPackageName = function () {
  var parts = coreUrl.parse(this.url);
  var dirs = path.dirname(parts.pathname).split('/').filter(Boolean);
  if (dirs[0].charAt(0) === '@') {
    // https://github.com/npm/npm/blob/2a5977e0c65b244e92d848fcd56f2f80ba8cdf3b/lib/utils/map-to-registry.js#L16
    return dirs.slice(0, 2).join('%2f');
  }
  return dirs[0];
}
```
- example usage
```shell
...
}

if (self.type == 'tar' && self.exists()) {
  self.emit('fetch-cached');
  // is this a tarfile and is it in the index?
  // yes: check sha1 hash
  var Package = require('./package.js');
  return Package.getIndex(self.getPackageName(), self.auth, function(err, data) {
    if (err) {
      return onDone(err, null, null);
    }
    var expectedHash = verify.getSha(self.basename, data);
    verify.check(self.exists(), function(err, actualHash) {
      if (err) {
        return onDone(err, null, null);
...
```

#### <a name="apidoc.element.npm_lazy.resource.prototype.getReadablePath"></a>[function <span class="apidocSignatureSpan">npm_lazy.resource.prototype.</span>getReadablePath (onDone)](#apidoc.element.npm_lazy.resource.prototype.getReadablePath)
- description and source-code
```javascript
getReadablePath = function (onDone) {
  var self = this;
  // try to find a shortcut
  if (!guard.isBlocking(self.url)) {
    if (self.type == 'index' && self.exists()) {
      // is this a index file?
      if (self.isUpToDate()) {
        self.emit('fetch-cached');
        // is the index up to date?
        // yes: return readable stream
        return onDone(null, self.exists(), self.lookup().etag);
      }
    }

    if (self.type == 'tar' && self.exists()) {
      self.emit('fetch-cached');
      // is this a tarfile and is it in the index?
      // yes: check sha1 hash
      var Package = require('./package.js');
      return Package.getIndex(self.getPackageName(), self.auth, function(err, data) {
        if (err) {
          return onDone(err, null, null);
        }
        var expectedHash = verify.getSha(self.basename, data);
        verify.check(self.exists(), function(err, actualHash) {
          if (err) {
            return onDone(err, null, null);
          }
          if (actualHash === expectedHash) {
            return onDone(null, self.exists(), self.lookup().etag); // return readable stream if file is good
          }

          // otherwise, cache is corrupted somehow, so bust cache and retry
          logger.log('Cached package is corrupt. Refetching ' + self.url);
          Cache.junk(self.url);
          self.getReadablePath(onDone);
        });
      });
    }
  }

  var removeAtEnd = self.exists();

  // queue the callback
  guard.onRelease(this.url, function() {
    // attempt to remove the old file at the end
    // but do not do this if we fail and decide to reuse an old index
    if (self.exists() && removeAtEnd && removeAtEnd != self.exists()) {
      Resource.removeFile(removeAtEnd);
    }
    if (self.err && !self.exists()) {
      return onDone(self.err, null, null);
    }
    // return readable path
    onDone(null, self.exists(), self.lookup().etag);
  });

  // are we blocking? => nothing more to do so return
  if (guard.isBlocking(self.url)) {
    logger.log('Request is pending, blocking ' + self.url);
    return;
  }

  // else: queue a get
  guard.block(self.url);
  this.retries = 0;
  this.err = null;
  this.retry();
}
```
- example usage
```shell
...

function downloadTar(req, res, uri) {
// direct cache access - this is a file get, not a metadata get
logger.log('cache get', uri);
var auth = req.headers.authorization;

Resource.get(uri, auth)
        .getReadablePath(function(err, fullpath, etag) {
          if (err) {
            res.statusCode = err.statusCode || 500;
            logger.error('[' + res.statusCode + '] Error: ', err);
            if (err.content) {
              res.write(err.content);
            }
            res.end();
...
```

#### <a name="apidoc.element.npm_lazy.resource.prototype.isUpToDate"></a>[function <span class="apidocSignatureSpan">npm_lazy.resource.prototype.</span>isUpToDate ()](#apidoc.element.npm_lazy.resource.prototype.isUpToDate)
- description and source-code
```javascript
isUpToDate = function () {
  if (cacheAge < 0) {
    return true;
  }
  var maxAge = new Date() - cacheAge,
      isUpToDate = (lastUpdated[this.url] &&
                    lastUpdated[this.url] > maxAge);
  return isUpToDate;
}
```
- example usage
```shell
...
// one API
Resource.prototype.getReadablePath = function(onDone) {
var self = this;
// try to find a shortcut
if (!guard.isBlocking(self.url)) {
  if (self.type == 'index' && self.exists()) {
    // is this a index file?
    if (self.isUpToDate()) {
      self.emit('fetch-cached');
      // is the index up to date?
      // yes: return readable stream
      return onDone(null, self.exists(), self.lookup().etag);
    }
  }
...
```

#### <a name="apidoc.element.npm_lazy.resource.prototype.listeners"></a>[function <span class="apidocSignatureSpan">npm_lazy.resource.prototype.</span>listeners (ev)](#apidoc.element.npm_lazy.resource.prototype.listeners)
- description and source-code
```javascript
listeners = function (ev) {
  return (this._events ? this._events[ev] || [] : []);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npm_lazy.resource.prototype.lookup"></a>[function <span class="apidocSignatureSpan">npm_lazy.resource.prototype.</span>lookup ()](#apidoc.element.npm_lazy.resource.prototype.lookup)
- description and source-code
```javascript
lookup = function () {
  return Cache.lookup(this.url, 'GET');
}
```
- example usage
```shell
...
  }
  if (typeof opts.proxy !== 'undefined') {
    proxy = opts.proxy;
  }
};

Resource.prototype.exists = function() {
  // logger.log('exists', this.url, 'GET', Cache.lookup(this.url, 'GET'));
  return this.lookup().path;
};

Resource.prototype.lookup = function() {
  return Cache.lookup(this.url, 'GET');
};
...
```

#### <a name="apidoc.element.npm_lazy.resource.prototype.on"></a>[function <span class="apidocSignatureSpan">npm_lazy.resource.prototype.</span>on (ev, cb)](#apidoc.element.npm_lazy.resource.prototype.on)
- description and source-code
```javascript
on = function (ev, cb) {
  this._events || (this._events = {});
  var e = this._events;
  (e[ev] || (e[ev] = [])).push(cb);
  return this;
}
```
- example usage
```shell
...
};

Package.getIndex = function(pname, auth, onDone) {
// package index
var uri = remoteUrl + pname,
    r = Resource.get(uri, auth);

r.on('fetch-error', function(err, current, max) {
  logger.log('Fetch failed (' + current + '/' + max + '): ' + uri, err);
});

r.on('fetch-cached', function() {
  logger.log('[OK] Reusing cached result for ' + uri);
});
...
```

#### <a name="apidoc.element.npm_lazy.resource.prototype.once"></a>[function <span class="apidocSignatureSpan">npm_lazy.resource.prototype.</span>once (ev, cb, when)](#apidoc.element.npm_lazy.resource.prototype.once)
- description and source-code
```javascript
once = function (ev, cb, when) {
  if(!cb) return this;
  function c() {
    if(!when) this.removeListener(ev, c);
    if(cb.apply(this, arguments) && when) this.removeListener(ev, c);
  }
  c.cb = cb;
  this.on(ev, c);
  return this;
}
```
- example usage
```shell
...
  });
  // write statuscode
  res.writeHead(pres.statusCode);
  // write response
  pres.pipe(res);
});

req.pipe(outgoing).once('error', function(e) {
  logger.log('Ignoring query error (not cached):', e);
  res.statusCode = 500;
  res.end('{}');
});

// logger.log(req.headers);
// req.pipe(process.stdout);
...
```

#### <a name="apidoc.element.npm_lazy.resource.prototype.removeAllListeners"></a>[function <span class="apidocSignatureSpan">npm_lazy.resource.prototype.</span>removeAllListeners (ev)](#apidoc.element.npm_lazy.resource.prototype.removeAllListeners)
- description and source-code
```javascript
removeAllListeners = function (ev) {
  if(!ev) { this._events = {}; }
  else { this._events[ev] && (this._events[ev] = []); }
}
```
- example usage
```shell
...
  });

  r.getReadablePath(function(err, data, etag) {
    if (err) {
      return onDone(err);
    }

    r.removeAllListeners('fetch-error');
    r.removeAllListeners('fetch-cached');

    return onDone(err, Package._rewriteLocation(JSON.parse(fs.readFileSync(data))), etag);
  });
};

Package.getVersion = function(pname, version, onDone) {
...
```

#### <a name="apidoc.element.npm_lazy.resource.prototype.removeListener"></a>[function <span class="apidocSignatureSpan">npm_lazy.resource.prototype.</span>removeListener (ev, cb)](#apidoc.element.npm_lazy.resource.prototype.removeListener)
- description and source-code
```javascript
removeListener = function (ev, cb) {
  var e = this._events[ev] || [], i;
  for(i = e.length-1; i >= 0 && e[i]; i--){
    if(e[i] === cb || e[i].cb === cb) { e.splice(i, 1); }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npm_lazy.resource.prototype.retry"></a>[function <span class="apidocSignatureSpan">npm_lazy.resource.prototype.</span>retry ()](#apidoc.element.npm_lazy.resource.prototype.retry)
- description and source-code
```javascript
retry = function () {
  var self = this;
  self.retries++;
  if (self.retries > maxRetries || (self.err && self.err.statusCode === 404)) {
    // if the second fetch fails, and we're fetching an index,
    // and we have (any) cached version then use that
    // logger.log(self.retries, self.type, self.exists());
    if (self.type == 'index' && self.exists()) {
      self.emit('fetch-cached');
      Cache.save();
      return guard.release(self.url);
    }

    // for non-index files, and index files that we don't have,
    // if we exhaust the number of retries then 500
    // did we exceed the max retries? => throw
    if (!self.err) {
      self.err = new Error();
    }
    self.err.message = 'URL is not in the npm_lazy cache, and it cannot be fetched (max retries exhausted): ' + self.url;

    // We need to read the whole stream because we want to potentially
    // respond to multiple clients with the same message.
    // Non-200 responses should be small regardless.
    var readToEnd = function(stream, done) {
      var resp = '';
      stream.on('data', function(content) {
        resp += content;
      });
      stream.on('end', function() {
        return done(resp);
      });
    };

    var done = function(content) {
      self.err.contentStream = null;
      self.err.content = content;
      Cache.save();
      return guard.release(self.url);
    };

    if (self.err.contentStream) {
      return readToEnd(self.err.contentStream, done);
    }
    return done('{ "error": "Unknown error" }');
  }

  this.fetchTimer = setTimeout(function() {
    self._afterFetch(new Error('Request timed out (' + timeout + 'ms)'));
  }, timeout);

  this._fetchTask(function(err, readableStream) {
    self._afterFetch(err, readableStream);
  });
}
```
- example usage
```shell
...
  return;
}

// else: queue a get
guard.block(self.url);
this.retries = 0;
this.err = null;
this.retry();
};

Resource.prototype.retry = function() {
var self = this;
self.retries++;
if (self.retries > maxRetries || (self.err && self.err.statusCode === 404)) {
  // if the second fetch fails, and we're fetching an index,
...
```

#### <a name="apidoc.element.npm_lazy.resource.prototype.when"></a>[function <span class="apidocSignatureSpan">npm_lazy.resource.prototype.</span>when (ev, cb)](#apidoc.element.npm_lazy.resource.prototype.when)
- description and source-code
```javascript
when = function (ev, cb) {
  return this.once(ev, cb, true);
}
```
- example usage
```shell
...

Lifecycle.prototype.isBlocking = function(resource) {
  return this.blocked.hasOwnProperty(resource);
};

Lifecycle.prototype.onRelease = function(resource, callback) {
  // console.log('Blocked: '+resource+' - setting callback for release');
  this.when('resource', function(name) {
    var isMatch = (name == resource);
    if (isMatch) {
      callback();
    }
    return isMatch;
  });
};
...
```



# <a name="apidoc.module.npm_lazy.verify"></a>[module npm_lazy.verify](#apidoc.module.npm_lazy.verify)

#### <a name="apidoc.element.npm_lazy.verify.check"></a>[function <span class="apidocSignatureSpan">npm_lazy.verify.</span>check (filename, cb)](#apidoc.element.npm_lazy.verify.check)
- description and source-code
```javascript
check = function (filename, cb) {
  // from npm:
  var crypto = require('crypto');
  var h = crypto.createHash('sha1'),
      s = fs.createReadStream(filename),
      errState = null;
  s.on('error', function(er) {
    if (errState) return;
    return cb(errState = er);
  }).on('data', function(chunk) {
    if (errState) return;
    h.update(chunk);
  }).on('end', function() {
    if (errState) return;
    var actual = h.digest('hex').toLowerCase().trim();
    cb(null, actual);
  });
}
```
- example usage
```shell
...
// yes: check sha1 hash
var Package = require('./package.js');
return Package.getIndex(self.getPackageName(), self.auth, function(err, data) {
  if (err) {
    return onDone(err, null, null);
  }
  var expectedHash = verify.getSha(self.basename, data);
  verify.check(self.exists(), function(err, actualHash) {
    if (err) {
      return onDone(err, null, null);
    }
    if (actualHash === expectedHash) {
      return onDone(null, self.exists(), self.lookup().etag); // return readable stream if file is good
    }
...
```

#### <a name="apidoc.element.npm_lazy.verify.getSha"></a>[function <span class="apidocSignatureSpan">npm_lazy.verify.</span>getSha (tarBaseName, json)](#apidoc.element.npm_lazy.verify.getSha)
- description and source-code
```javascript
function getSha(tarBaseName, json) {
  var expected;
  if (!json.versions) {
    throw new Error('Package index JSON is in unexpected format!' +
      ' A '.versions' keys is required ' + JSON.stringify(json));
  }

  // search 'versions.nnn.dist.tarball' for the right tarball
  Object.keys(json.versions).forEach(function(version) {
    var item = json.versions[version];
    if (path.basename(item.dist.tarball) == tarBaseName) {
      expected = item.dist.shasum;
    }
  });
  return expected;
}
```
- example usage
```shell
...
// is this a tarfile and is it in the index?
// yes: check sha1 hash
var Package = require('./package.js');
return Package.getIndex(self.getPackageName(), self.auth, function(err, data) {
  if (err) {
    return onDone(err, null, null);
  }
  var expectedHash = verify.getSha(self.basename, data);
  verify.check(self.exists(), function(err, actualHash) {
    if (err) {
      return onDone(err, null, null);
    }
    if (actualHash === expectedHash) {
      return onDone(null, self.exists(), self.lookup().etag); // return readable stream if file is good
    }
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
