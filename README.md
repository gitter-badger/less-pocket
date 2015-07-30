# LESS CSS For Busy People

## Definition
Dynamic CSS preprocessor

## Purpose
Take `.less` files, compile them to `.css`. LESS files may contain an advanced form of CSS. LESS syntax supports variables, mixins, functions, and others fancy features.

> If you have ever written more than 200 lines of CSS you'll probably like CSS. CSS preprocessor are so handy that once you try one you never come back.

## Compilers
Many compilers exist for many environments.

### 1. Node compiler (the easy way)
- Requires Node: https://github.com/heyallan/node
- Requires NPM (comes with Node)
- Source: https://github.com/less/less.js
```shell
## tech node about less
$ npm install -g less

# Compile less
$ lessc --compress styles.less > styles.css
```

### 2. Gulp (automator) (the developer way)
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
