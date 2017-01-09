# Elementary OS configuration

##Download Elementary OS from here: 
##http://sourceforge.net/projects/elementaryos/files/stable/

##First you update your system
sudo apt-get update && sudo apt-get dist-upgrade


##Install Google Chrome
wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
sudo sh -c 'echo "deb http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google-chrome.list'
sudo apt-get update
sudo apt-get install google-chrome-stable


##Clean-up System
sudo apt-get purge midori-granite
sudo apt-get purge noise
sudo apt-get purge software-center
sudo apt-get purge scratch-text-editor
sudo apt-get purge bluez
sudo apt-get purge modemmanager
sudo apt-get autoremove
sudo apt-get autoclean

##Remove some Switchboard Plug's
sudo rm -rf /usr/lib/plugs/GnomeCC/gnomecc-bluetooth.plug
sudo rm -rf /usr/lib/plugs/GnomeCC/gnomecc-wacom.plug

##Install File Compression Libs
sudo apt-get install unace unrar zip unzip xz-utils p7zip-full p7zip-rar sharutils rar uudeview mpack arj cabextract file-roller

##Install Guake Terminal
sudo apt-get install guake

##Install Ubuntu Restricted Extras
sudo apt-get install ubuntu-restricted-extras

##Enable all Startup Applications
cd /etc/xdg/autostart
sudo sed --in-place 's/NoDisplay=true/NoDisplay=false/g' *.desktop

##Install Gimp
sudo add-apt-repository ppa:otto-kesselgulasch/gimp
sudo apt-get update
sudo apt-get install gimp gimp-data gimp-plugin-registry gimp-data-extras

##Install Elementary OS extras
sudo apt-add-repository ppa:versable/elementary-update
sudo apt-get update

sudo apt-get install elementary-desktop elementary-tweaks
sudo apt-get install elementary-dark-theme elementary-plastico-theme elementary-whit-e-theme elementary-harvey-theme
sudo apt-get install elementary-elfaenza-icons elementary-nitrux-icons
sudo apt-get install elementary-plank-themes
sudo apt-get install wingpanel-slim indicator-synapse

##Install Skype
sudo apt-add-repository "deb http://archive.canonical.com/ubuntu/ precise partner"
sudo apt-get update && sudo apt-get install skype


