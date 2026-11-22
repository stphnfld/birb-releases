# Birb releases

Windows installers for **Birb**, a Discord bot for Dota 2 in-house leagues: game nights, balanced or drafted teams, ratings, betting, giveaways, team seasons and more.

This repository only holds release builds. Birb checks here for updates and installs them itself.

## Install

1. Open the [latest release](https://github.com/stphnfld/birb-releases/releases/latest) and download **Birb-Setup-x.y.z.exe** from *Assets*.
2. Run it. If Windows shows *"Windows protected your PC"*, click **More info → Run anyway**. Birb isn't code-signed yet, so new versions show this for a while.
3. It installs just for you, with no admin rights needed, and opens Birb's setup window. Paste your Discord bot's token, add the bot to your server, and you're done.

Birb then lives in the bird icon by the clock. Your settings and league data are kept in `%LOCALAPPDATA%\Birb`, and updates and uninstalls never touch them.

## Check a download

Each installer has a `.sha256` file next to it. Birb's updater checks it automatically. To check by hand, in PowerShell:

```powershell
Get-FileHash -Algorithm SHA256 .\Birb-Setup-0.3.1.exe
```

The hash should match the one in `Birb-Setup-0.3.1.exe.sha256`.
