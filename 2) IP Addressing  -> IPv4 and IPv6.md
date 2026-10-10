# Think of an IP adress like  Your Home's postel address without it the postman (router) can't deliver your letter (data packet ) to the right house IPv4 is like a 6-digit PIN code -running out globally IPv6    is like a full GPS Coordinate-Virtually Unlimited adress for Every Device  on Earth 

#  IPv4-32-BIT (4octels ) :-
     
   # dotted-decimal notation 
   
      IP = 192.168.1.105
      Subnet = 255.255.255.0
      Gateway = 192.168.1.1
   
   # Private Range-Net Internet routable 
      Class A = 10.0.0.0/0 - 16M host 
      Class B = 172.168.0.0/12 - 1M host 
      Class C :  192.168.0.0/16  - 65K host 
      
# CIDR : /24 = 256 IPS (254 usable ) ./16 = 65,536 IPS 
Smaller Prefix = bigger network 




# IPV6 -128-BIT (B Hex Group)

   # Full Notation
        full:2001:Odb8:85a3:0000::8a2e:0370:7334
   # Compressed (:: = all zeror)
        short : 2001:db8::0000::8a2e:0370:7334
   # Why IPv6 matters to Hackers
        1) 340 undecillion address (never runs out )
        2) Built-in IPsec ( Encryption by design)
        3) No NAT- every device is publicly reachable)
        * Often ignored in firewall -> bypass!

  =>  Attack : IPv6 is often misconfigured  or excluded from firewall rules Attackers use it  to Completely bypass IPv4-only Security bypass IPv4-only Security Controls 

# commands  for  networking  Commands 

 1 )  checking  IP Adress 
  
└─$ ip a                               => show all network interfaces & IP

└─$ ifconfig                           => same (older command)

└─$ hostname -I                        => quick - just show your IP


2) Test connectivity

└─$ ping google.com                    => check if you can reach a host

└─$ ping -c 4 google.com               => send only 4 pings


2) Network Connections

└─$ ss -tulng                          => show open ports & listening services

└─$ netstat -tulng                     => same (older command)


3) DNS lookup

└─$ nslookup google.com                => find IP of a domain

└─$ dig google.com                     => get detailed DNS info


4) Download files

└─$ wget https://example.com/file.zip  => download a file

└─$ curl https://example.com           => fetch web content


























































































