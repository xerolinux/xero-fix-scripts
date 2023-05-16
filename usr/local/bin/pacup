#!/bin/bash

echo
echo "#################################"
echo "  XeroLinux Pacman.conf Updater  "
echo "#################################"
echo
# Check if pacman.conf.old file exists in /etc/
if [ -f "/etc/pacman.conf.old" ]; then
    echo "Deleting existing pacman.conf.old file..."
    sudo rm /etc/pacman.conf.old
fi
sleep 3
# Rename pacman.conf to pacman.conf.old
if [ -f "/etc/pacman.conf" ]; then
    echo "Renaming pacman.conf to pacman.conf.old..."
    sudo mv /etc/pacman.conf /etc/pacman.conf.old
fi
sleep 3
# Grab new pacman.conf from GitHub repository
echo "Downloading new pacman.conf..."
sudo wget -O /etc/pacman.conf https://raw.githubusercontent.com/xerolinux/xero-fixes/main/conf/pacman.conf
echo
echo "#######################################################################"
echo "  All Done ! If all went well you should be able to update no issues.  "
echo "#######################################################################"
sleep 6
