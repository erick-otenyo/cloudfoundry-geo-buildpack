Cloudfoundry buildpack: geo
=====================

This is a [Cloudfoundry (cf) buildpack](http://devcenter.heroku.com/articles/buildpacks) that
vendors main geo/gis libraries like geos, proj and gdal.

You will use this buildpack with other major cloudfoundry buildpack such as the [python buildpack](https://github.com/cloudfoundry/python-buildpack).

This is a small modification to the [heroku-geo-buildpack](https://github.com/cyberdelia/heroku-geo-buildpack), for use in cloudfoundry / bluemix.

Currently this fork installs:
  ```
     geos version: 3.4.2
     gdal version: 1.11.1
     proj version: 4.8.0_1
  ```


Usage
-----

Example usage:

You may have to use a buildpack that will enable setting multi-buildpacks on your bluemix environment.

After some trial and error, [cf-multi-buildpack](https://github.com/pl31/cf-multi-buildpack.git) was my pick.

In this case, you must have a file named `.cfbuildpacks` at the root of your django project with the buildpacks information.

For example:
  ```
  https://github.com/edge-spatial/heroku-geo-buildpack.git
  https://github.com/cloudfoundry/python-buildpack.git
  
  ```
Then push the app with the `-b https://github.com/pl31/cf-multi-buildpack.git` flag:
  ```
  cf push -b https://github.com/pl31/cf-multi-buildpack.git
  ```
  
Have some pancakes if it worked ! :) 

If it did not work,open an issue for help..
