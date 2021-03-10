# gulp-angular-templates

This plugins allows you to bundle templates directly in your application using the ```$templateCache``` service.

Install it with ```npm install https://github.com/joshuapack/gulp-angular-templates```.

## Usage

```javascript
var angularTemplates = require('gulp-angular-templates');

gulp.task('html', function () {
    return gulp.src('app/partials/**/*.html')
        .pipe(angularTemplates())
        .pipe(gulp.dest('./build/'));
});
```

## API

### angularTemplates(options)

#### options.basePath
Type: `String`

The path that should be prefixed to the path that was specified using ```gulp.src```.

#### options.module
Type: `String`

The name of the module that will be used.

#### options.standalone
Type `Boolean`

Indicate whether the module name that was specified using ```options.module``` is intended to be standalone.