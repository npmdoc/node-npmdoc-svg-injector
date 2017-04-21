# npmdoc-svg-injector

#### api documentation for  [svg-injector (v1.1.3)](https://github.com/iconic/SVGInjector)  [![npm package](https://img.shields.io/npm/v/npmdoc-svg-injector.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-svg-injector) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-svg-injector.svg)](https://travis-ci.org/npmdoc/node-npmdoc-svg-injector)

#### Fast, caching, dynamic inline SVG DOM injection library

[![NPM](https://nodei.co/npm/svg-injector.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/svg-injector)

- [https://npmdoc.github.io/node-npmdoc-svg-injector/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-svg-injector/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-svg-injector/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-svg-injector/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-svg-injector/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-svg-injector/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "svg-injector",
    "description": "Fast, caching, dynamic inline SVG DOM injection library",
    "version": "1.1.3",
    "author": {
        "name": "Iconic",
        "url": "https://useiconic.com/"
    },
    "main": "svg-injector.js",
    "homepage": "https://github.com/iconic/SVGInjector",
    "repository": {
        "type": "git",
        "url": "https://github.com/iconic/SVGInjector"
    },
    "keywords": [
        "SVG",
        "Scalable Vector Graphics",
        "SVG injector",
        "images",
        "img",
        "html",
        "DOM"
    ],
    "license": "MIT",
    "devDependencies": {
        "jshint": "^2.5.0",
        "uglify-js": "^2.4.13",
        "github-changes": "0.0.11"
    },
    "scripts": {
        "test": "jshint svg-injector.js",
        "build": "uglifyjs ./svg-injector.js --stats --compress --mangle --comments --output ./svg-injector.min.js --source-map svg-injector.map.js && mv -f svg-injector.{map,min}.js ./dist",
        "changelog": "github-changes -o iconic -r SVGInjector --use-commit-body",
        "changelog-post": "git add CHANGELOG.md && git commit -m 'Updated CHANGELOG'",
        "release": "for TASK in (test build changelog changelog-post tag); do npm run $TASK; done",
        "tag": "git tag ${npm_package_version} && git push --tags",
        "test-version": "bash -c 'echo $npm_package_version'"
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
