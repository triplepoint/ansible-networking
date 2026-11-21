# Intro

This role configures `nftables` such that the host will be suitable for routing
and NAT.  It installs the ruleset to `/etc/nftables.conf`, checks it with
`nft --check` before installing it, enables the `nftables` service, and turns on
IPv4 and IPv6 forwarding.

The ruleset bundled with this role (`templates/nftables_config.j2`) is written
for one specific network: apart from the WAN interface, its interface names and
rules are hard-coded.  For any other network, write your own ruleset template
and point `gateway_routing_and_nat_nftables_template` at it.

## Requirements

None.

## Role Variables

- `gateway_routing_and_nat_wan_interface`: the WAN interface name, used by the
  bundled ruleset for NAT and the "outbound traffic" direction.
- `gateway_routing_and_nat_nftables_template`: the template rendered to
  `/etc/nftables.conf`.  Defaults to the bundled ruleset.

See the [comments in the default variables file](defaults/main.yml) for details.

## Dependencies

None.

## Example Playbook

    - hosts: whatever
      roles:
        - triplepoint.networking.gateway_routing_and_nat

## License

MIT
