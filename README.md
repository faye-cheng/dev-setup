# Custom Setup for MacOS

## Terminal Shell

### Install iTerm2

`brew cask install iterm2`

### Install VSCode

### Install Oh My Zsh

https://gist.github.com/kevin-smets/8568070
https://www.reddit.com/r/zsh/comments/ciziab/powerlevel10k_configuration_wizard/

### Set theme to powerlevel10k and follow instructions

## Customize terminal prompt

https://vscode.readthedocs.io/en/latest/editor/command-line/

### Install `cowsay`, `fortune`, and `lolcat`

`brew install cowsay`
`brew install fortune`
`sudo gem install lolcat`

### Create custom fortunes

Create a new file, here I'm calling it quotes:

`touch quotes`

Edit the file with quotes separated by "%":

`vim quotes`

After adding content, convert file:

`strfile quotes`

### custom fish_prompt

Custom ascii font: http://www.network-science.de/ascii/

I moved these files to my faye_setup folder, so update it to the quotes path. Edit config.fish file in `~/.config/fish/config.fish`.

```
function fish_greeting
  echo
  echo " .          .                        .______"
  echo "(|  |  |___ |\  _.   _    . .   _   () |_. _,        _    /"
  echo " |  |  | |/ |/ /   / \_/|/|/|  |/     /| |/ |  |  | |/   /"
  echo "  \/ \/  |_/|_/\__/\_/  | | |_/|_/   (/   \/|_/ \/|/|_/ o"
  echo "                                                 (|"

  set animal (random choice {turkey,blowfish,default,dragon,small,turtle,elephant,moose,stegosaurus,tux})
end
```
To view all cowsay files, do `cowsay -l`

cowsay files are located in: `/usr/local/Cellar/cowsay/3.04/share/cows`
