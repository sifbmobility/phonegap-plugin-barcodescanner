# Customized

local_plugins\phonegap-plugin-barcodescanner\8.1.0\phonegap-plugin-barcodescanner\src\android\barcodescanner.gradle

- Android gradle dependencies 'com.android.support:support-v4:24+'

local_plugins\phonegap-plugin-barcodescanner\8.1.0\phonegap-plugin-barcodescanner\src\ios\CDVBarcodeScanner.mm

- iOS Using fullscreen for UIModalPresentationStyle

==========>>>

- Changes (local_plugins/phonegap-plugin-barcodescanner/8.1.0/phonegap-plugin-barcodescanner/src/android/barcodescanner.gradle)
  implementation to compile >

compile(name:'barcodescanner-release-2.1.5', ext:'aar')

- to
  implementation(name:'barcodescanner-release-2.1.5', ext:'aar')
  =========

- Changes (apps/showroom-mb/local_plugins/phonegap-plugin-barcodescanner/8.1.0/phonegap-plugin-barcodescanner/package.json)
  Remove "jasmine-node": "1.14.5", from devDependecies to settle npm audit vulnerabilities problem

# Redmine #19928 - Jenn Hong

affected path: showroom-nx/apps/showroom-mb/local_plugins/phonegap-plugin-barcodescanner/8.1.0/phonegap-plugin-barcodescanner/src/windows/lib/Reader.cs

===========

Line 117 - Add logging in catch block for exception event

From -
catch (OperationCanceledException) { }

To -
catch (OperationCanceledException) {
Console.WriteLine("Barcode reading operation was canceled.");
}

===========

# Installation

If your platforms having the existing plugin, remove it first. Make sure platforms & plugins do not have the plugins.

- Remove plugin
  cordova plugin rm phonegap-plugin-barcodescanner

- Add plugin
  cordova plugin add ./apps/showroom-mb/local_plugins/phonegap-plugin-barcodescanner/8.1.0/phonegap-plugin-barcodescanner
