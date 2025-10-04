Franklin T9 Manager - controls a Franklin T9 (r717) Hotspot device over SSH via plink.exe and ICMP commands

Made using Visual Studio, written in C#

<img width="300" height="200" alt="image" src="https://github.com/user-attachments/assets/eb9cc602-9c6c-4ba5-a0c0-4ede45db8604" />

Purpose:

This application was written to remotely confirm online status/connectivity for a Franklin T9 rooted 4G wireless access point. This device is small, inexpensive, rootable, and provides access to physical terminals for attaching external antennae. This is especially useful if you would like to pair the T9 with a home network router, such as an ASUSWRT system (if you are looking for a router, I would highly recommend selecting one which can be flashed with ASUSWRT-Merlin https://asuswrt-merlin.net/ for its extensive feature set).

Detailed technical documentation on the Franklin T9 (r717) 4G Hotspot available at https://docs.google.com/document/d/1LgYLB0sJbwAMW2VfcNoGavIJQhiYCJzsWK4onOFdSys/edit

See file MyCustomApplicationContext.cs for majority of functionality.

Features:

- network accessibility status in the form of a visual icon (green == online, red == offline)

- remotely reboot the T9 by sending an SSH command by wrapping plink.exe (from the makers of PuTTY)

- easily access all of the secret administrative/debug pages
   - upon opening a shortcut, a notification containing the default username & password pops up which can be clicked to copy for easy pasting

- easily access comprehensive initial set up document

Dependencies required to run:
1) Download .NET Desktop Runtime 6.0.36: https://dotnet.microsoft.com/en-us/download/dotnet/6.0

Build process:
1) Download .NET SDK 6.0.428: dotnet.microsoft.com/en-us/download/dotnet/6.0
2) Run in administrator shell in project directory: dotnet publish -c Release -r win-x64 --self-contained false

Potential Future Features:

- connection (band and signal strength) and data usage info on a hover bubble popup

- band selection menu

- automated setup (e.g. disabling automatic update, sim unlocking, installing TTL modifier script)

- changing default passwords for hidden pages, wifi network
