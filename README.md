# MY-NAS

## This project

My First ansible project, so i am rebuild my home made nas server and makeing it automaited 
using 
------------
## How to run command
Use the example inventories.yml file
`mv inventories/inventories.yml.example  inventories/inventories.yml`

add the ip address or hostname of the server using

and add your userinfo vars/useraccounts.yml.example to vars/useraccounts.yml

Note!: to set a password for the user 
    1. install whois (sudo apt-get install whois)
    2. mkpasswd --method=sha-512

Run this command to start the process `ansible-playbook playbook/nas.yml`


## Each Ansible Role does
1. Base basic install of os and setup
     1. Running update on OS is fully up to date
     2. Installing ntp
     3. Configuaring ntp time server (max 5)
2. Openmediavault setup
     1. Get openmediavault repo info 
     2. Get openmediavault-extras repo info
     3. Install openmediavault
     4. Installing extras
         1. openmediavault-fail2ban
         2. openmediavault-route
         3. openmediavault-lvm2
         4. openmediavault-minidlna
         5. openmediavault-clamav
         6. openmediavault-downloader
         7. openmediavault-couchpotato
         8. openmediavault-sickbeard
     5. Configuare openmediavault
     6. Adding users to nas
3. Modifeing Openmediavault interface GUI (Planning on doing)
4. Add extra items for NAS (Planning on doing)
     1. Media converter (Planning on doing)
     2. Dymamic IP updater (Planning on doing)
5. Setting up logrotate
     1. sickbeard
     2. couchpotato
6. Lockdown the NAS server (doing)
     1. Disable root user
     2. Enable Firewall
     3. Lock down all ports
     4. Enable ports (Planning on doing)
        1. 80
        2. 443
        3. 22
        4. samba-ports
        5. minidlna-port
        6. sickbeard-port
        7. couchpotato-port