# LESS CSS For Busy People

## Definition
Dynamic CSS preprocessor

## Purpose
Compile `.less` files into `.css` files. LESS files may contain an advanced form of CSS. LESS syntax supports variables, mixins, functions, and others fancy features.

> If you have ever ventured to wirte more than 200 lines of CSS you'll probably love CSS. CSS preprocessors are so handy. Must of us believe that once you try a CSS preprocessor you never go back.

## Compilers
Many compilers exist for many environments. Let's see a couple of them.

### 1. Node compiler (manual way)
- Requires Node: https://github.com/heyallan/node
- Requires NPM (comes with Node)
- Source: https://github.com/less/less.js
```shell
## install less compiler globally
$ npm install -g less

# compile less
$ lessc --compress styles.less > styles.css
```

### 2. Gulp (automated way)
Gulp is a task automator. You install dependencies, setup `gulpfile.js`, and let gulp run compilation (and any other task) on "autopilot" mode. Gulp uses `gulpfile.js` to remember tasks and preferences.
- *Gulp: https://github.com/gulpjs/gulp/blob/master/docs/getting-started.md*
- *Less plugin: https://github.com/plus3network/gulp-less*

```shell
# install dependencies
$ npm install --global gulp         # install gulp globally
$ npm install --save-dev gulp       # install gulp in project
$ npm install --save-dev gulp-less  # install less support
```
```javascript
// create gulpfile.js
var gulp = require('gulp');
gulp.task('less', function() {
  return gulp.src('./less/**/*.less')
    .pipe(less())
    .pipe(gulp.dest('./public/css'))
});
```
```shell
# run gulp file
$ gulp
```

## Update
```shell

```

## Example
```javascript

```

## Reference
http://lesscss.org/features/
