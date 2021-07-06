# set static ip on ubuntu server using netplan:
```
ubuntu@ubuntu:~$ cat /etc/netplan/50-cloud-init.yaml

network:
    ethernets:
        eth0:
            dhcp4: true
            optional: true
    version: 2

network:
  version: 2
  renderer: networkd
  ethernets:
    eth0:
     dhcp4: no
     addresses: [192.168.0.18/24]
     gateway4: 192.168.0.1
     nameservers:
       addresses: [8.8.8.8,8.8.4.4]
```
After configuring netplan file, use:
```
sudo netplan apply
```
In case you run into some issues execute:
```
sudo netplan --debug apply
```

