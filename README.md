# Windows for Developers (Not Windows Developers)

This is a short description with solutions for every developer new on Windows coming from macOS or GNU/Linux. Sometimes you have to work on Windows as a developers because of company guidelines. So this description is for you.

- [Package Manager](#package-manager)
- [Terminal](#terminal)

## Package Manager

On GNU/Linux distributions you have package manager by default on board (for example apt on debian) and you know how useful it is.

Also on macOS you have unofficial package managers like homebrew (short: brew) which are very good and useful since macOS has no official package manager.

So working on Windows as a developer you may be looking for a package manager on Windows and you're very lucky since there is a solution:

[Chocolatey - The Package Manager for Windows](https://chocolatey.org/)

### Installation

The installation is very easy. Just open a PowerShell as Administrator:

1. Press Windows Key
2. Enter "PowerShell"
3. Right Click on "Windows PowerShell" and then "Start as Administrator"

Then run the following command:

```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```

After that you can start the Windows Command Shell (cmd.exe) and use the ```choco``` command.

### Usage

The usage of choco command is also very easy and similar to the apt or brew command. I think the most important commands are search, info and install.

You can see all commands with:

```choco -h``` or ```choco /?```

**Please keep in mind to start the Command Shell or PowerShell as Administrator when using Chocolatey.**

## Terminal

Besides the package manager the terminal is on of the most important tools of a developer coming from macOS or GNU/Linux.

On Windows there is the Command Shell (cmd.exe) and PowerShell (PowerShell.exe). But to me as a developer these command shells were not quite satisfying so I was looking for another solution.

Amazingly I found one good solution from Microsoft called Microsoft Terminal, which is currently a preview version:

[Microsoft Terminal (Preview)](https://www.microsoft.com/en-us/p/windows-terminal-preview/9n0dx20hk701)

You can also install it using Chocolatey: ```choco install microsoft-windows-terminal```

I primarily use it with the Windows-Subsystem for Linux (WSL) which is I think the easiest way to use Linux on Windows.

[Windows-Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/install-win10)
