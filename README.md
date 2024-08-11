# BookOAH
A tool to get Samsung Galaxy Book exclusive apps running on any hardware(without modifying them).

> [!NOTE]
> For now, we are using *regedit* instead of *reg import* to reimport the registry values(because of a weird error), which means you will have to confirm the import every reboot or the Samsung apps won't work.
> Thanks for understanding!

> [!CAUTION]
> I am not responsible for any damage done to your Windows installation.
> You are doing this at your own risk.

## Requirements
The tool only supports the following Windows versions(or newer):
* Windows 11 21H2
* Windows 11 22H2
* Windows 11 23H2
> Installing it on older versions can break your installation!
You also need to be logged in to your Microsoft account.
To prevent false positives, disable your antivirus before downloading the automatic installer.

## Installation Guide
### Automatic Installation _(recommended)_
* Download the automatic installer from the [latest release](https://github.com/jakissajmon/BookOAH/releases/latest).
* Open the installer, customize the installation to your liking and press _Patch_.
* Done!
### Manual Installation _(not recommended)_
* Download the [setup.reg file](https://github.com/jakissajmon/BookOAH/raw/main/setup.reg) and import it into your registry.
* Install the [Samsung Update](https://apps.microsoft.com/detail/9nq3hdb99vbf) and [Samsung Account](https://apps.microsoft.com/detail/9p98t77876kz) app on your computer.
* Create a new script in any location with the following code:
```
@echo off
reg import setup.reg
regedit setup.reg
```
and save it as a batch file(.bat).
* Create a new folder(named ``C:\oneui``) and copy the new batch file and the setup.reg file into this folder.
* Create a new task in Task Scheduler(taskschd.msc) in the path ``\`` named ``BookOAH`` starting the batch file in your newly created folder **as an administrator** every time **any user logs in**.
* Download the Samsung apps you want from the [Microsoft Store](https://apps.microsoft.com/search?query=Samsung).
* Done!

> [!WARNING]
> Redistribution of this software in source or binary forms shall be free of all charges or fees to the recipient of this software.
