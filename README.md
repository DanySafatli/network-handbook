# WIP_network-handbook

## CompTIA+ Certification  

Entry level certification

## Comptia Network + Objectives N10-006
  
- See PDF
- Navigate to Pearson VUE in For test takers tab (https://home.pearsonvue.com/)
- CompTIA blueprint will list the metadata of the exam
- Not all multiple choice questions
- Passing is 720 and above from scale 100-900

## 1. Network Architecture for CompTIA Network+

- Introducing network devices
- Understanding network services and applications
- Configuring network services and applications
- Understanding WAN technologies
- Installing and terminating network cables and connectors
- Differentiating between common network topologies
- Differentiating between common network infrastructures
- Implementing a network addressing scheme
- Understanding routing concepts and protocols
- Introducing unified communication technologies
- Comparing cloud and virtualization technologies
- Implementing a basic network

## 1.1 - Explain the Functions and Applications of Various Network Devices 

- Core connectivity devices
- Security devices
- Special purpose devices

### Hub
- Works at OSI Layer 1 (Physical)
- Hubs are multiport repeaters
  * Regenerate the signal  
- One big collision domain
- Good for network diagnostics and nothing else

### Switch
- Successor to the bridge
- Works at OSI Layer 2 (Data Link)
  * Can also function at OSI Layer 3 (Network)
- Switches store an in-memory MAC (aka media access control) table and provide dedicated bandwidth to each port (collision domain)

### Router
- Operates at OSI Layer 3 (Network)
- Seperate entire networks
- Modular design (especially Cisco)

### Wireless Acess Point
- Provides IEEE 802.11 connectivity
- Many support Power over Ethernet (PoE)
  * IEEE 802.af specifies 15.4W power
- Wireless LAN controllers
  * Centralized management of many WAPs
  
### Ethernet Domains
- Hub
  * One collision domain
- Switch
  * Four collision domains
- Router
  * Four broadcast and collision domains

### Configuring a Router
- VMWare or Virtualbox will allow for creation of computer and aoppliance instances in software
  * Vyos
  
    `$ show int`   
    `$ config`   
    `# set interfaces ethernet eth0 address 10.0.0.254/24`   
    `# save`   
    `# ping 10.0.0.254`   
    `# clear`
    
  * Ability to use tab completion with various CLI's
  * NOTE - Always ensure that you save configuration changes. A common beginner's mistake is making configurations and not saving the changes
  
### Security Devices
- Firewall
  * Exist as software or hardware varieties
  * Selectively allow or block network traffic
    - IP addresses, port numbers - packet-filtering firewall
  * Stateful packet inspection - Identifies sessions and can enforce rules on high level applications and services
  * Serves as a gatekeeper
- Intrusion Detection
  * Intrusion Detection System (IDS) - Passive detection of network traffics
    - Also called NIDS
  * Host-Based IDS (HIDS) - Protects local computer (Tripwire)
  * Intrusion Prevention System (IPS) - Active prevention of network attacks
  * Threat detection often involves signatures and anomolies
- Proxy/Cotent Filter
  * Forward proxy: Hides internal computers IP addresses from the internet
  * Reverse proxy: Publishes internal applications to the internet
  * Proxy provides security and sometimes content caching
  * Content filters use a subscription service (WebSense) to classify web content
  * Generally network devices often combine different but related functions as a all in one operation
- Remote Access and Performance Devices
  * Analog Modem
    - Modulate digital signals to anaolg for transmission over phone lines
    - Receiving modem demodulates analog to digital
    - Modems can have a purpose today
      * Special-purpose equipment that already uses a modem to send small amounts of data
      * "If it ain't broke, don't fix it"    
  * VPN Concentrator
    - Provides dedicated hardware circuitry to host virtual private network (VPN) connections
    - VPN protocols (tunneling and encryption) can be resource intensive
    - Server software can provide VPN services, with decreased cost but also decreased performance and scale
  * Load Balancer
    - Distributes incoming network traffic across multiple nodes
    - Load balancing gives users a faster experience
    - Load balancing is a way of providing high availability (HA)
  * Packet Shaper
    - Prioritize network traffic based upon your business rules
    - Ensures that certain types of traffic always have adequate bandwidth
    - Also ensures that low-priority traffic gets squashed to avoid DoS
    
### Load Balancing in Action Demonstration
  `C:\> ping -4 www.google.com`   
  `C:\> nslookup www.google.com`   
- We use nslookup to query Domain Name System (DNS) servers for informational or troubleshooting purposes
  
### Network Applicances with GUI Demonstration
- Web graphical interfaces (GUIs) are populare because you can get to them from almost anywhere, provided you have a web browser

### The Rack Unit
- Most enterprise servers come as rack mounted appliances
- Mount to rack by rails and "ears"
  * 1U standard is 1.75 inches or 44mm
  * Average rack is 42U or 19 inches wide (483mm)
  
## 1.1.Z - Appendix

### Useful Links
- Understanding Network Hubs -> (http://www.techiwarehouse.com/engine/5ea76190/Understading-Networking-Hubs)
- Network Bridges -> (http://compnetworking.about.com/cs/internetworking/g/bldef_bridge.htm)
- Network Switch -> (https://en.wikipedia.org/wiki/Network_switch)
- Difference Between Hubs, Switches, and Routers -> (http://www.webopedia.com/DidYouKnow/Hardware_Software/router_switch_hub.asp)
- How Does a Network Switch Work? -> (http://www.cisco.com/cisco/web/solutions/small_business/resource_center/articles/connect_employees_and_offices/how_does_a_network_switch_work/index.html)
- Networking Basics - What You Need to Know -> (http://www.cisco.com/cisco/web/solutions/small_business/resource_center/articles/connect_employees_and_offices/networking_basics/index.html)
- Router (Computing) -> (https://en.wikipedia.org/wiki/Router_%28computing%29)
- Router Hardware 101 -> (http://lifehacker.com/5830886/know-your-network-lesson-1-router-hardware-101)
- Understanding Routing -> (http://www.enterprisenetworkingplanet.com/netsp/article.php/3607381/Networking-101-Understanding-Routing.htm)
- Wireless Access Point (https://en.wikipedia.org/wiki/Wireless_access_point)
- Access Point, Wireless (http://compnetworking.about.com/cs/wireless/g/bldef_ap.htm)
- Configuring a Wireless Access Point (http://www.dummies.com/how-to/content/configuring-a-wireless-access-point.html)
- Power over Ethernet (PoE) -> (https://en.wikipedia.org/wiki/Power_over_Ethernet)
- PoE Explained -> (http://www.veracityglobal.com/resources/articles-and-white-papers/poe-explained-part-1.aspx)
- Piet Mondrian -> (http://www.theartstory.org/artist-mondrian-piet.htm)
- Collision Domain -> (https://en.wikipedia.org/wiki/Collision_domain)
- Broadcast Domain -> (https://en.wikipedia.org/wiki/Broadcast_domain)
- Collision Domains vs. Broadcast Domains -> (http://ciscoskills.net/2011/03/30/collision-domains-vs-broadcast-domains/)
- Collision & Broadcast Domains -> (http://study-ccna.com/collision-broadcast-domain)
- VMware Workstation -> (http://www.vmware.com/products/workstation)
- VMware Solution Exchange (Virtual Appliances) -> (https://solutionexchange.vmware.com/store)
- Oracle VM VirtualBox -> (https://www.virtualbox.org/)
- VyOS Virtual Router -> (http://vyos.net/wiki/Main_Page)
- Firewall (Computing) -> (https://en.wikipedia.org/wiki/Firewall_(computing))
- Stateful Firewall -> (https://en.wikipedia.org/wiki/Stateful_firewall)
- What is Stateful Inspection? -> (http://www.webopedia.com/TERM/S/stateful_inspection.html)
- HIDS/NIDS -> (http://searchsecurity.techtarget.com/definition/HIDS-NIDS)
- HIDS -> (https://en.wikipedia.org/wiki/Host-based_intrusion_detection_system)
- NIDS -> (https://en.wikipedia.org/wiki/Intrusion_detection_system)
- IPS -> (https://en.wikipedia.org/wiki/Intrusion_prevention_system)
- Tripwire HIDS -> (http://www.tripwire.com/)
- Proxy Server -> (https://en.wikipedia.org/wiki/Proxy_server)
- Content Control Software -> (https://en.wikipedia.org/wiki/Content-control_software)
- Websense Content Filter Appliance -> (https://www.websense.com/content/v-series-appliances.aspx)
- Using the PING Command -> (https://technet.microsoft.com/en-us/library/cc737478(v=ws.10).aspx)
- Using NSLOOKUP -> (https://support.microsoft.com/en-us/kb/200525)
- Traffic Shaping -> (https://en.wikipedia.org/wiki/Traffic_shaping)
- Blue Coat Traffic Shapers -> (https://www.bluecoat.com/products/packetshaper)
- Load Balancer -> (https://en.wikipedia.org/wiki/Load_balancing_(computing))
- F5 Networks Load Balancers -> (https://f5.com/glossary/load-balancer)
- Meaning of 'RTFM' -> (http://www.internetslang.com/RTFM-meaning-definition.asp)
- Rack Unit -> (https://en.wikipedia.org/wiki/Rack_unit)

## 1.2 - Compare and Contrast the Use of Networking Services and Applications

### Study Alerts for Exam
- Know your basic vocabulary (especially VPN protocols)
- Apply when web services or UC is appropriate

### Understanding VPN Services
- Purpose of VPN
  * Provides remote access to external employees
  * Cheaper to setup and maintain than a leased line
  * Advantages: 
    - Cost, scalability
  * Disadvantages:
    - User must initiate a VPN connection
    - Performance can be poor
- VPN Deployment Types
  * Site to site
    - Site to site VPNs are used to connect on premise network to a cloud service such as Microsoft Azure
  * Host to site
  * Host to host
- VPN Encapsulation
- VPN Protocols
  * PPP: Layer 2 protocol with a long history
  * PPTP: Older, Microsoft centric tunneling protocol (TCP 1723)
    - Uses generic routing encapsulation (GRE IP Protocol value 47) for tunnel and MPPE (microsoft point to point encryption) for encryption
  * L2TP: Combination of PPTP and L2TP (TCP 1701)
    - Uses Internet protocol security (IPSec) and IKE encryption
  * IPSec: Can be used with IKE to create VPN tunnels (UDP 500)
    - Can break NAT (network address translation) because in tunnel mode sue to IP header encryption
  * SSL VPN: VPN by using SSL/TLS (TCP 443)
- Radius Components
  * aka Remote and User Dial In User Service
  * AAA protocol (Authentication, Authorization, Accounting)
- AAA Differences
  * RADIUS
    - Vendor neutral
    - Uses UDP (best effort)
    - Encrypts only payload
    - Combines authentication and authroization 
    - Pros: Interoperability and performance
  * TACASS+
    - Cisco proprietary
    - TCP (ensured delivery)
    - Encrypts entire session
    - Isolates the "three A's"
    - Pros: Security and flexibility
    - Cisco's Identity Services (ISE) supports RADIUS but not TACACS+

### Web Serveices Basics
- Development methods to allow Web Applications to communicate with each other
- Uses standard protocols (Web ptorocols: HTTP, HTTPS, XML, SOAP)
- As a network administrator, you may need to manage firewall exceptions for Web Services (but you shouldn't have to)
- Example: LAMP Web application exchanging data with a Windows Server IIS/ASP.NET Web application

### Unified Communications Basics
- Suite of real time communications technologies
- IP telephony (IPT) and voice over IP (VOIP)
- Presence
- Instant Messaging
- Web conferencing/collaboration
- Voice mail, etc. from desktop or mobile device

## 1.2.Z - Appendix

### Useful Links
- Virtual Private Network -> (https://en.wikipedia.org/wiki/Virtual_private_network)
- VPNs and VPN Technologies -> (http://www.ciscopress.com/articles/article.asp?p=24833)
- Types of VPN Access -> (http://www.orbit-computer-solutions.com/Types-of-VPN-Access.php)
- Site-to-Site VPN -> (http://computer.howstuffworks.com/vpn4.htm)
- Remote Access VPN -> (http://computer.howstuffworks.com/vpn3.htm)
- Host Your Own Private VPN -> (http://www.instructables.com/id/Host-Your-Own-Virtual-Private-Network-VPN-with-O/)
- LogMeIn Hamachi VPN -> (https://secure.logmein.com/products/hamachi/)
- Configure Site-to-Site VPN with Microsoft Azure -> (https://msdn.microsoft.com/en-us/library/azure/dn133795.aspx)
- Encryption and Security Protocols in a VPN -> (http://computer.howstuffworks.com/vpn7.htm)
- Understanding VPN Tunneling -> (http://www.enterprisenetworkingplanet.com/netsp/article.php/3624566/Networking-101-Understanding-Tunneling.htm)
- VPN Tunneling Protocols -> (https://technet.microsoft.com/en-us/library/cc771298(v=ws.10).aspx)
- VPN Tunneling -> (http://compnetworking.about.com/od/vpn/a/vpn_tunneling.htm)
- Configure a Firewall for VPN Traffic -> (https://technet.microsoft.com/en-us/library/dd458955(v=ws.10).aspx)
- What Ports are Used in a VPN? -> (http://kb.juniper.net/InfoCenter/index?page=content&id=KB5671)
- NAT Compatibility Requirements -> (https://www.ietf.org/rfc/rfc3715.txt)
- How Does NAT-T Work with IPSec? -> (https://supportforums.cisco.com/document/64281/how-does-nat-t-work-ipsec)
- Why SSL VPN? -> (https://openvpn.net/index.php/open-source/339-why-ssl-vpn.html)
- Microsoft SSTP Protocol -> (https://technet.microsoft.com/en-us/magazine/2007.06.cableguy.aspx)
- RADIUS Protocol and Components (https://technet.microsoft.com/en-us/library/cc726017(v=ws.10).aspx)
- RADIUS vs. TACACS+ -> (http://www.networkworld.com/article/2838882/radius-versus-tacacs.html)
- TACACS+ and RADIUS Comparison -> (http://www.cisco.com/c/en/us/support/docs/security-vpn/remote-authentication-dial-user-service-radius/13838-10.html)
- IPv4 Address Blocks Reserved for Documentation -> (https://tools.ietf.org/html/rfc5737)
- Using the IPCONFIG Command -> (https://support.microsoft.com/en-us/kb/314850)
- Introduction to Web Services -> (http://www.w3schools.com/webservices/ws_intro.asp)
- Web Service -> (https://en.wikipedia.org/wiki/Web_service)
- What is DevOps? -> (http://blog.pluralsight.com/what-is-devops)
- What is Unified Communications? -> (http://voip.about.com/od/unifiedcommunications/a/UnifiedComm.htm)
- UC Architecture Basics -> (http://www.cisco.com/c/en/us/td/docs/voice_ip_comm/uc_system/UC6-0-1/system_description/SDIPC.html)
- Session Initiation Protocol (SIP) -> (https://en.wikipedia.org/wiki/Session_Initiation_Protocol)
- Microsoft Lync/Skype for Business -> (http://products.office.com/en-us/lync/lync-2013-video-conferencing-meeting-software)
- Cisco UC Products and Services -> (http://www.cisco.com/c/en/us/products/unified-communications/index.html)
- DirectAccess Always-on VPN -> (https://technet.microsoft.com/en-us/windows/directaccess.aspx)

## 1.3 Configuring Network Services and Applications

### Study Alerts for Exam
- Understand the Basic concepts of DNS, DHCP, NAT
- Recognize when to use relevant command line tools (ipconfig, ifconfig)

### DHCP
- aka Dynamic Host Configuration Protocol
  * RFC 1531
  * UDP port 67 (server); port 68 (client)
- Many devices need statically assigned IPv4 addresses
  * Servers, access points, printers, switches and routers
- Request for Commants (RFC) documents are published by the Internet Engineering Task Force (IETF)
- Method for automating client IPv4 Address assignment

### DNS
- aka Domain Name System
- Distributed database of hostname to IP address mappings
- Defined in RFC 1035
- UDP, TCP port 53
- Records (A, AAAA, MX, CNAME, PTR)
- Dynamic DNS
- DHCP Integration

### DNS Troubleshooting Skills
- Windows
  * ipconfig
  * nslookup
  * dig
- Linux
  * ifconfig
  * nslookup
  * dig

### Proxy, Address Translation, and Port Forwarding
- Forward and Reverse Proxies
  * Proxies provide security and possibly caching and/or content filtering
  
### IPV4 Address Exhaustion
- IPv4 address space is 32 bits = 4.2billion addresses
- IPv6  address gives us 128 bits, almost unlimited amount
- RFC 1883 codified IPv6 in 1996, will be a long time before tranisitioning permanently

### Network Address Translation (NAT)
- Nat: one to one, one to many
- Dynamic NAT: Sharing multiple public IPs
- PAT - Port mapping or port forwarding
- DNAT: Also called port forwarding; used to publish private IPs to public internet
- SNAT: Source, static, stateful, secure

## 1.3 - Appendix

### Useful Links
- Microsoft Visio 2013 Trial -> (http://www.microsoft.com/en-us/evalcenter/evaluate-visio-professional-2013)
- What is a SOHO Network? -> (http://www.dsl.com/faqs/what-is-a-soho-network/)
- RFC 1918 (Private IPv4 Addresses) -> (https://tools.ietf.org/html/rfc1918)
- RFC 3046 (DHCP Relay Agent) -> (https://tools.ietf.org/html/rfc3046)
- APIPA - Automatic Private IP Addressing -> (http://compnetworking.about.com/cs/protocolsdhcp/g/bldef_apipa.htm)
- Dynamic Host Configuration Protocol -> (https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol)
- DHCP Overview -> (https://technet.microsoft.com/en-us/library/cc731166.aspx)
- IPCONFIG -> (http://ss64.com/nt/ipconfig.html)
- IFCONFIG -> (http://linux.die.net/man/8/ifconfig)
- NSLOOKUP -> (https://support.microsoft.com/en-us/kb/200525)
- DIG -> (https://www.madboa.com/geek/dig/)
- Domain Name System -> (https://en.wikipedia.org/wiki/Domain_Name_System)
- Root Name Server -> (https://en.wikipedia.org/wiki/Root_name_server)
- RFC 2663: NAT -> (https://tools.ietf.org/html/rfc2663)
- Forward Proxy vs. Reverse Proxy -> (http://www.jscape.com/blog/bid/87783/Forward-Proxy-vs-Reverse-Proxy)
- Port Forwarding -> (https://en.wikipedia.org/wiki/Port_forwarding)
- IPv4 Address Exhaustion -> (https://en.wikipedia.org/wiki/IPv4_address_exhaustion)
- Did Bill Gates Really Say the 640K Quote? -> (http://www.computerworld.com/article/2534312/operating-systems/the--640k--quote-won-t-go-away----but-did-gates-really-say-it-.html)
- RFC 2460: IPv6 -> (https://tools.ietf.org/html/rfc2460)
- Network Address Translation -> (https://en.wikipedia.org/wiki/Network_address_translation)
- NAT and PAT: What's the Difference? -> (http://blog.boson.com/bid/53313/NAT-and-PAT-What-s-the-Difference)




