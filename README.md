# IonicCameraPluginDemo

## Initial Setup
Mostly from: http://sourcefreeze.com/cordova-camera-plugin-example-using-ionic-framework/

http://ionicframework.com/getting-started/


## Adding Cordova Camera Support

http://ngcordova.com/docs/install/

http://ngcordova.com/docs/plugins/camera/


``` $ cordova platform list ```

Installed platforms:
  android 5.1.1
  ios 3.8.0
Available platforms:
  amazon-fireos ~3.6.3 (deprecated)
  blackberry10 ~3.8.0
  browser ~4.1.0
  firefoxos ~3.6.3
  osx ~4.0.1
  webos ~3.7.0

If this shows that ios is onlyi 3.8.0 update ios.

``` $ cordova platform update ios ```

``` $ cordova platform list ```

Installed platforms:
  android 5.1.1
  ios 4.1.1
Available platforms:
  amazon-fireos ~3.6.3 (deprecated)
  blackberry10 ~3.8.0
  browser ~4.1.0
  firefoxos ~3.6.3
  osx ~4.0.1
  webos ~3.7.0

``` $ cordova plugin add cordova-plugin-camera ```

Include the source to index.html.

```
<script src="lib/ionic/js/ionic.bundle.js"></script>
<script src="lib/ngCordova/dist/ng-cordova.js"></script>
```

Add ngCordova to angular.module within app.js

``` angular.module('starter', ['ionic', 'ngCordova']) ```

Building of iOS should work.

``` ionic build ios ```
