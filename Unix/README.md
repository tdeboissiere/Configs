# Unix configuration

##First you update your system
sudo apt-get update && sudo apt-get dist-upgrade

##Install Google Chrome
wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
sudo sh -c 'echo "deb http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google-chrome.list'
sudo apt-get update
sudo apt-get install google-chrome-stable

##Clean-up System
sudo apt-get autoremove
sudo apt-get autoclean

##Install Useful apps
sudo apt-get install guake redshift synapse baobab

## Install Sublime Text 3 (see website for .deb package)

https://www.sublimetext.com/3


## Install zshell and oh my zsh

sudo apt-get install zshell
chsh -s $(which zsh)
sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"


## Install gnome shell

sudo apt-get install gnome-shell
(choose lightdm rather than gdm3 to avoid UI manager conflicts)

## Launch terminal as a maximized terminal

Edit keyboard shortcut (custom shortcut) with the command:
gnome-terminal --window --maximize

## Nice color scheme for terminal

sudo apt-get install dconf-cli
# select monokai
wget -O xt https://git.io/vKOB6 && chmod +x xt && ./xt && rm xt


## Allow alt tabbing only across current workspace
gsettings set org.gnome.shell.app-switcher current-workspace-only true