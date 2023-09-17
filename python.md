# I) Python Development with VS Code
To setup Python with VS Code, you just need a few step before coding. It's more simple than in previous tutorials :
- First, go on [python](https://www.python.org/downloads/) web site and install the version you would like. During the setup of the installation, go to advanced setting and check if "add path" is selected. You also can add shortcut, but you don't have to,
- After that, install the [VS Code](https://code.visualstudio.com/#alt-downloads) version you want and go into the extension menu. Install python extension (multiple extensions will be installed),
- Finally, create .py file and VS Code will automatically add python interpreter thanks to the first step (path added). If the adding doesn't work, click on the button in the bottom right corner near the notification icon and add the interpreter manually.

# II) Python with pyenv-win and pyenv-win-venv

## 1) Install pyenv-win and setup Env variables
### a) Install pyenv-win using, in CMD:
```
git clone using command prompt git clone https://github.com/pyenv-win/pyenv-win.git "%USERPROFILE%\.pyenv"
```
### b) In admin Powershell, add Env variables using:
```
[System.Environment]::SetEnvironmentVariable('PYENV',$env:USERPROFILE + "\.pyenv\pyenv-win\","User")
[System.Environment]::SetEnvironmentVariable('PYENV_ROOT',$env:USERPROFILE + "\.pyenv\pyenv-win\","User")
[System.Environment]::SetEnvironmentVariable('PYENV_HOME',$env:USERPROFILE + "\.pyenv\pyenv-win\","User")
[System.Environment]::SetEnvironmentVariable('path', $env:USERPROFILE + "\.pyenv\pyenv-win\bin;" + $env:USERPROFILE + "\.pyenv\pyenv-win\shims;" + [System.Environment]::GetEnvironmentVariable('path', "User"),"User")
```
## 2) Install pyenv-win-venv and setup Env variables
### a) Install pyenv-win-venv using, in CMD:
```
git clone https://github.com/pyenv-win/pyenv-win-venv "%USERPROFILE%\.pyenv-win-venv"
```
### b) In admin Powershell, add Env variables using:
```
[System.Environment]::SetEnvironmentVariable('path', $env:USERPROFILE + "\.pyenv-win-venv\bin;"  + [System.Environment]::GetEnvironmentVariable('path', "User"),"User")
```
If you are getting any unauthorized access errors or unauthorized access to functions, in admin Powershell, use:
```
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope LocalMachine
```
> Source : this quick guide is possible thanks to Kiran Kumar Kotari developers of [pyenv-win](https://github.com/pyenv-win/pyenv-win), Arbaaz Laskar developers of [pyenv-win-venv](https://github.com/pyenv-win/pyenv-win-venv) and all contributors of this 2 projects. More information and example on those links.