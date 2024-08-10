# BookOAH
A tool to get Samsung Galaxy Book exclusive apps running on any hardware.

> [!NOTE]
> The project isn't finished _yet_.
> Come back soon!

> [!CAUTION]
> I am not responsible for any damage done to your Windows installation.
> You are doing this at your own risk.

## Supported Windows Versions
The tool only supports the following Windows versions(or newer):
* Windows 11 21H2
* Windows 11 22H2
* Windows 11 23H2

## Installation Guide
### Automatic Installation _(recommended)_
* Download the automatic installer from the [latest release](https://github.com/jakissajmon/BookOAH/releases/latest).
* Open the installer, customize the installation to your liking and press _Patch_.
* Done!
### Manual Installation _(not recommended)_
* Download the [setup.reg file](https://github.com/jakissajmon/BookOAH/raw/main/setup.reg) and import it into your registry.
* Download the [Samsung Update](https://github.com/jakissajmon/BookOAH/raw/main/SAMSUNGUPDATE.Msixbundle) package and install it on your computer.
* Create a new script in any location with the following code:
```
@echo off
reg import setup.reg
```
and save it as a batch file(.bat).
* Create a new folder(for example ``C:\oneui``) and copy the new batch file and the setup.reg file into this folder.
* Create a new task in Task Scheduler(taskschd.msc) starting the batch file in your newly created folder **as an administrator** every time **any user logs in**.
* Done!

> [!WARNING]
> Redistribution of this software in source or binary forms shall be free of all charges or fees to the recipient of this software.
