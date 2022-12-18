# ansible-rpi-base

An ansible role to configure base settings for a raspberry pi.

## Requirements

- write Raspberry Pi OS Lite (32-bit) to microSD using Raspberry Pi Imager with following changes to advanced settings
    - [x] enable ssh
    - [x] set username & password
    - [x] configure wireless lan
    - [ ] enable telemetry
- insert the microSD card to the RaspberryPi Zero
- connect via SSH using configured credentials
- setup ssh key authentication if not configured with Raspberry Pi Imager 
    - e.g. `ssh-copy-id -i ~/.ssh/id_ed25519 <username>@<ip_address>`

## Role Variables

See defaults for configurable variables.

## Example

### requirements.yml

    - src: https://github.com/hulkk/ansible-rpi-base
      name: rpi-base

### Playbook

    - hosts: raspberrypi
      roles:
        - rpi-base
