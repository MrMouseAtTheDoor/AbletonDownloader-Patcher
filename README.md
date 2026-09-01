<b>English</b> | [Русский](https://github.com/MrMouseAtTheDoor/AbletonDownloader-Patcher/blob/main/README.ru.md)

# AbletonDownloader-Patcher
The easiest and safest way to download and patch Ableton Live.

All editions and versions starting from 9 (9, 10, 11, 12, ...) are supported.  
<br>Works on Windows and Linux (Wine).

This is an open-source implementation of the R2R patch and `R2RLIVE.dll` of Ableton Live, written in Python. Like `R2RLIVE.dll`, this script uses Team R2R's signing key only.

This is not my patcher; I simply compiled the Python script into an exe for easier use and slightly modified the appearance of the downloader. Essentially, this is a fork, but I do not credit the authors because, as I understand it, they no longer wish to be associated with such projects.

## How to use
1. Download the latest version of AbletonDownloader-Patcher: 
2. Extract everything from the archive into one folder
### Downloading Ableton Live
1. Open the `AbletonDownloader.html` file in your browser.
2. Select the required parameters and specify the necessary version of Ableton Live (e.g., 12.4.5, 11.0, 10.0.6, 9.7.7).
3. Click Generate Download Link — the download of the program from the official site will begin.
4. Install Ableton Live  
<br>Windows: extract everything from the archive and run the installer.
### Patching Ableton Live
1. Launch Ableton Live
2. In the authorization window, click "No internet on this computer," then click "Save..." and save the file. This file will open automatically, or you can open it manually. Copy "Your hardware code" from there.
3. Close Ableton Live
4. Open the `config.json` file
5. In the hwid field, paste the copied hardware code
6. If you installed Ableton Live not in the default folder, replace the "auto" value in the file_path field with the path to the Ableton Live executable  
<br>(Replace the single backslash \ in the path with a double backslash \\)  
<br>Example: `"file_path": "C:\\Programs\\Ableton Live 12 Suite\\Program\\Ableton Live 12 Suite.exe",`
7. Specify the required version and edition in the "version" and "edition" fields
8. Save the changes in the file
9. Run `AbletonPatcher.exe`. If "auto" is set in file_path, you will be prompted to choose from the installed versions of Ableton Live. Select the desired one.
10. If everything is correctly specified in `config.json`, Ableton Live will be successfully patched, and a file `Authorize.auz` will be created in the output folder.
11. Launch Ableton Live and drag the `Authorize.auz` file (from the output folder) into the program window.
12. It is recommended to disable automatic updates for Ableton Live:  
<br>Options → Settings → License & Updates → Get Automatic Updates → Never  
<br>Otherwise, after an update, you may need to repeat the patching process.
