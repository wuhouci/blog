/etc/sysctl.conf

net.ipv4.ip_forward=1

#sysctl -p

#firewall-cmd --add-masquerade --zone-public

#firewall-cmd --query-masquerade

#firewall-cmd --direct --passthrough ipv4 -t nat -A POSTROUTING -s 192.168.*.*/* -j SNAT --to-source *.*.*.*

####

firewall-cmd --add-forward-port=port=3389:proto=tcp:toport=3389:toaddr=192.168.*.*

#firewall-cmd --add-masquerade --zone=public --permanet

####

#nmcli con add type bridge con-name br-ex ifname br-ex autoconnect yes

#nmcli con add type bridge con-name br-in ifname br-in autoconnect yes

#nmcli con show

//#nmcli connection delete ?ifname?

//#nmcli connection delete "~name~"

//#nmcli connection add type bridge-slave con-name ?ifname? autoconnect yes master br-ex

//#firewall-cmd --zone=external --change-interface=?briname?

//#firewall-cmd --zone=internal --change-interface=?briname?

//#firewall-cmd --list-all-zones

//#firewall-cmd --zone=external --add-masquerade

//#firewall-cmd --zone=external --list-all

//#firewall-cmd --direct --passthrough ipv4 -t nat -I POSTROUTING -o br-ex -j MAQQUERADE -s 192.168.*.*/*

//#nmcli conn modify br-in ipv4.addresses 192.168.*.*/* autoconnect yes ipv4.method manual

//#nmcli conn up br-in

//#ip addr

//#firewall-cmd --zone=external --add-forward-port=port=3389:proto=tcp:toport=3389:toaddr=192.168.*.* 

//#firewall-cmd --zone=external --list-forward-ports
