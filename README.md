<p align="middle">
<img align="middle" height="100" src="https://raw.githubusercontent.com/Void48/chatsen.readme.improvements/master/assets/ayyybubu/logo.png">
<p>
<h1 align="middle">Chatsen</h1>

<p align="middle" float="left">
  <a href="https://chatsen.app/discord"><img src="https://img.shields.io/discord/758710852756570153?color=5865F2&label=chat&logo=discord&logoColor=white"></a>
  <a href="https://hanadigital.github.io/grev/?user=chatsen&repo=chatsen"><img src="https://img.shields.io/github/downloads/chatsen/chatsen/total?color=23B14D"></a>
  <a href="https://github.com/chatsen/chatsen/blob/master/LICENSE"><img src="https://img.shields.io/github/license/chatsen/chatsen"></a>
</p>
<p align="middle" float="left">
<a href="https://apps.apple.com/us/app/chatsen/id1574037007"><img height="75" src="https://user-images.githubusercontent.com/85196642/144549880-7fb6b342-a9f9-47e3-a78d-b4b23e9d4b3e.png"></a>
  <a href="https://testflight.apple.com/join/I7Fm27MH"><img height="75" src="https://raw.githubusercontent.com/Void48/chatsen.readme.improvements/master/assets/testflightbadge.png"></a>
  <a href="https://play.google.com/store/apps/details?id=com.chatsen.chatsen"><img height="75" src="https://play.google.com/intl/en_us/badges/images/generic/en_badge_web_generic.png"></a>
</p>

Chatsen is a cross-platform application that allows you to chat on Twitch with support for 3rd-party services such as 7TV, BTTV and FFZ.  
It also features a built-in video player and a variety of other features, such as auto-completion, notifications (on supported platforms), whispers, and more to come!

# Media
<p align="middle" float="left">
  <img src="https://raw.githubusercontent.com/chatsen/resources/master/assets/screenshots/1.png" width="200" />
  <img src="https://raw.githubusercontent.com/chatsen/resources/master/assets/screenshots/2.png" width="200" />
  <img src="https://raw.githubusercontent.com/chatsen/resources/master/assets/screenshots/3.png" width="200" />
  <img src="https://raw.githubusercontent.com/chatsen/resources/master/assets/screenshots/4.png" width="200" />
</p>

The Chatsen logo was graciously made by @ayyybubu! You can find him on [Twitter](https://twitter.com/ayyybubu) or [Twitch](https://twitch.tv/ayyybubu)

# Downloads
You can find the latest release for supported platforms **(iOS, Android)** [here](https://github.com/Chatsen/chatsen/releases).

# Store Releases
- [x] [Play Store](https://play.google.com/store/apps/details?id=com.chatsen.chatsen)
- [x] [App Store](https://apps.apple.com/us/app/chatsen/id1574037007)
- [x] [Apple TestFlight](https://testflight.apple.com/join/I7Fm27MH)
- [ ] F-Droid Store

# Supported platforms
- [x] Android 5+ **(>=4.1 && <5.0 also supported but without login/video player)**
- [x] iOS 12.2+ **(Compatibility: Lowest supported iOS version is 9.0, but some things might not work since it's so old)**

# Support and donations
Support the project on Patreon and get some cool badges next to your username in return!
https://www.patreon.com/chatsen

# Build instructions
To build Chatsen, all you should need is the Flutter SDK on the **master** branch and its required dependencies for your platform [(Android Studio for Android](https://developer.android.com/studio) and [Xcode for iOS)](https://developer.apple.com/xcode/resources/).  
Running the following commands should allow you to build the application successfully:

```bash
flutter create .
rm -rf test

# Android
sed -i '/<\/manifest>/i \ \ \ \ <uses-sdk tools:overrideLibrary="io.flutter.plugins.webviewflutter"/>' ./android/app/src/main/AndroidManifest.xml
sed -i '/.*package=".*".*/i \ \ \ \ xmlns:tools="http://schemas.android.com/tools"' ./android/app/src/main/AndroidManifest.xml
sed -i '/.*package=".*".*/a \ \ \ <uses-permission android:name="android.permission.INTERNET"/>' ./android/app/src/main/AndroidManifest.xml
sed -i '/.*release {.*/a \ \ \ \ \ \ \ \ \ \ \ \ shrinkResources false\n\ \ \ \ \ \ \ \ \ \ \ \ minifyEnabled false' ./android/app/build.gradle
flutter pub run flutter_launcher_icons:main
flutter build apk

# iOS
flutter pub run flutter_launcher_icons:main
flutter build ios --no-codesign
```

You may also check the GitHub Actions file [here](https://github.com/chatsen/chatsen/blob/master/.github/workflows/main.yml) for more details.

# Licensing
Chatsen is distributed under the AGPLv3 licence. A copy may be found in the LICENSE file in that repository. All the dependencies remain under their original licenses.

# Usage
This project and its releases are provided as-is, no support is provided. Use at your own discretion.

# Privacy Policy
Chatsen does not collect any personal or identifying information whatsoever. There are no servers, services or backend running related to the project either.  
Since Chatsen uses the Twitch API, however, you are subject to their Privacy Policy available at: https://www.twitch.tv/p/en/legal/privacy-notice/

# Contact
- Discord: https://chatsen.app/discord
