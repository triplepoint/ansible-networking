# Intro

Configure the network interfaces on the host. This more or less amounts to
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
        - triplepoint.networking.network_interfaces

## TODOs

- Migrate to netplan, away from ifupdown

## License

MIT

## Notes

- see the [Debian Networking documentation on Ethernet Interfaces](https://wiki.debian.org/NetworkConfiguration#Setting_up_an_Ethernet_Interface)
- regarding vlans and bridging - http://blog.frosty-geek.net/2011/02/ubuntu-tagged-vlan-interfaces-and.html
- regarding vlan interfaces - http://manpages.ubuntu.com/manpages/xenial/man5/vlan-interfaces.5.html
