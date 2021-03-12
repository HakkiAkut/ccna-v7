# ccna-v7
packet tracer

**day1.pkt**

Connected one router with 2 switches and connected 2 switches with 4 computer for each switch. And pinged 2 computer from different switches.

**day2.pkt**

Made 2 network 

First, one switch(192.168.1.X) connected with 3 computer  

Second, one switch(192.168.2.X) connected with 3 laptop

Added ip and gateways to the end devices.

Connected two switches with using router

First one with gigabitEthernet 0/0 port and second one with gigabitEthernet 0/1 port

added name(as Router1)  password to enable mode as well as user of Router(with CLI)
    
      enable secret cisco
      conf t
      hostname Router1
      line console 0
      password cisco
      login
      
added ip address to the Router
     
     conf t
     int gigabitEthernet 0/0
     ip add 192.168.1.10 255.255.255.0

opened port of gigabitEthernet 0/0
    
    int gigabitEthernet 0/0
    no shutdown
    
added ip address to the Router
     
     conf t
     int gigabitEthernet 0/1
     ip add 192.168.2.10 255.255.255.0

opened port of gigabitEthernet 0/1
    
    int gigabitEthernet 0/1
    no shutdown
    
Configuring telnet, only 5 end devices can connect each time and added password

    line vty 0 4
    password cisco
    login

Opened password-encryption service
    
    service password-encryption
    
Switch Configuration, new name added to first switch(as SW1)

    enable
    conf t
    hostname SW1
    
Added password to enable mode and user
    
    enable secret cisco
    line console 0
    password cisco
    login
    
Added telnet
    
    line vty 0 4
    password cisco
    login

Vlan configuration (since switch is layer2 cant add ip so need to do vlan config)

    interface vlan 1
    ip address 192.168.1.100 255.255.255.0
    
Added gateway to vlan

    ip default-gateway 192.168.1.10
    
SSH Configuration to Router(Router1)
    
    ip domain name lab.lab
    crypto key generate rsa
    username admin secret cisco // added to db as user
    username ccna secret ccna  // added another user
    ip ssh version 2
    line vty 0 4
    transport input ssh
    login local
    
for login from end device
    
    ssh -l admin 192.168.1.10 
    
