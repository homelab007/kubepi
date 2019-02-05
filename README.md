# Pi Setup

## Enable SSH on a headless Rpi

Once the image is on SD card place file called ssh in to the boot folder. This will enable ssh access at the next boot.

- Login: ```pi@IP_ADDRESS```

- Default password on Raspbian: ```raspberry```

- Tool to Flash OS images: [Etcher](https://www.balena.io/etcher/)

- Pis are connected to local router and network used is 192.168.1.0/24

## Setup Play

- Find Raspberry Pi IP addresses on your network

  ```sudo nmap -sF  192.168.1.1/24```

- Update ```inventory/hosts-dhcp.yml``` file with Raspberry Pi addresses that were dynamical assigned

- Update mac_mapping in ```./inventory/group_vars/all/mac_mapping.yml``` with Raspberry Pi mac addresses
  - Optionally change hostnames
  - Optionally change IP addresses to match your network range

- Run play

  ```cd ansible &&  ansible-playbook -i inventory/hosts-dhcp.yml setup-play.yml```
