📁 README.md

# 🪟 Komorebi + YASB Setup (Windows Tiling WM)

This repository contains my personal configuration for [Komorebi](https://github.com/LGUG2Z/komorebi) and [YASB (Yet Another Status Bar)](https://github.com/amnweb/yasb), including the **YASB 002 Dynamic Theme**.

> 🧠 Inspired by [Diiv’s YouTube tutorial](https://www.youtube.com/watch?v=u7Gi1fU8LTQ&list=LL&index=8)  
> 💻 Tiling window management + custom status bar, right on Windows!

---

## ⚙️ Features

- Full Komorebi + YASB setup
- Nerd Font integration (JetBrainsMono)
- Weather, volume, taskbar, workspace, and app widgets
- Power menu with animations
- Wallpaper gallery + auto-theming integration (optional)

---

## 🚀 Setup Instructions

### 🛠 Step 1: Enable Long Path Support

Open **PowerShell as Administrator** and run:

```powershell
Set-ItemProperty 'HKLM:\SYSTEM\CurrentControlSet\Control\FileSystem' -Name 'LongPathsEnabled' -Value 1

🧩 Step 2: Install Komorebi + WHKD

winget install LGUG2Z.komorebi
winget install LGUG2Z.whkd

🔁 Step 3: Restart Terminal

After installation, close and reopen your terminal. Then run:

komorebic quickstart

💾 Step 4: Install YASB

    Option A – GitHub:
    Download YASB v1.7.6

    Option B – Winget:

winget install --id AmN.yasb

🖋 Step 5: Edit Configuration

    Clone this repo:

git clone https://github.com/qarzia/Windows-Setup-Configuration-Files/tree/main/Yasb.Komorobi
cd Yasb.Komorobi

Replace your yasb.yaml with the one in the config/ folder:

    Or open it with VS Code:

    code .\config\yasb_config.yaml

Start Komorebi:

    komorebic start --whkd

📁 Files

    config/yasb_config.yaml – Full YAML config for YASB

    config/komorebi.json – [optional, add yours here]

🎨 Font Recommendation

Install a Nerd Font from: https://www.nerdfonts.com/font-downloads
Recommended: JetBrainsMono Nerd Font
📸 Screenshot
![My-Yasb-Bar-Screenshot](https://github.com/user-attachments/assets/e931a3fc-b56b-45c3-ab8e-b04cb3c319b5)

https://github.com/qarzia/Windows-Setup-Configuration-Files/blob/main/Yasb.Komorobi/Screenshots/My-Yasb-Bar-Screenshot.png


🧼 Optional Apps Used

    Obsidian

    GitHub Desktop

    Discord

    Spotify

    Firefox

    Windows Terminal

🙏 Credits

    Komorebi by LGUG2Z

    YASB by amnweb

    Huge thanks to Diiv for tutorials and inspiration!
