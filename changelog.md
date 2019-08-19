===========
What's new?
===========

[6.1934]
* Rename method disableMappyLogs to disableAnonymousStudiesLogs
  + (void)disableAnonymousStudiesLogs:(BOOL)disabled;
* Add new method
  + (void)disableAdvertisingLogs:(BOOL)disabled;
* Add new method
  + (void)setConsents:(nonnull NSDictionary<NSString *,NSNumber *> *)consents;
* Add new method
  + (void)setCustomHostForLocations:(nullable NSString *)locationsHost forVisits:(nullable NSString *)visitsHost;

[6.1914]
* The SDK now send also logs to Mappy by default
* Change start method signature with two mandatory parameters : locationsID and visitsID
  + (void)startDataXYAllowingBackgroundMode:(BOOL)backgroundModeAllowed 
                            withLocationsID:(nonnull NSString *)locationsID
                            withVisitsID:(nonnull NSString *)visitsID;

* Add a method to customize the broadcasting time interval : 
  + (void)setDataXYBroadcastInterval:(NSTimeInterval)interval;

* Add a method to disable logs sending to Mappy :
  + (void)disableMappyLogs:(BOOL)disabled;
