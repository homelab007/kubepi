# Pi Setup

## Enable SSH on a headless Rpi

Once the image is on SD card place file called ssh in to the boot folder. This will enable ssh access at the next boot.

Default password on Raspbian is raspberry
Login is pi@IP_ADDRESS

Flash OS images: https://www.balena.io/etcher/

## Setup Play

```bash

cd ansible
ansible-playbook setup-play.yml
```