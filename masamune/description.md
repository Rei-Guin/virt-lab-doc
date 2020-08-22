# Masamune
---
### I. Reason:
- Provide both support for IPv4 and IPv6, IPv6 also provide more instances than it's counterpart
- Routers or switches can't provide support for IPv6
- Integrate into IPAM system
- Logs activities and provide management interface on IP address scope
- If this server were to failed, other machines can still use the default DHCP provided by router or switch

### II. Tasks:
- Monitor IP address scope and log activities
- Manipulate both IPv4 and IPv6 for multiple subnets

### III. Development Logs:
- Init server
- Finished setting up Masamune

### IV. Error Logs:
- N/A

### V. TODO:
- Assign more subnets and reserve static IP address for specific machines. The current config only assigning random addresses to any machines within IP range 192.168.122.10 - 192.168.122.100
