# Guides : Set-up
This repository contains multiple guides to help you to set-up, application, fix some problems and code in better conditions. The main applications used in these tutorials will be Unity, Intellij and VS Code. The main programming languages will be Java, C#, Python and Dart.
## Integrate Google Play Services and Publish your Android mobile game from Unity in 2020
For this tutorial, I did a video about that on YouTube (in French sorry, but it's easy to follow all steps). You can check-out this video with the link below : 
https://youtu.be/fAWV4mw5agY
## Unity Development with VS Code
VS Code compared to Visual Studio is optimized just for coding, so the interface is more simple but complete for development and easiest to use. That's why I use it for C# with Unity and Python. In this tutorial, we will see how to set-up VS Code and Unity, thanks to steps list below because it quit simple, but you can have a problem during the set-up and the solution is below. This link can also help you to understand all operations : https://code.visualstudio.com/docs/other/unity
### Steps to follow (all files are in the repository or you can find them in internet, but the version can be different) :
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
