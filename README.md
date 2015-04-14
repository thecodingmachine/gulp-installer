[Gulp installer for Composer](http://mouf-php.com/packages/mouf/gulp-installer)
=============================

This is an installer that will download [Gulp](http://gulpjs.com/) and install it in your PHP project.

Why?
----

Because Gulp is an extraordinary tool to manage assets (JS, CSS, LESS, SASS, Coffeescript files....) and because 
it is not a common tool in the PHP stack.

Gulp is a NodeJS package. Installation is performed using NPM via the [Koala framework's composer extra assets](https://github.com/koala-framework/composer-extra-assets/) 
plugin. If NodeJS is not available on your computer, it will be downloaded and installed
locally, thanks to [Mouf's node-installer](https://github.com/koala-framework/composer-extra-assets/) package.

Usage
-----

Simply include this package in your `composer.json` requirements:

**composer.json**
```json
{
    "require": {
        "mouf/gulp-installer": "~1.0"
    }
}
```

Then, you can run Gulp using the `vendor/bin/gulp` script (`vendor/bin/gulp.bat` on Windows).

Most of the time, you will want to install a number of plugins with Gulp. Thanks to 
[Koala framework's composer extra assets](https://github.com/koala-framework/composer-extra-assets/), you can add
those dependencies directly into you `composer.json` file.

Sample
------

**composer.json**
```json
{
    "require": {
        "mouf/gulp-installer": "~1.0"
    },
    "extra": {
        "require-npm": {
            "gulp-concat": "~2.4.3",
            "gulp-uglify": "~1.1.0",
            "gulp-sourcemaps": "~1.3.0",
            "gulp-livereload": "~3.7.0",
            "gulp-minify-css": "~0.4.5",
            "gulp-less": "~3.0.0"
        }
    }
}
```

Hey! But that package does not contain anything expect a composer.json file!
----------------------------------------------------------------------------

Yup. Historically, this package used to contain a Composer plugin, but since most of the code used to generate
the link to `gulp` has been put in [Koala framework's composer extra assets](https://github.com/koala-framework/composer-extra-assets/),
this package is reduced to a mere `composer.json`.
