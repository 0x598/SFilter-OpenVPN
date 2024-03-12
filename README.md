# SFilter-OpenVPN
This is a script that automatically whitelists people that connect into OpenVPN. (As in the sense that they will be saved forever).  This script will drop the port while still allowing the clients to connect into openVPN therefore preventing any annoying socket flooding.

## Setup
1. Locate your openVPN ```server.conf``` file. This file is commonly found inside ```/etc/openvpn/server/server.conf```**.**
2. Copy and Paste the following lines into the ```server.conf``` file:
**status openvpn-status.log 2**
3. Restart the openVPN client.
**sudo systemctl restart openvpn-server@server.service**

## Recommendations
Locate the ```push``` line in your ```server.conf``` file and replace it with the following line to only allow TUN traffic:
**push "redirect-gateway def1 bypass-dhcp"**
This ensures that only the necessary traffic is allowed through the VPN tunnel, providing a more secure and stable connection.
