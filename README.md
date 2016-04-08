# IonicCameraPluginDemo

## Initial Setup
Mostly from: http://sourcefreeze.com/cordova-camera-plugin-example-using-ionic-framework/

### Adding Coredova Camera Support

Found the following command at http://ngcordova.com/docs/plugins/camera/

``` $ cordova plugin add cordova-plugin-camera ```

Got warning:
Using this version of Cordova with older version of cordova-ios is being deprecated. Consider upgrading to cordova-ios@4.0.0 or newer.


``` $ cordova platform list ```
```
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
```
  This shows that ios is only 3.8.0.

``` $cordova platform update ios ```
```
Updating ios project...
iOS project updated with cordova-ios@4.1.1
cp: copyFileSync: could not write to dest file (code=ENOENT):/Users/blakefaris/Documents/Development/Ionic/CameraPluginDemo/platforms/ios/HelloCordova/config.xml

Error: ENOENT, no such file or directory '/Users/blakefaris/Documents/Development/Ionic/CameraPluginDemo/platforms/ios/HelloCordova/config.xml'
```
Even with the error ios 4.1.1 seems to now be used:

``` $ cordova platform list ```
```
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
```

### ionic run ios
Error occurs:
fatal error: 'Cordova/CDVViewController.h' file not found

Possible Solution:
http://stackoverflow.com/questions/34546607/xcode-7-2-in-archive-getting-the-issue-cordova-cdvviewcontroller-h-file-n

Uploading to Ionic Apps and using iPhone app Ionic View works.  A picture can be taken with the camera or chosen from the camera roll.
