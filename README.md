_Data Center Leaf/Spine topology, VXLAN, MLAG, BGP underlay_

**Configure Apline Hosts**

  sea-dc-host1
  
     docker exec -it clab-dc1-sea-dc-host1 sh
     apk update
     apk add net-tools iproute2 iputils-ping
     ifconfig eth1 10.110.0.101 netmask 255.255.255.0
     route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.110.0.1 dev eth1
     ping -i 30 10.110.0.102
     
  sea-dc-host2
  
     docker exec -it clab-dc1-sea-dc-host2 sh
     apk update
     apk add net-tools iproute2 iputils-ping
     ifconfig eth1 10.130.0.101 netmask 255.255.255.0
     route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.130.0.1 dev eth1
     ping -i 30 10.130.0.102

  sea-dc-host3
  
     docker exec -it clab-dc1-sea-dc-host3 sh
     apk update
     apk add net-tools iproute2 iputils-ping
     ifconfig eth1 10.110.0.101 netmask 255.255.255.0
     route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.110.0.1 dev eth1
     ping -i 30 10.110.0.102

  sea-dc-host4
  
     docker exec -it clab-dc2-sea-dc-host4 sh
     apk update
     apk add net-tools iproute2 iputils-ping
     ifconfig eth1 10.130.0.102 netmask 255.255.255.0
     route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.130.0.1 dev eth1
     ping -i 30 10.140.0.101

  sea-dc-host5
  
     docker exec -it clab-dc1-sea-dc-host5 sh
     apk update
     apk add net-tools iproute2 iputils-ping
     ifconfig eth1 10.120.0.101 netmask 255.255.255.0
     route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.120.0.1 dev eth1
     ping -i 30 10.120.0.102

  sea-dc-host6
  
     docker exec -it clab-dc1-sea-dc-host6 sh
     apk update
     apk add net-tools iproute2 iputils-ping
     ifconfig eth1 10.120.0.102 netmask 255.255.255.0
     route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.120.0.1 dev eth1
     ping -i 30 10.140.0.101

  sea-dc-host7
  
     docker exec -it clab-dc1-sea-dc-host7 sh
     apk update
     apk add net-tools iproute2 iputils-ping
     ifconfig eth1 10.140.0.101 netmask 255.255.255.0
     route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.140.0.1 dev eth1
