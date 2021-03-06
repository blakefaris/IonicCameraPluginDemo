# IonicCameraPluginDemo
Ionic app that uses the Cordova Camera plugin to take a take or chose a photo then display the taken/chosen photo.
This app also allows for choosing and playing back a video.

## Setup
1. ```$ git clone git@github.com:blakefaris/IonicCameraPluginDemo.git```
1. ```$ cd IonicCameraPluginDemo```
1. ```$ cordova plugin add cordova-plugin-camera```  
1. ```$ cordova platforms add ios```
1. ```$ cordova build ios```
1. Refer to **Running on iPhone**


## My Initial Project Setup
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

If this shows that iOS is only 3.8.0 update iOS.

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

### Running on iPhone ###
1. Use a USB cable and connect your iPhone to your computer
1. Open **/platforms/ios/IonicCameraPluginDemo.xcodeproj**
1. For devices choose your iPhone
1. Click **Run**

#### Troubleshooting ####

##### Issue #####
I found that running in Ionic View for iOS there was no issues taking or choosing a photo.  However, when ran on an actual iPhone errors would occur. Initially, the buttons were unresponsive.  Touching 'Take Photo' or 'Choose Photo' would do nothing.

After some messing around I got the buttons to at least log an error in Xcode, something similar to the following:
```
ERROR: Plugin 'Camera' not found, or is not a CDVPlugin. Check your plugin mapping in config.xml
CDVCommandQueue executePending FAILED pluginJSON Camera takePicture
```

##### Solution #####
http://stackoverflow.com/questions/20326504/cordova-ios-plugins-fail-after-building-unless-i-remove-platform-and-plugin-jso

1. rm -rf platforms/ios
1. rm plugins/ios.json
1. cordova platforms add ios
1. cordova build ios

A better solution is do the recommended 'config.xml' changes.
