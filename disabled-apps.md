# Android app disabling

The idea here is to disable android apps in a way that requires me to plug my phone into a computer and run ADB commands to re-enable.
Hopefully this will prove to be enough of a barrier that it will effectively mean my phone is the kind of dumbphone that I want, one with messaging apps, financial apps, maps etc. but no infinite scrolling or web browsing.

# Disabled apps

firefox - org.mozilla.firefox
instagram - com.instagram.android
facebook - com.facebook.katana
reddit - com.reddit.frontpage
twitter - com.twitter.android

# Disable commands

adb shell pm disable-user --user 0 org.mozilla.firefox
adb shell pm disable-user --user 0 com.instagram.android
adb shell pm disable-user --user 0 com.facebook.katana
adb shell pm disable-user --user 0 com.reddit.frontpage
adb shell pm disable-user --user 0 com.twitter.android

# See list of disabled apps

adb shell pm list packages -d

# Re-enable the disabled apps

adb shell pm enable org.mozilla.firefox
adb shell pm enable com.instagram.android
adb shell pm enable com.facebook.katana
adb shell pm enable com.reddit.frontpage
adb shell pm enable com.twitter.android
