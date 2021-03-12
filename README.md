# ccna-v7
packet tracer

**Day 2**

Made 2 network 

First, one switch connected with 3 laptop

Second, one switch connected with 3 computer and one router(as end device)

added password to enable mode as well as user of Router(with CLI)
    
      enable secret cisco
      line console 0
      password cisco
      login
      
added ip address to the Router
     
     conf t
     int giga 0/0
     ip add 192.168.1.10 255.255.255.0

opened port of giga 0/0
    
    int giga 0/0
    no shutdown
