# Compile LESS using Gulp

[← Go back LESS Pocket Guide](https://github.com/heyallan/less-pocket)

## Overview

[Gulp](https://github.com/gulpjs/gulp/blob/master/docs/getting-started.md) is a task automator.

Prerequisites:
- Node (see [Node Pocket Guide](https://github.com/heyallan/node-pocket))
- NPM (comes with Node, see [NPM Pocket Guide](https://github.com/heyallan/npm-pocket))

Pros:
- Fully customizable and automated workflow
- Use `gulpfile.js` to save workflow and options
- Use `gulpfile.js` to share same exact setup accross environments

Cons:
- You may have to take some time to setup a `gulpfile.js` to your taste

## Example

### Install

```shell
$ npm init                          # setup package.json (if you haven't)
$ npm install --global gulp         # install gulp globally (if you haven't)
$ npm install --save-dev gulp       # install gulp locally (will save options to package.json)
$ npm install --save-dev gulp-less  # install compiler locally (will save options to package.json)
```

Many other plugins can be added e.g. concatenate, minify, lint, rename, etc.

### Setup
```javascript
// gulpfile.js
var gulp = require('gulp');
var gulp = require('gulp-less');

gulp.task('less', function() {
  return gulp.src('./src/less/*.less')
    .pipe(less())
    .pipe(gulp.dest('./dist/css/'))
});
```

### Compile
```shell
# run task
$ gulp less
```

### Before compilation

```
project/
├── package.js
├── gulpfile.js
├── src/
│   ├── less/
│   │   ├── styles.less
│── dist/
│   ├── img/
│   ├── js/
│   ├── css/
│   │   ├── <-- empty
```

### After compilation
```
project/
├── package.js
├── gulpfile.js
├── src/
│   ├── less/
│   │   ├── styles.less
├── dist/
│   ├── img/
│   ├── js/
│   ├── css/
│   │   ├── styles.css <-- compiled file
```
Rinse and repeat.
