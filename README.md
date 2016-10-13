# openmediavault-NAS

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
     4. Configuare openmediavault (working on)
 
 
 
