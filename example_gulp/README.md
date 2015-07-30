# Compile LESS using Gulp

[← Go back to LESS overview](https://github.com/heyallan/less-pocket)

Gulp is a task automator. Install dependencies, setup `gulpfile.js`, and let gulp run tasks on "autopilot".

*Prerequisites:*
- Node: https://github.com/heyallan/node-pocket
- NPM (comes with Node)

*Pros:*
- Fully customizable and automated workflow
- Use `gulpfile.js` to save workflow and options
- Use `gulpfile.js` to share same exact setup accross environments

*Cons:*
- You may have to take some time to setup a `gulpfile.js` to your taste

## Example

### Install dependencies

- Gulp: https://github.com/gulpjs/gulp/blob/master/docs/getting-started.md
- Less plugin: https://github.com/plus3network/gulp-less
- Other plugins can be added like concatenation, minification, etc.

```shell
# install dependencies
$ npm init                          # create package.json
$ npm install --global gulp         # install gulp globally (if you haven't)
$ npm install --save-dev gulp       # install gulp locally (will save options to package.json)
$ npm install --save-dev gulp-less  # install less compiler locally (will save options to package.json)
```

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
# run less task
$ gulp less
```

### Before compilation

```
project/
├── src/
│   ├── less/
│   │   ├── styles.less
│── dist/
│   ├── img/
│   ├── js/
│   ├── css/
│   │   ├── <empty>
```

### After compilation
```
project/
├── src/
│   ├── less/
│   │   ├── styles.less
├── dist/
│   ├── img/
│   ├── js/
│   ├── css/
│   │   ├── styles.min.css
```
Rinse and repeat.
