# flatalias
a CLI tool to automatically create formatted flatpak app launch shortcut commands in BASH, FISH and ZSH usind "alias"

Usage:

- download to your $PATH for example `~/.local/bin` or `~/.bin`
- make it executable `chmod +x flatalias`
- run it

How it works:
1. it lists your installed Flatpak apps
2. From this list it extracts the application IDs and formats it to have no dashes, underlines or capital letters
3. It searches for the formatted appID in your `~/.bashrc`, `~/.config/fish/config.fish` or `~/.zshrc`
4. If its not there, it appens a line like following to the document (append = it skips shell config files you don't use!)

```
alias libreoffice="flatpak run org.libreoffice.LibreOffice"
```
