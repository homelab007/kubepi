# Pi Setup

## Enable SSH on a headless Rpi

Once the image is on SD card place file called ssh in to the boot folder. This will enable ssh access at the next boot.

- Login: ```pi@IP_ADDRESS```

- Default password on Raspbian: ```raspberry```

- Tool to Flash OS images: [Etcher](https://www.balena.io/etcher/)

## Setup Play

- Find Raspberry Pi IP addresses on your network

    sudo nmap -sF  192.168.0.1/24

- Update inventory file with Raspberry Pi addresses

- Update mac_mapping in ./inventory/group_vars/all/mac_mapping.yml with Raspberry Pi mac addresses
  - Optionally change hostnames
  - Optionally change IP addresses to match your network range

- Run play

    cd ansible
    ansible-playbook setup-play.yml

- Update inventory with new ip addresses