/interface ethernet set ether1 name=speedy

/interface ethernet set ether2 name=lokal

ip address add address=192.168.1.2/24 interface=speedy

ip address add address=192.168.88.1/24 interface=lokal

/interface pppoe-client add name=pppoe-out1 user=144372800263@telkom.net password=xxxxx interface=speedy service-name=internet disabled=no

/ip route add gateway= 180.246.114.1

/ip dns set servers=8.8.8.8,8.8.4.4 allow-remote-requests=yes

/ip firewall nat add chain=srcnat action=masquerade