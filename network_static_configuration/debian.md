Edit those lines in `/etc/network/interfaces`: 

```
# The primary network interface

auto ens18
iface ens18  inet static
        address 192.168.1.10
        netmask 255.255.255.0
        gateway 192.168.1.1
        dns-nameservers 192.168.1.1

```
