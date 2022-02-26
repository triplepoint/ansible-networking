# Intro
Configure the network interfaces on the host.  This more or less amounts to
configuring the contents of `/etc/network/interfaces`

## Requirements
None.

## Role Variables
See the [comment in the default variables file](defaults/main.yml) for information on configuration.

## Dependencies
None.

## Example Playbook
    - hosts: whatever
      roles:
        - triplepoint.network_interfaces

## Role Testing
This role is tested with `molecule`, using `pipenv` to handle dependencies and the Python testing environment.

### Setting Up Your Execution Environment
``` sh
pip install pipenv
```

Once you have `pipenv` installed, you can build the execution virtualenv with:
``` sh
pipenv install --dev
```

### Running Tests
Once you have your environment configured, you can execute `molecule` with:
``` sh
pipenv run molecule test
```

### Regenerating the Lock File
You shouldn't have to do this very often, but if you change the Python package requirements using `pipenv install {some_package}` commands or by editing the `Pipfile` directly, or if you find the build dependencies have fallen out of date, you might need to regenerate the `Pipfile.lock`.
``` sh
pipenv update --dev
```
Be sure and check in the regenerated `Pipfile.lock` when this process is complete.

## License
MIT

# Notes
- see the [Debian Networking documentation on Ethernet Interfaces](https://wiki.debian.org/NetworkConfiguration#Setting_up_an_Ethernet_Interface)
- regarding vlans and bridging - http://blog.frosty-geek.net/2011/02/ubuntu-tagged-vlan-interfaces-and.html
- regarding vlan interfaces - http://manpages.ubuntu.com/manpages/xenial/man5/vlan-interfaces.5.html
