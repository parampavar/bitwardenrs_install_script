# bitwardenrs_install_script
Install Script for BitWarden_RS for Ubuntu 20.04 using https://github.com/dani-garcia/bitwarden_rs

Please note this is an unofficial install script and support requests for the install should come here not to https://github.com/dani-garcia/bitwarden_rs

This installs BitWarden_RS on Ubuntu 20.04 with SQLite, configures firewall and enables fail2ban.

Requirements 1GB Ram (perhaps overspec'd for running BitWarden_RS but much less compile will take to long. It already takes quite a while to run the script)

Prerequisites Ubuntu 20.04 Create non root user DNS record created on domain (you can get free domains from freenom.com) pointed to your external IP Ports 80, 443 and 22 opened on your firewall and pointed to the deployment machine.

Install.sh will install the newest version of BitWarden_RS and Bitwarden Web.

If logged in as root add a user using these commands prior to install: $ adduser bitwardenrs $ usermod -a -G sudo bitwardenrs

Switch to bitwardenrs user (script won't run as root) $ su bitwardenrs

Change Directory to bitwardenrs home $ cd ~/

Download the install script from github $ wget https://raw.githubusercontent.com/dinger1986/bitwardenrs_install_script/master/install.sh

Set Script as executable $ chmod +x install.sh

Run script $ ./install.sh

Fill in info as requested as the script runs

Once complete go to https://yourdomain/admin
