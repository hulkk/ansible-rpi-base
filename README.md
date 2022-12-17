# ansible-rpi-base

A brief description of the role goes here.

## Requirements

- write RaspberryPi OS Lite (32-bit) to microSD using Raspberry Pi Imager with following changes to advanced settings
    - [x] enable ssh
    - [x] set username & password
    - [x] configure wireless lan
    - [ ] enable telemetry
- insert the microSD card to the RaspberryPi Zero
- connect via SSH using configured credentials
- setup ssh key authentication if not configured with Raspberry Pi Imager 
    - e.g. `ssh-copy-id -i ~/.ssh/id_ed25519 <username>@<ip_address>`

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }
