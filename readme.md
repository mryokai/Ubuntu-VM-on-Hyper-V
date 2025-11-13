How to install ubuntu VM on Hyper-V

Run Hyper-V manager

New VM

Follow the steps and use the linux iso

After the VM is created, don't run yet.

Go to Settings and disable SecureBoot

Connect to the VM

sudo apt update && sudo apt upgrade -y

sudo apt install xrdp

sudo vi /etc/xrdp/startwm.sh

Codes to be added in startwm.sh file - 
export DESKTOP_SESSION=ubuntu
export GNOME_SHELL_SESSION_MODE=ubuntu
export XDG_CURRENT_DESKTOP=ubuntu:GNOME


sudo systemctl enable -now xrdp

sudo ufw allow from any to any port 3389 proto tcp
