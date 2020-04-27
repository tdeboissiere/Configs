# Unix configuration

## First you update your system

  `sudo apt-get update && sudo apt-get dist-upgrade`

## Install Google Chrome

  ```
  wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
  sudo sh -c 'echo "deb http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google-chrome.list'
  sudo apt-get update
  sudo apt-get install google-chrome-stable
  ```

## Clean-up System

  ```
  sudo apt-get autoremove
  sudo apt-get autoclean
  ```

## Install Useful apps

  `sudo apt-get install guake redshift synapse baobab hdfview graphviz openssh-server htop vim git gnome-tweak-tool ncdu`


Add redshift and guake to startup app with the Startup Application program

## Install nice wallpaper

http://www.omgubuntu.co.uk/2016/10/amazing-linux-penguin-wallpaper

## Install math fonts to print PDF with formulaes

  `sudo apt-get installfonts-mathjax`



## Install zshell and oh my zsh

  ```
  sudo apt-get install zshell
  chsh -s $(which zsh)
  sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
  ```


## Install gnome shell

`
  sudo apt-get install gnome-shell
`

(choose lightdm rather than gdm3 to avoid UI manager conflicts)

## Allow alt tabbing only across current workspace

  `gsettings set org.gnome.shell.app-switcher current-workspace-only true`

## Install dash to panel for gnome 3

  ```
  sudo apt-get install chrome-gnome-shell 
  sudo apt-get install libproxy1-plugin-networkmanager gnome-shell-extension-system-monitor
  #then go to gnome shell extension website to install required ones
  ```

## Install equinux theme + Paper icons

  ```
  https://github.com/ddnexus/equilux-theme
  https://snwh.org/paper/download
  ```

```
Layan: https://github.com/vinceliuice/Layan-gtk-theme
papirus: https://github.com/PapirusDevelopmentTeam/papirus-icon-theme/#ubuntu-and-derivatives
```

## Arc Extension for gnome

    sudo apt install gnome-shell-extensions gnome-menus gir1.2-gmenu-3.0

## Install Firefox color +  equilux

```
https://addons.mozilla.org/en-US/firefox/addon/firefox-color/?src=search
https://github.com/cj-sv/equilux-firefox
```

## Install zsh plugins

```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
git clone --recursive https://github.com/joel-porquet/zsh-dircolors-solarized ~/.zsh/zsh-dircolors-solarized
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
~/.fzf/install
```

## Configure desktop with tweak tool

Open gnome-tweak-tool and then:

In Extensions, install the gnome shell extensions app, then install: TopIcons Plus, User Theme, Dash to Dock and Dash to Panel

For Dash to Dock, select bottom position and in launchers, untick show open window on preview
For Dash to Panel, select size 32 instead of 48 and choose display on top. In behaviour tag, untick show on preview
For TopIconPlus, set ray alignment to right

In Appearance, select Adapta as theme, Paper for Icons, Shell theme as Adapta


## Add Night Light

- Display => Night light

## Configure terminal


Nice color scheme for terminal

  ```
  sudo apt-get install dconf-cli
  #select monokai dark
  wget -O gogh https://git.io/vQgMr && chmod +x gogh && ./gogh && rm gogh  
  ```

In Edit/Profile Preferences

- Give a name to the profile
- In Colours, untick User colors from system scheme
- In scrolling, untick keystroke and limit scrollback
- In Shortcuts, update ctrl+c and ctrl+v
- Untick sound

Shortcuts:

In Settings/Keyboard/Shortcuts : deactivate the launch new terminal shortcut, create a new one with the following command `gnome-terminal --window --maximize`


## Sound

In Settings/Sound, disable alerts


## Install latex

sudo apt-get install texlive-latex-base
sudo apt-get install texlive-fonts-recommended
sudo apt-get install texlive-fonts-extra
sudo apt-get install texlive-latex-extra

