Complete Setup Guide: Google Drive + rclone + Silent Auto-Mount on Windows

(Using remote name: gdrive)
1️⃣ Install rclone

    Download rclone for Windows: https://rclone.org/downloads/

    Extract or install, e.g., C:\rclone

    (Optional) Add rclone folder to your system PATH

2️⃣ Configure rclone for Google Drive

    Open Command Prompt (Win + R, type cmd, Enter).

    Run:

rclone config

    Follow the prompts:

n) New remote
name> gdrive
Storage> drive
client_id> [press Enter]
client_secret> [press Enter]
scope> 1 (Full access)
root_folder_id> [press Enter]
service_account_file> [press Enter]
Edit advanced config? (y/n) n
Use auto config? (y/n) y

    Authorize rclone in the browser window that opens.

    After authorization, configuration is done.

3️⃣ Create a Scripts Folder

Make a folder for scripts without using your username, for example:

C:\rclone-scripts

4️⃣ Create the Mount Batch File

    Open Notepad.

    Paste:

@echo off
start "" rclone mount gdrive: X: --vfs-cache-mode writes --network-mode

    Replace X: with your desired drive letter.

    Save as:

C:\rclone-scripts\mount_gdrive.bat

5️⃣ Create the VBScript for Silent Launch

    Open Notepad.

    Paste:

Set WshShell = CreateObject("WScript.Shell")
WshShell.Run chr(34) & "C:\rclone-scripts\mount_gdrive.bat" & chr(34), 0
Set WshShell = Nothing

    Save as:

C:\rclone-scripts\mount_gdrive_silent.vbs

6️⃣ Create a Scheduled Task to Run at Login

    Open Task Scheduler (Win + S → search).

    Click Create Task.

    General tab:

        Name: Mount Google Drive

        Check Run with highest privileges

        Configure for your Windows version

    Triggers tab:

        New → At log on → select your user → OK

    Actions tab:

        New → Start a program
        Program/script:

wscript.exe

Arguments:

        "C:\rclone-scripts\mount_gdrive_silent.vbs"

    Click OK to save.

7️⃣ Testing

    Restart or log off/on.

    Your Google Drive mounts silently at drive X:.

8️⃣ Unmount

Run in Command Prompt:

taskkill /IM rclone.exe /F

Notes:

    If rclone.exe is not in your PATH, use full path in .bat file, e.g.:

start "" "C:\rclone\rclone.exe" mount gdrive: X: --vfs-cache-mode writes --network-mode

    Replace X: with any free drive letter.