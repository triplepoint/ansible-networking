# Intro

This role configures `iptables` such that the host will be suitable for routing
and NAT.

## Requirements

None.

## Role Variables

See the [comment in the default variables file](defaults/main.yml) for information on configuration.

## Dependencies

None.

## Example Playbook

    - hosts: whatever
      roles:
        - triplepoint.networking.gateway_routing_and_nat

## License

MIT
