#!/bin/bash
#set -e
echo "#################################"
echo "       Fixing Samba Shares       "
echo "#################################"
sleep 1.5
##Change your username here
read -p "What is your login? It will be used to add this user to smb : " choice
sudo smbpasswd -a $choice
sudo gpasswd -a $USER sambashare
sleep 1.5
cd /etc/samba/ && sudo mv smb.conf smb.conf.orig
cd /etc/samba/ && sudo wget https://raw.githubusercontent.com/xerolinux/xero-fixes/main/conf/smb.conf
sudo mkdir -p /var/lib/samba/usershares
sudo chown root:sambashare /var/lib/samba/usershares
sudo chmod 1770 /var/lib/samba/usershares
sudo systemctl enable --now smb
echo "#################################"
echo "   Done Please Reboot To Apply   "
echo "#################################"
sleep 6
