# I) Integrate Google Play Services and Publish your Android mobile game from Unity
For this tutorial, I did a video about that on YouTube (in French sorry, but it's easy to follow all steps). You can check-out this video with the link below : 
[YouTube](https://youtu.be/fAWV4mw5agY)

# II) Unity Development with VS Code
VS Code compared to Visual Studio is optimized just for coding, so the interface is more simple but complete for development and easiest to use. That's why I use it for C# with Unity and Python. In this tutorial, we will see how to set-up VS Code and Unity, thanks to steps list below because it quit simple, but you can have a problem during the set-up and the solution is below. This link can also help you to understand all operations : [Unity with VSCode](https://code.visualstudio.com/docs/other/unity)
## Steps to follow :
- Install [Visual Studio Code](https://code.visualstudio.com/Download),
- Install the [.NET Core SDK](https://dotnet.microsoft.com/en-us/download/dotnet/sdk-for-vs-code?utm_source=vs-code&amp;utm_medium=referral&amp;utm_campaign=sdk-install),
- Restart your computer,
- Install C# extension and reload VS Code (you don't need any Unity extensions).

After that, it's possible the it doesn't work. To see that, you can create a Unity C# script and write GameObject or Rigidbody to see if the code completion works. You can also see in the VS Code OUTPUT Panel a failure in OmniSharp Log. If it's your case :
- Install [.NET Framework 4.7.1 Developer Pack](https://dotnet.microsoft.com/en-us/download/dotnet-framework/thank-you/net471-developer-pack-offline-installer);

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