Cloudfoundry buildpack: geo
=====================

This is a [Cloudfoundry (cf) buildpack](http://devcenter.heroku.com/articles/buildpacks) that
vendors main geo/gis libraries like geos, proj and gdal.

You will use this buildpack with other major buildpack such as python buildpack.

This is a small modification to the [heroku-geo-buildpack](https://github.com/cyberdelia/heroku-geo-buildpack), for use in cloudfoundry / bluemix.

Currently this fork installs:
  ```
     geos version: 3.4.2
     gdal version: 1.11.1
     proj version: 4.8.0_1
  


Usage
-----

Example usage:
