# Guides : Set-up
This repository contains multiple guides to help you to set-up, application, fix some problems and code in better conditions. The main applications used in these tutorials will be Unity, Intellij and VS Code. The main programming languages will be Java, C#, Python and Dart.
## 1) Integrate Google Play Services and Publish your Android mobile game from Unity
For this tutorial, I did a video about that on YouTube (in French sorry, but it's easy to follow all steps). You can check-out this video with the link below : 
[YouTube](https://youtu.be/fAWV4mw5agY)
## 2) Unity Development with VS Code
VS Code compared to Visual Studio is optimized just for coding, so the interface is more simple but complete for development and easiest to use. That's why I use it for C# with Unity and Python. In this tutorial, we will see how to set-up VS Code and Unity, thanks to steps list below because it quit simple, but you can have a problem during the set-up and the solution is below. This link can also help you to understand all operations : [Unity with VSCode](https://code.visualstudio.com/docs/other/unity)
### Steps to follow (all files and links are in the repository) :
- Install Visual Studio Code,
- Install the .NET Core SDK,
- Restart your computer,
- Install C# extension and reload VS Code (you don't need any Unity extensions).

After that, it's possible the it doesn't work. To see that, you can create a Unity C# script and write GameObject or Rigidbody to see if the code completion works. You can also see in the VS Code OUTPUT Panel a failure in OmniSharp Log. If it's your case :
- Install .NET Framework 4.7.1 Developer Pack;

If the problem persists :
- Uninstall C# extension and reload VS Code,
- Install C# extension (in the repository) in VS Code from VSIX,
- Reload VS Code.

Finally :
- Open a Unity Project, go in "Edit --> Preferences --> External Tools",
- In "External Script Editor" select Visual Studio Code.

<p align="center">
  <img width="483" alt="Step4" src="https://user-images.githubusercontent.com/73184884/125639435-1eb0b12b-58cd-4665-82e2-33fe9ef783c4.PNG">
</p>

## 3) Python Development with VS Code
To setup Python with VS Code, you just need a few step before coding. It's more simple than in previous tutorials :
- First, go on [python](https://www.python.org/downloads/) web site and install the version you would like. During the setup of the installation, go to advanced setting and check if "add path" is selected. You also can add shortcut, but you don't have to,
- After that, install the [VS Code](https://code.visualstudio.com/#alt-downloads) version you want and go into the extension menu. Install python extension (multiple extensions will be installed),
- Finally, create .py file and VS Code will automatically add python interpreter thanks to the first step (path added). If the adding doesn't work, click on the button in the bottom right corner near the notification icon and add the interpreter manually.
## 4) Flutter/Dart Development with IntelliJ
If you want to know how to set-up Flutter and Dart: plugins, SDK, import libraries with the terminal... this video explains everything :

Or you can also read this little guide to help you to configure your environment :
### 1) Global setup
- Install Intellij --> install plugins Flutter and Dart (auto), 
- Install flutter zip file on the flutter web site : https://flutter.dev/docs/get-started/install,
- Install Java and JDK,
- Install Android studio.

### 2) Import lib and use flutter commands in terminal :
Add in Path in Environment variable : C:\Users\yourName\flutter\bin
### 3) Fix error lib import on Intellij :
Open 'Edit Configuration' --> 'Additionnal run args' and add :
```
--no-sound-null-safety
```
### 4) Update flutter dependencies (pubspec.yaml) :
```
flutter pub get
```
### 5) Modify laucher icon and app name :
a) In pubspec.yaml, add :
```
dependencies:
	flutter_launcher_icons: "^0.8.0"
flutter_icons:
	android: true
	ios: true
	image_path: "path/image.png"
```
b) In Android --> app --> src --> main --> AndroidManifest.xml, modify :

android:label="Your app name"

c) Save and update in terminal with :
```
flutter pub get
flutter pub run flutter_launcher_icons:main
```
### 6) Build your app
```
flutter build apk --no-sound-null-safety
flutter install 
```
## 5) Java Development with IntelliJ
Coming soon.

## State:
- [x] Work in progress
- [ ] Work completed
