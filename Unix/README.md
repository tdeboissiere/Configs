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

  `sudo apt-get install guake redshift synapse baobab hdfview graphviz openssh-server htop vim git gnome-tweak-tool`


Add redshift and guake to startup app with the Startup Application program

## Install nice wallpaper

http://www.omgubuntu.co.uk/2016/10/amazing-linux-penguin-wallpaper

## Install math fonts to print PDF with formulaes

  `sudo apt-get installfonts-mathjax`

## Install Sublime Text 3 (see website for .deb package)

  `https://www.sublimetext.com/3`


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

## Launch terminal as a maximized terminal

Edit keyboard shortcut (custom shortcut) with the command:

  `gnome-terminal --window --maximize`

## Nice color scheme for terminal

  ```
  sudo apt-get install dconf-cli
  #select monokai
  wget -O xt https://git.io/vKOB6 && chmod +x xt && ./xt && rm xt
  ```


## Allow alt tabbing only across current workspace

  `gsettings set org.gnome.shell.app-switcher current-workspace-only true`

## Install dash to panel for gnome 3

  ```
  sudo apt-get install chrome-gnome-shell
  #then go to gnome shell extension website to install required ones
  ```

## Install adapta theme and numix icons and moka icons

  ```
  sudo add-apt-repository ppa:numix/ppa
  sudo add-apt-repository ppa:tista/adapta
  sudo add-apt-repository ppa:moka/daily
  sudo apt-get update

  sudo apt-get install moka-icon-theme adapta-gtk-theme numix-gtk-theme numix-icon-theme-circle
  
  # Paper
  sudo add-apt-repository ppa:snwh/pulp
  sudo apt-get update
  sudo apt-get install paper-icon-theme
  sudo apt-get install paper-cursor-theme
  sudo apt-get install paper-gtk-theme
  
  ```
## Configure desktop with tweak tool

Open gnome-tweak-tool and then:

In Extensions, install the gnome shell extensions app, then install: TopIcons Plus, User Theme, Dash to Dock and Dash to Panel

For Dash to Dock, select bottom position and in launchers, untick show open window on preview
For Dash to Panel, select size 32 instead of 48 and choose display on top. In behaviour tag, untick show on preview
For TopIconPlus, set ray alignment to right

In Appearance, select Adapta as theme, Paper for Icons, Shell theme as Adapta


## Install node js > 6

  ```
  curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -
  sudo apt-get install -y nodejs
  ```
