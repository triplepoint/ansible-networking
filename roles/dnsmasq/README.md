# Intro

Set up and install `dnsmasq`, to handle DHCP and DNS.

## Requirements

None.

## Role Variables

See the [comment in the default variables file](defaults/main.yml) for information on configuration.

Note that not all the bells and whistles of `dnsmasq` are configurable in this role.

Also, see the [dnsmasq config documentation](http://thekelleys.org.uk/gitweb/?p=dnsmasq.git;a=blob_plain;f=dnsmasq.conf.example;hb=HEAD) for more information on dnsmasq configuration details.

## Dependencies

None.

## Example Playbook

    - hosts: whatever
      roles:
        - triplepoint.networking.dnsmasq

## License

MIT
