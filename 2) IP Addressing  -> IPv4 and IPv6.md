Think of an IP adress like  Your Home's postel address without it the postman (router) can't deliver your letter (data packet ) to the right house IPv4 is like a 6-digit PIN code -running out globally IPv6    is like a full GPS Coordinate-Virtually Unlimited adress for Every Device  on Earth 

#  IPv4-32-BIT (4octels ) :-
     
   # dotted-decimal notation 
   
      IP = 192.168.1.105
      Subnet = 255.255.255.0
      Gateway = 192.168.1.1
   
   # Private Range-Net Internet routable 
      Class A = 10.0.0.0/0 - 16M host 
      Class B = 172.168.0.0/12 - 1M host 
      Class C :  192.168.0.0/16  - 65K host 
      
 CIDR : /24 = 256 IPS (254 usable ) ./16 = 65,536 IPS 
Smaller Prefix = bigger network 



# commands for  IPv4
       ip -4 addr                    (Display IPv4 addresses)
       ip -4 route                   (Display IPv4 routing table)
       ping -4 -c 4 google.com       (Test IPv4 connectivity)
        nslookup -type=A google.com   (Find Google's IPv4 address)
     dig A google.com              (Query IPv4 DNS records)
     ip -4 neigh                   (Display IPv4 neighbors)
    traceroute -4 google.com      (Trace IPv4 network route)
     nmap -4 <IPv4-address>        (Scan an IPv4 host)
    ip -4 link show               (Display network interfaces)
    ss -4 -lntup                  (Display IPv4 listening services)



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


  # Commands for IPv6 
       
         ip -6 addr                    (Display IPv6 addresses)
       ip -6 route                   (Display IPv6 routing table)
         ping -6 -c 4 google.com       (Test IPv6 connectivity)
       nslookup -type=AAAA google.com (Find Google's IPv6 address)
      dig AAAA google.com           (Query IPv6 DNS records)
     ip -6 neigh                   (Display IPv6 neighbors)
     traceroute -6 google.com      (Trace IPv6 network route)
     nmap -6 <IPv6-address>        (Scan an IPv6 host)
     ip -6 link show               (Display network interfaces)
     ss -6 -lntup                  (Display IPv6 listening services)
    cat /proc/net/if_inet6        (Display kernel IPv6 interface addresses)



### IPv4 vs IPv6

| Feature              | IPv4                  | IPv6                        |
| -------------------- | --------------------- | --------------------------- |
| Address size         | 32 bits               | 128 bits                    |
| Number of groups     | 4 octets              | 8 groups                    |
| Format               | Decimal               | Hexadecimal                 |
| Separator            | Dot (`.`)             | Colon (`:`)                 |
| Example              | `8.8.8.8`             | `2001:4860:4860::8888`      |
| DNS record           | A                     | AAAA                        |
| Bits per group       | 8 bits                | 16 bits                     |
| Address notation     | Dotted decimal        | Colon-separated hexadecimal |
| Address availability | Limited address space | Vast address space          |





    
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


























































































