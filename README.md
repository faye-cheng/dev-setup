# Faye's Custom Environment Set Up for MacOS

## Terminal Shell

### Install iTerm2

`brew cask install iterm2`

### Install Fish

Install fish shell via Homebrew:

`brew install fish`

Add fish to /etc/shells:

`echo "/usr/local/bin/fish" | sudo tee -a /etc/shells`

Make fish the default shell:

`chsh -s /usr/local/bin/fish`

### Install Oh My Fish

`curl -L https://get.oh-my.fish | fish`

### Set omf theme to bobthefish

`omf install bobthefish`

## Custom terminal prompt

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

Edit config.fish file in `~/.config/fish/config.fish`, make sure fortune is calling the custom quote folder you created:

```
function fish_greeting
  set animal (random choice {default,dragon,small,turtle,elephant,moose,stegosaurus,tux})
  fortune quotes | cowsay -f $animal | lolcat
end
```

To view all cowsay files, do `cowsay -l`

cowsay files are located in: `/usr/local/Cellar/cowsay/3.04/share/cows`
