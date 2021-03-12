# ccna-v7
packet tracer

**day1.pkt**

Connected one router with 2 switches and connected 2 switches with 4 computer for each switch. And pinged 2 computer from different switches.

**day2.pkt**

Made 2 network 

First, one switch(192.168.1.X) connected with 3 computer  

Second, one switch(192.168.2.X) connected with 3 laptop

Connected two switches with using router

First one with gigabitEthernet 0/0 port and second one with gigabitEthernet 0/1 port

added password to enable mode as well as user of Router(with CLI)
    
      enable secret cisco
      conf t
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
