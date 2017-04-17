# test coverage for  [tesseract.js (v1.0.10)](https://github.com/naptha/tesseract.js)  [![npm package](https://img.shields.io/npm/v/npmtest-tesseract.js.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-tesseract.js) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-tesseract.js.svg)](https://travis-ci.org/npmtest/node-npmtest-tesseract.js)
#### Pure Javascript Multilingual OCR

[![NPM](https://nodei.co/npm/tesseract.js.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/tesseract.js)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-tesseract.js/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-tesseract.js/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-tesseract.js/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-tesseract.js/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-tesseract.js/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-tesseract.js/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-tesseract.js/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-tesseract.js/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-tesseract.js/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-tesseract.js/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-tesseract.js/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-tesseract.js/build/test-report.html](https://npmtest.github.io/node-npmtest-tesseract.js/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-tesseract.js/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-tesseract.js/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-tesseract.js/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-tesseract.js/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-tesseract.js/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-tesseract.js/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-tesseract.js/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-tesseract.js/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": "",
    "browser": {
        "./src/node/index.js": "./src/browser/index.js"
    },
    "bugs": {
        "url": "https://github.com/naptha/tesseract.js/issues"
    },
    "dependencies": {
        "file-type": "^3.8.0",
        "is-url": "^1.2.2",
        "jpeg-js": "^0.2.0",
        "level-js": "^2.2.4",
        "node-fetch": "^1.6.3",
        "object-assign": "^4.1.0",
        "png.js": "^0.2.1",
        "tesseract.js-core": "^1.0.2"
    },
    "description": "Pure Javascript Multilingual OCR",
    "devDependencies": {
        "babel-preset-es2015": "^6.16.0",
        "babelify": "^7.3.0",
        "browserify": "^13.1.0",
        "envify": "^3.4.1",
        "http-server": "^0.9.0",
        "pako": "^1.0.3",
        "watchify": "^3.7.0"
    },
    "directories": {},
    "dist": {
        "shasum": "e11a96ae76147939d9218f88e287fb69414b1e5d",
        "tarball": "https://registry.npmjs.org/tesseract.js/-/tesseract.js-1.0.10.tgz"
    },
    "gitHead": "fc15b0ef43cbf2d8729f8db2ef06a16b2497a16e",
    "homepage": "https://github.com/naptha/tesseract.js",
    "license": "Apache-2.0",
    "main": "src/index.js",
    "maintainers": [
        {
            "name": "antimatter15"
        },
        {
            "name": "bijection"
        }
    ],
    "name": "tesseract.js",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/naptha/tesseract.js.git"
    },
    "scripts": {
        "build": "browserify src/index.js -t [ babelify --presets [ es2015 ] ] -o dist/tesseract.js --standalone Tesseract && browserify src/browser/worker.js -t [ babelify --presets [ es2015 ] ] -o dist/worker.js",
        "release": "npm run build && git commit -am 'new release' && git push && git tag 'jq -r '.version' package.json' && git push origin --tags && npm publish",
        "start": "watchify src/index.js  -t [ envify --NODE_ENV development ] -t [ babelify --presets [ es2015 ] ] -o dist/tesseract.dev.js --standalone Tesseract & watchify src/browser/worker.js  -t [ envify --NODE_ENV development ] -t [ babelify --presets [ es2015 ] ] -o dist/worker.dev.js & http-server -p 7355",
        "test": "echo \"Error: no test specified\" & exit 1"
    },
    "version": "1.0.10"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
