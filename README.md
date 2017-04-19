# npmdoc-npm_lazy

#### api documentation for  [npm_lazy (v1.14.0)](https://github.com/mixu/npm_lazy#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-npm_lazy.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-npm_lazy) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-npm_lazy.svg)](https://travis-ci.org/npmdoc/node-npmdoc-npm_lazy)

#### Lazy local npm cache server

[![NPM](https://nodei.co/npm/npm_lazy.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/npm_lazy)

- [https://npmdoc.github.io/node-npmdoc-npm_lazy/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-npm_lazy/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-npm_lazy/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-npm_lazy/build/apidoc.html)

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
            "name": "cl0sey"
        },
        {
            "name": "mixu"
        }
    ],
    "name": "npm_lazy",
    "optionalDependencies": {},
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



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
