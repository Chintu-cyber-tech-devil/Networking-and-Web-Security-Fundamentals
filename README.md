# Networking-and-Web-Security-Fundamentals
Practical networking and web security fundamentals covering IP addressing, DNS, TCP/UDP, HTTP/HTTPS, and HTTP security headers.


1) Networking , IPS , DNS , and TCP/UOP Protocols

    The foundation of every Cyber attack start here Understand  how the data moves across network-then learn ho wto intercept , redirect and analyse it
   
       1) Network Types 
       2) OSI Model 
       3) IPv4 / IPv6 
       4) subnetting 
       5) DNS Deep Div 
       6) TCP vs UOP 
       7) 3-way Handshake 
       8) Ports & Nmap 

2) What is Network?

    Devices Connected to Communicate and Share Data
   
                    (or)
   
     Who is Connected ? What are they communicating ?How ?And  where is the weakness? 

4) Types :
    1) LPN : Local area Network 
            ( Devices in Same building/home .Your home wi-fi is LAN .Uses Ethernet  (or) wi-fi Low Latency ,high Speed ) 
    2) WAN : Wide Area Network 
             ( Spans Cities (or) countries .The Internet itself is the world's largest WAN-million of LANs joined Via Routers and IPS )  
    3) VPN : Virtual Private Network 
             ( Encrypted Tunnel Over public internet . Hackers anonymize traffic ; defenders secure remote worker with it ) 
    4) OSI : OSI 7-Layer Model 
             ( Standardize how data travels app-to-wire .Each Layer adds/removes a header called encapsulation ) 

             => 7-Layers Model OSI 

             7) Application  =>   HTTP , DNS , FTP , SMTP 
             6) Presentation =>   TLS/SSL , Encoding , JPEG
             5) Session      =>   Session , Auth , NetBIOS 
             4) Transport    =>   TCP , UDP , Ports 
             3) Network      =>   IP , ICMP , Routing 
             2) Data Link    =>   MAC Address , ARP , Switch 
             1) Physical     =>   Cables , Wi-fi signal ,hubs 

 5) knowing which OSI Layer an attack targets tell you exactly which tools to use -Nmap ( L3/4) ,Burp Suits (L7) Wireshark(L2+)  

             

 
