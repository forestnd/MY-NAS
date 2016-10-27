# MY-NAS

## This project

My First ansible project, so i am rebuild my home made nas server and makeing it automaited 
using 
------------
## How to run command
Use the example inventories.yml file
`mv inventories/inventories.yml.example  inventories/inventories.yml`

add the ip address or hostname of the server using

Run this command to start the process `ansible-playbook -i inventories/inventory.yml.example playbook/nas.yml`


## Each Ansible Role does
1. Base basic install of os and setup
     1. Switching the DHCP to Static
     2. Configure DNS settings
     3. Running update on OS is fully up to date
     4. Installing ntp
     5. Configuaring ntp time server (max 5)
2. Openmediavault setup (working on)
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
     5. Configuare openmediavault (working on)
     6. Adding users to nas (working on)
3. Modifeing Openmediavault interface (Planning on doing)
4. Add extra items for NAS (Planning on doing)
     1. Media converter (Planning on doing)
     2. Dymamic IP updater (Planning on doing)
 5. Lockdown the NAS server (Planning on doing)
     1. Disable root user (Planning on doing)
     2. Enable Firewall (Planning on doing)
     3. Lock down all ports (Planning on doing)
     4. Enable ports (Planning on doing)
        1. 80
        2. 443
        
 
 
