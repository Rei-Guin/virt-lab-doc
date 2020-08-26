# Masamune
---
### I. Reason:
- Provide both support for IPv4 and IPv6, IPv6 also provide more instances than it's counterpart
- Routers or switches can't provide support for IPv6
- Integrate into IPAM server (Aria)
- Logs activities and provide management interface on IP address scope
- If this server were to failed, other machines can still use the default DHCP provided by router or switch
- Provide DNS service using virtual bridge for VMs

### II. Tasks:
- Monitor IP address scope and log activities
- Manipulate both IPv4 and IPv6 for multiple subnets
- Provide DNS service

### III. Development Logs:
- Init server
- Finished setting up Masamune using `dhcp-server`
- Changed to `dnsmasq` to provide both dhcp and dns services

### IV. Error Logs:
- `dnsmasq` failed to start because `dhcpd` still running and the service for `dhcp` is already bind

### V. Fixes:
- Disabled and removed `dhcpd`, then use `dnsmasq` instead

### V. TODO:
- Assign more subnets and reserve static IP address for specific machines. The current config only assigning random addresses to any machines within IP range 192.168.122.10 -> 192.168.122.100 (done)
