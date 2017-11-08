# Documentation SDK DTSXY
DTSXY is a framework developed to collect relevant information about user's location to better fit its needs.

## Requirements
* iOS 9+
* CoreLocation framework

## CocoaPods
To integrate DTSXY SDK into your Xcode project using CocoaPods, add into your pod file: 
```
source 'https://github.com/digitaltostore/specXY.git'
. . .
pod 'DTSXY'
```

## Getting started
1. If you don't use Cocoapods, drag the framework into your project manually
2. In info.plist add the pairs:
```
NSLocationWhenInUseUsageDescription : your custom message for iOS 9 and 10 users
NSLocationAlwaysUsageDescription: your custom message for iOS 9 and 10 users
NSLocationAlwaysAndWhenInUsageDescription: your custom message for iOS 11+ users
```
Those keys declare why you are requesting location and will be shown to the user.

3. In Capabilities enable Background Modes and select:
	* Location updates
4. In your AppDelegate, import the framework:
For ObjC project:
```objective-c
#import <DTSXY/DTSXY.h>
```
or for swift project:
```swift
import DTSXY
```
5. In didFinishLaunchingWithOptions add the following statement:
```objective-c
[DataXY startDataXYWithDTSID:@"YOUR_CLIENT_ID_NUMBER" allowingBackgroundMode:NO];
```
The client ID must be passed in order to init the SDK and start the location tracking. 
Pass NO to backgroundMode parameter in order to save user battery (recommended configuration).
If you pass YES, the SDK will perform continuous tracking and will have a significant 
battery impact (60% in one day). 

6. Stop the SDK
The SDK can be stopped whenever needed by calling
```objective-c
[DataXY stopDataXY];
```

## Contact

If you are having trouble using the SDK, please contact us at support.sdk.ios@adhslx.com
For commercial support, please write to vosdonnees@adhslx.com
