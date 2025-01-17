---
page_title: "pritunl_server Resource - terraform-provider-pritunl"
subcategory: ""
description: |-
  The organization resource allows managing information about a particular Pritunl server.
---

# Resource `pritunl_server`

## Schema

### Required

- **name** (String) The name of the server

### Optional

- **allowed_devices** (String) Device types permitted to connect to server.
- **bind_address** (String) Network address for the private network that will be created for clients. This network cannot conflict with any existing local networks
- **block_outside_dns** (Boolean) Block outside DNS on Windows clients.
- **cipher** (String) The cipher for the server
- **debug** (Boolean) Show server debugging information in output.
- **dh_param_bits** (Number) Size of DH parameters
- **dns_mapping** (Boolean) Map the vpn clients ip address to the .vpn domain such as example_user.example_org.vpn This will conflict with the DNS port if systemd-resolve is running.
- **dns_servers** (List of String) Enter list of groups to allow connections from. Names are case sensitive. If empty all groups will able to connect
- **groups** (List of String) Enter list of groups to allow connections from. Names are case sensitive. If empty all groups will able to connect
- **hash** (String) The hash for the server
- **id** (String) The ID of this resource.
- **inactive_timeout** (Number) Disconnects users after the specified number of seconds of inactivity..
- **inter_client** (Boolean) Enable inter-client routing across hosts.
- **ipv6** (Boolean) Enables IPv6 on server, requires IPv6 network interface
- **link_ping_interval** (Number) Time in between pings used when multiple users have the same network link to failover to another user when one network link fails.
- **link_ping_timeout** (Number) Optional, ping timeout used when multiple users have the same network link to failover to another user when one network link fails..
- **max_clients** (Number) Maximum number of clients connected to a server or to each server replica.
- **max_devices** (Number) Maximum number of devices per client connected to a server.
- **mss_fix** (Number) MSS fix value
- **multi_device** (Boolean) Allow users to connect with multiple devices concurrently.
- **network** (String) Network address for the private network that will be created for clients. This network cannot conflict with any existing local networks
- **network_end** (String) Ending network address for the bridged VPN client IP addresses. Must be in the subnet of the server network.
- **network_mode** (String) Maximum number of clients connected to a server or to each server replica.
- **network_start** (String) Starting network address for the bridged VPN client IP addresses. Must be in the subnet of the server network.
- **network_wg** (String) Network address for the private network that will be created for clients. This network cannot conflict with any existing local networks
- **organization_ids** (List of String) The list of attached organizations for the server
- **otp_auth** (Boolean) Enables two-step authentication using Google Authenticator. Verification code is entered as the user password when connecting
- **ping_interval** (Number) Interval to ping client
- **ping_timeout** (Number) Timeout for client ping. Must be greater then ping interval
- **port** (Number) The port for the server
- **port_wg** (Number) Network address for the private network that will be created for clients. This network cannot conflict with any existing local networks
- **pre_connect_msg** (String) Messages that will be shown after connect to the server
- **protocol** (String) The protocol for the server
- **replica_count** (Number) Replicate server across multiple hosts.
- **restrict_routes** (Boolean) Prevent traffic from networks not specified in the servers routes from being tunneled over the vpn.
- **route** (Block List) The list of attached routes for the server (see [below for nested schema](#nestedblock--route))
- **search_domain** (String) DNS search domain for clients. Separate multiple search domains by a comma.
- **status** (String) The status of the server
- **vxlan** (Boolean) Use VXLan for routing client-to-client traffic with replicated servers.

<a id="nestedblock--route"></a>
### Nested Schema for `route`

Required:

- **network** (String) Network address with subnet to route

Optional:

- **comment** (String) Comment for route
- **nat** (Boolean) NAT vpn traffic destined to this network


