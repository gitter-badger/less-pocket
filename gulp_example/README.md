# Compile LESS using Gulp

[← Go back to LESS overview](https://github.com/heyallan/less)

Gulp is a task automator. Install dependencies, setup `gulpfile.js`, and let gulp run tasks on "autopilot".

*Prerequisites:*
- Node: https://github.com/heyallan/node
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

```shell
# install dependencies
$ npm init                          # create package.js
$ npm install --global gulp         # install gulp automator globally
$ npm install --save-dev gulp       # install gulp automator in project, and save options to package.js
$ npm install --save-dev gulp-less  # install less compiler in project, and save options to package.js
```

### Setup
```javascript
// gulpfile.js
var gulp = require('gulp');
gulp.task('less', function() {
  return gulp.src('./less/**/*.less')
    .pipe(less())
    .pipe(gulp.dest('./public/css'))
});
```

### Compile
```shell
# run gulp file
$ gulp
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
