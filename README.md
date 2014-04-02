# gulp-phantom [![Build Status](https://travis-ci.org/cognitom/gulp-phantom.svg?branch=master)](https://travis-ci.org/cognitom/gulp-phantom)

A [PhantomJS](http://phantomjs.org/) plugin for [gulp](https://github.com/wearefractal/gulp).


## Install

```bash
brew install phantomjs
npm install gulp-phantom --save-dev
```


## Usage

```javascript
var gulp = require("gulp");
var phantom = require("gulp-phantom");

gulp.task('phantom', function(){
  gulp.src("./phantom/*.(js|coffee)")
    .pipe(phantom({
      ext: csv
    }))
    .pipe(gulp.dest("./csv/"));
});
```

or write it in CoffeeScript.

```coffeescript
gulp = requier 'gulp'
phantom = require 'phantom'

gulp.task 'phantom', ->
  gulp.src './phantom/*.(js|coffee)'
  .pipe phantom ext:'.csv'
  .pipe gulp.dest './csv/'
```


## Options

The options are the same as what's supported by `phantomjs`.

- `ext: '.txt'`
- `loadImages: true` Loads all inlined images: 'true' (default) or 'false'