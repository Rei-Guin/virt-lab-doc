# Aria
---
### I. Reason:
- As the number of VMs and devices increased, I need a centralized platform to manage IP addresses so Aria is created to serve as an **IPAM** server
- Provide GUI-friendly and easy-to-access browser interface to manage IP addresses, subnets, devices, etc...
- Act as a primary database (MariaDB) that contains network information, secondary database will be created in case of incidents, backups or emergencies

### II. Tasks:
- Monitor status of machines in the network
- Manage IP addresses via browser interface and CLI
- Simplified IP addresses logging and assigning

### III. Development Logs:
- The installation process was straight from https://phpipam.net/news/phpipam-installation-on-centos-7/
- However, the commands `checkmodule` and `semodule_package` were not installed by default so I had a hard time finding which packages do these commands belong to
- Managed to locate `checkpolicy` and `policycoreutils-python` and proceed with creating policy for network pinging
- Had to change `fping` path because the installed path on `Aria` in different from the setting on the browser interface
- Toggle between `enforcing` and `permissive` SE linux modes to test the pinging functions

### IV. Error Logs:
- N/A

### V. Fixes:
- N/A

### V. TODO:
- Change DNS server from google to other DNS server
