We have OneSignal integrated with our product and it works great in Android. When we attempt to compile/link it for iOS we get into various issues. Over the course of a week, we have searched and attempted the various steps in forums. We are able to get it to the point where it states: flutter.tools [!] The 'Pods-Runner' target has frameworks with conflicting names: onesignal.framework.

1) we are on 1.0.3

2) Followed OneSignal documentation for iOS

3) we can't remove use_frameworks! then other plugins we rely wont work.

4) podfile in post_install section after config.build_settings['ENABLE_BITCODE'] = 'NO'

5) config.build_settings ['SWIFT_VERSION'] = '4.2'Any assistance you may be able to provide would be greatly appreciated.
