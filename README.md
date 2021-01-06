# Custom Setup for MacOS

## Screensaver
### Apple TV Aeriel

https://github.com/JohnCoates/Aerial/releases/\
https://aerialscreensaver.github.io/

## Terminal Shell

### Install iTerm2

`brew cask install iterm2`

### Install VSCode

VSCode Themes
https://vscodethemes.com/

Edit theme in workbench
https://code.visualstudio.com/docs/getstarted/settings

Seti Black
https://vscodethemes.com/e/bobsparadox.seti-black

Custom User Settings:
```{
    "workbench.colorTheme": "Seti Black",
    "editor.wordWrap": "on",
    "workbench.colorCustomizations": {
      // sidebar
        "sideBar.background": "#202020",
        "activityBar.background": "#202020",
        "activityBar.activeBorder": "#6fc4fc",
        "activityBarBadge.background": "#ff8f7b",
      // icons
        "activityBar.inactiveForeground": "#f3e5e5",
        "activityBar.foreground": "#f7d168",
      // tabs
        "tab.activeBackground": "#202020",
        "tab.activeBorder": "#51d698",
        "tab.border": "#000000",
        "tab.inactiveBackground": "#202020",

      // editor
        "editor.background": "#111010"
      },
      "editor.fontSize": 11
}
```

### Enable vscode shortcut from terminal

https://kevgriffin.com/how-to-run-visual-studio-code-from-zsh-on-mac-osx/

`code () { VSCODE_CWD="$PWD" open -n -b "com.microsoft.VSCode" --args $* ;}` in .zshrc file

### Install Oh My Zsh

https://gist.github.com/kevin-smets/8568070
https://www.reddit.com/r/zsh/comments/ciziab/powerlevel10k_configuration_wizard/

### Set theme to powerlevel10k and follow instructions

For Powerlevel10k run:

git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k
Then edit your ~/.zshrc and set ZSH_THEME="powerlevel10k/powerlevel10k". Once you do so, when you start a new terminal session, the Powerlevel10 configure wizard will be launched to set your prompt, beware, there are many many options!

If you want to trigger the configuration wizard immediately, simply run p10k configure to discover all options, which are plentiful.

### Other themes
https://github.com/Powerlevel9k/powerlevel9k/wiki/Show-Off-Your-Config

