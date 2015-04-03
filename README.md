[Gulp installer for Composer](http://mouf-php.com/packages/mouf/gulp-installer)
=============================

This is an installer that will download [Gulp](http://gulpjs.com/) and install it in your PHP project.
Installation is performed using NPM via the [Koala framework's composer extra assets](https://github.com/koala-framework/composer-extra-assets/) 
plugin. Gulp is a NodeJS package. If NodeJS is not available on your computer, it will be downloaded and installed
locally, thanks to [Mouf's node-installer](https://github.com/koala-framework/composer-extra-assets/) package.

Why?
----

Because Gulp is an extraordinary tool to manage assets (JS, CSS, LESS, SASS, Coffeescript files....) and because 
it is not a common tool in the PHP stack.

How?
----

Simply include this package in your `composer.json` requirements:

```json
{
    "require": {
        "mouf/gulp-installer": "~1.0"
    }
}
```

Then, you can run Gulp using the `vendor/bin/gulp` script (`vendor/bin/gulp.bat` on Windows).
