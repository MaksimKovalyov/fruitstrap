fruitstrap
==========
Install and debug iPhone apps without using Xcode. Designed to work on unjailbroken devices.

## Requirements

* Mac OS X. Tested on Lion and Snow Leopard.
* You need to have a valid iPhone development certificate installed.
* Xcode must be installed, along with the SDK for your iOS version.

## Usage

* `fruitstrap [-d] <app> [device_id]`
* Optional `-d` flag launches a remote GDB session after the app has been installed.
* `<app>` must be an iPhone application bundle, *not* an IPA.
* Optional device id, useful when you have more than one iPhone/iPad connected to your computer

## Demo

* The included demo.app represents the minimum required to get code running on iOS.
* `make install` will install demo.app to the device.
* `make debug` will install demo.app and launch a GDB session.

## Notes

* With some modifications, it may be possible to use this without Xcode installed; however, you would need a copy of the relevant DeveloperDiskImage.dmg (included with Xcode). GDB would also run slower as symbols would be downloaded from the device on-the-fly.

## Issues

* If the app is not compiled for the right iOS version, fruitstrap will succeed but the app will not run (eg. if your app is iOS 5+ only and the device is running iOS 4, fruitstrap runs and seems to copy the app to the device, but it does not appear in Springboard)
