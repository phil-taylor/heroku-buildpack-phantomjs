Heroku buildpack: PhantomJS
=======================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) of PhantomJS(http://phantomjs.org).

Usage
-----

Example usage:

```shell
$ heroku create --stack cedar --buildpack https://github.com/stomita/heroku-buildpack-phantomjs.git

# or if your app is already created:
$ heroku config:add BUILDPACK_URL=https://github.com/stomita/heroku-buildpack-phantomjs.git

$ git push heroku master
```

Note
-----
This version has been patched so that the following environment variables are updated to include phantomjs paths.

    PATH="$PATH:/$HOME/vendor/phantomjs/bin"
    LD_LIBRARY_PATH="$LD_LIBRARY_PATH:/$HOME/vendor/phantomjs/lib"

It has been tested and verified to work on CloudFoundry V2.
