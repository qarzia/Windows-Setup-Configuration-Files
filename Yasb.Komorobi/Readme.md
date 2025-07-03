🪟 Komorebi + YASB Beginner Guide

This is my personal setup for Komorebi and YASB, using the YASB 002 Dynamic theme.

    💙 Special thanks to Diiv for the inspiration and guidance!
    📺 Watch their full tutorial on YouTube:
    Diiv's Komorebi + YASB Setup Guide

https://www.youtube.com/watch?v=u7Gi1fU8LTQ&list=LL&index=8

🛠️ Step 0.1 – Enable Long Path Support (Important for Windows)

Open PowerShell as Administrator and run this:

Set-ItemProperty 'HKLM:\SYSTEM\CurrentControlSet\Control\FileSystem' -Name 'LongPathsEnabled' -Value 1

💻 Step 0.2 – Install Komorebi + WHKD

In your terminal (PowerShell or Windows Terminal), run:

winget install LGUG2Z.komorebi
winget install LGUG2Z.whkd

🔁 Step 0.3 – Restart Your Terminal

Close the terminal completely and open a new one. Then, run:

komorebic quickstart

This will generate your initial config files and folder structure for Komorebi.
📋 Step 0.4 – Requirements

    ✅ Windows 10 or 11

    ✅ Nerd Fonts
    Install a Nerd Font (I recommend JetBrainsMono Nerd Font) and set it as your terminal or status bar font.

📦 Step 1 – Install YASB (Yet Another Status Bar)

You can install it either:

    Via GitHub: YASB v1.7.6 Release
    or

    Via terminal with winget:

winget install --id AmN.yasb

🚀 Step 2 – Start Komorebi + YASB

    Launch YASB first.

    Then run Komorebi with:

    komorebic start --whkd

📝 Step 3 – Customize the Config

To edit your Komorebi configuration:

code .\komorebi.json

    🧠 Tip: This opens your komorebi.json in Visual Studio Code (make sure it's installed).

You can either:

    Modify it to your preferences,

    Or replace it with my configuration files
