Franklin T9 Manager - controls a Franklin T9 (r717) Hotspot device over SSH via plink.exe and ICMP commands

Made using Visual Studio, written in C#

<img width="392" height="262" alt="image" src="https://github.com/user-attachments/assets/eb9cc602-9c6c-4ba5-a0c0-4ede45db8604" />

Run:
1) Download .NET Desktop Runtime 6.0.36: https://dotnet.microsoft.com/en-us/download/dotnet/6.0

Build:
1) Download .NET SDK 6.0.428: dotnet.microsoft.com/en-us/download/dotnet/6.0
2) Run in administrator shell in project directory: dotnet publish -c Release -r win-x64 --self-contained false

Detailed technical documentation on the Franklin T9 (r717) 4G Hotspot available at https://docs.google.com/document/d/1LgYLB0sJbwAMW2VfcNoGavIJQhiYCJzsWK4onOFdSys/edit

Features include:

- network accessibility status (I use an Asus router to extend wifi reach/hardwire multiple devices so simply being network connected doesn't mean the T9 is connected)

- menu options to remotely reboot the T9 (sends an SSH command using plink.exe, from the makers of PuTTY)

- provides links to all of the secret administrative/debug pages, upon opening provides a notification contiaining default password which can be clicked to copy for easy entry

- link to comprehensive set up document I'm working on

Future features:

- connection (band and signal strength) and data usage info on a hover bubble popup

- band selection menu

- automated setup (e.g. disabling automatic update, sim unlocking, installing TTL modifier script)

- changing default passwords for hidden pages, wifi network

See file MyCustomApplicationContext.cs for majority of functaionality.

