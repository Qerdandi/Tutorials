# I) Flutter/Dart Development with IntelliJ
If you want to know how to set-up Flutter and Dart: plugins, SDK, import libraries with the terminal... you can read this little guide to help you to configure your environment :

## 1) Global setup
- Install Intellij --> install plugins Flutter and Dart (auto), 
- Install flutter zip file on the flutter web site : https://flutter.dev/docs/get-started/install,
- Install Java and JDK,
- Install Android studio.

## 2) Import lib and use flutter commands in terminal :
Add in Path in Environment variable : C:\Users\yourName\flutter\bin

## 3) Fix error lib import on Intellij :
Open 'Edit Configuration' --> 'Additional run args' and add :
```
--no-sound-null-safety
```
## 4) Update flutter dependencies (pubspec.yaml) :
```
flutter pub get
```
## 5) Modify launcher icon and app name :
### a) In pubspec.yaml, add :
```
dependencies:
	flutter_launcher_icons: "^0.8.0"
flutter_icons:
	android: true
	ios: true
	image_path: "path/image.png"
```
### b) In Android --> app --> src --> main --> AndroidManifest.xml, modify :

android:label="Your app name"

### c) Save and update in terminal with :
```
flutter pub get
flutter pub run flutter_launcher_icons:main
```
## 6) Build your app
```
flutter build apk --no-sound-null-safety
flutter install 
```

# II) Apache Cordova with VS Code

## 1) Install Apache Cordova and dependencies

### a) Install Java jdk 17 (LTS version is recommended)
- Add Env Variable : `JAVA_HOME=C:\Program Files\__Download__\Java\jdk-19` (System Variable)
> jdk 17 version is just an example (also works with jdk 19)

### b) Install [Android Command Line Tools](https://developer.android.com/studio)
- Unzip `cmdline-tools` folder in a new folder named `android_sdk` (Example location: `C:\Users\User1\__Download__\android_sdk`)
- Put all files, in `android_sdk`, in a new folder named `latest` child of `android_sdk`
- Add Env Variable :  
`ANDROID_HOME=C:\Users\User1\__Download__\android_sdk` (System Variable)  
`C:\Users\User1\__Download__\android_sdk\cmdline-tools\latest\bin` in Path (System Variable)  

### c) Install [sdkmanager tools](https://developer.android.com/tools/sdkmanager)
- Open CMD as admin
- Execute this command: 
```
sdkmanager "platform-tools" "platforms;android-33" "build-tools;33.0.2"
```

### d) Install [Gradle](https://gradle.org/releases/)
- Unzip folder and rename it `gradle` in `C:\Users\User1\__Download__\android_sdk\`
- Add Env Variable:  
`%ANDROID_HOME%\gradle\bin` in Path (System Variable)  
`%ANDROID_HOME%\platform-tools` in Path (System Variable)  
`%ANDROID_HOME%\latest\bin` in Path (System Variable)
`%ANDROID_HOME%\build-tools` in Path (System Variable)

### e) Install [Nodejs](https://nodejs.org/en/download)
- Add Env Variable:  
`C:\Users\User1\AppData\Roaming\npm` in Path (User Variable)  
`C:\Program Files\__Download__\nodejs\` in Path (System Variable)  

### f) Install Cordova
- Execute in CMD this command:
```
npm install -g cordova
```

### g) Setup VS Code
- Install `Cordova Tools` extension

> Source: [Android Platform Guide](https://cordova.apache.org/docs/en/11.x/guide/platforms/android/index.html)

## 2) Create and build Android app

### a) Create a project by executing in CMD:
```
cordova create <project-directory> <package-name> <project-name>
cd <project-directory>
cordova platform add android --save
```

### b) Build Android app (.apk file) by executing in CMD:
```
cordova build android
```
> Source: [Create your first Cordova app](https://cordova.apache.org/docs/en/11.x/guide/cli/index.html)