# SFilter-OpenVPN
This is a script that automatically whitelists people that connect into OpenVPN. (As in the sense that they will be saved forever).  This script will drop the port while still allowing the clients to connect into openVPN therefore preventing any annoying socket flooding.

## Setup
1. Locate your openVPN ```server.conf``` file. This file is commonly found inside ```/etc/openvpn/server/server.conf```.
