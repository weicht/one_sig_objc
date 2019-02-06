We have OneSignal integrated with our product and it works great in Android. When we attempt to compile/link it for iOS we get into various issues. Over the course of a week, we have searched and attempted the various steps in forums.

Based upon our attempts, we end up in one of two scenarios:

A)
```flutter.tools [!] The 'Pods-Runner' target has frameworks with conflicting names: onesignal.framework.```

B)
```In file included from /Users/weicht/devel/flutter/.pub-cache/hosted/pub.dartlang.org/onesignal-1.0.5/ios/Classes/OneSignalCategories.m:28:
    /Users/weicht/devel/flutter/.pub-cache/hosted/pub.dartlang.org/onesignal-1.0.5/ios/Classes/OneSignalCategories.h:28:9: fatal error: 'OneSignal/OneSignal.h' file not found
    #import <OneSignal/OneSignal.h>
            ^~~~~~~~~~~~~~~~~~~~~~~
    1 error generated.
    /Users/weicht/devel/flutter/.pub-cache/hosted/pub.dartlang.org/onesignal-1.0.5/ios/Classes/OneSignalTagsController.m:29:9: fatal error: 'OneSignal/OneSignal.h' file not found
    #import <OneSignal/OneSignal.h>
            ^~~~~~~~~~~~~~~~~~~~~~~
    1 error generated.
```  
    
    
    
Notes:    
    
1) we are on 1.0.3

2) Followed OneSignal documentation for iOS

3) we can't remove use_frameworks! then other plugins we rely wont work.

4) podfile in post_install section after config.build_settings['ENABLE_BITCODE'] = 'NO'

5) config.build_settings ['SWIFT_VERSION'] = '4.2'



