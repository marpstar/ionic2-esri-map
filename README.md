# ionic2-esri-map

Prototype app demonstrating one approach for using Ionic (v3+) with the ArcGIS API for JavaScript.

# How to install

* Clone or download this repo
* Create an Ionic project. It can be either android or iOS

```
	npm install –g cordova ionic
	ionic start testApp tabs
	cd testApp
	ionic cordova platform add android
	npm install angular-esri-loader
```

* Run a quick test to make sure that boilerplate Ionic project loaded but running `ionic serve` from your projects
roots directory. If you don't get a web page launch then look for errors, something didn't install right.
* Then copy `index.html`, `home.html` and `home.ts` from this repo to their respective directories in your new project.
* Then build your project
 
```
	ionic cordova build android 
	ionic cordova run android
```

* Be sure to test your app on a native device!


# Notes
* Last tested using Ionic 3.10.3, Angular Core 4.1.3, Android 8.0, Chrome 60.0 (64-bit). 
* Not getting a location result in Android - do the following steps:
	* If you are using Android Studio look for errors in Android Monitor. You may have also gotten an application alert box when the `watchPosition()` request timed out.
	* Add these permissions to the `AndroidManifest.xml file`. You can find it under `/<your_project_directory>/platforms/android/`:

	```
	  <uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />
    <uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
	```
	
	* Go into the application settings on the device and enable `Location`.
	* Close your application using swipe and then restart it.


