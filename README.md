# WIP_network-handbook

## CompTIA+ Certification  

Entry level certification

## Comptia Network + Objectives N10-006
  
- See PDF
- Navigate to Pearson VUE in For test takers tab (https://home.pearsonvue.com/)
- CompTIA blueprint will list the metadata of the exam
- Not all multiple choice questions
- Passing is 720 and above from scale 100-900

## 1. Overview of Network Architecture for CompTIA Network+

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

## 1.3.Z - Appendix

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

## 1.4 Explain the Characteristics and Benefits of Various WAN Technologies

### WAN Basics
- What is LAN?
  * WANs connect networks that are wider range
    - Distance is relative
  * Own LANs and Lease WANs

### WAN Connection Types
  * Dedicated leased line
    - Reserved point to point link
  * Circuit switched connection
    - As needed link (phone call)
  * Packet switched connection
    - Pseudo dedicated virtual links
    
### Dedicated Leased Line Technologies
- Circuits use multiplexing technology to aggregate 64 Kbps channels
- Layer 2 protocols are PPP or Cisco HDLC (PPP is multiprotocol and multilink)
- T1: 24 DS0 channels = 1.544 Mbps (~$200/mo)
- E1: 32 DS0 channels = 2.048 Mbps
- T3: 28 T1s = 44.7 Mbps (~$5-10K/mo)
- E3: 34 Mbps

### SONET and OC Levels
- Synchronous Optical Network (SONET): Layer 1 technology that uses fiber optic cabling
  * Can transmit some Layer 2 encapsulations like Asynchronous Transfer Mode (ATM)
  * ATM required special hardware which costs significantly more
- Uses TDM to support multiple data flows over single fiber
- OC3: Equivalent to 100 TAz @ 155 Mbps (~$20-45K/mo)
- OC12: Equivalent to 4 OC3s @ 622 Mbps
- DWDM (Dense Wavelength Division Multiplexing): Each light Wavelength carries a data stream independantly; more expensive than CWDN
- CWDM (Course Wavelength Divsion Multiplexing); Spectrum broken less granularly than DWDN

### Circuit Switched WAN Technologies
- Circuit Switched Connections
  * Analog Modem
  * ISDN
  * Digital Subscriber Line
  * Broadband Cable
- Analog Modem and ISDN
  * Analog to digital modulation
  * Voice or Data @ 53 Kbps
- Integrated Services Digital Network
  * Voice or data over PTSN
  * B: 64 Kbps x 2 (128 Kbps total)
  * D: 16 Kbps control panel
  * Requires modem and ISDN telephones
- Digital Subscriber Line
  * Digital voice and data over PSTN
  * ASDL is more common
  * Uses PPPoE and IP
- Broadband Cable
  * Data over cable tv coax cabling
  * Generally asymmetric transfers
  * Uses DOCSIS (data over cable service interface specification)
  
### Packet Switched WAN Technologies
- Frame Relay
  * Was the standard for business WANs
  * Operates at OSI Layer 2
  * Permanent or switched virtual circuits (PVCs, SVCs)
  * DTE (Data Terminal Equip): Modem or CSU/DSU on customer's side - terminates the connection
  * DCE (Data COmmunications Equip): On Providers side
- MPLS
  * Microprotocol Label Switching
  * The current WAN standard
  * Single backbone can route Frame, ATM, Metro Ethernet, etc
  * Header functions as OSI Layer 2.5
  * MPLS uses special headers called "labels" to make routing decisions
- Metro Ethernet
  * Used in metropolitan area network (MAN ) environments
  * Can do pure Ethernet, Ethernet over SONET, Ethernet over MPLS

### Wireless WAN Technologies
- Satellite
  * Appropriate for locations that are far way
  * Need satellite dish and line of sight
  * Latency because satellites travel 22K miles high
  * Sensitivity to weather
  * Pay for the data transfer (like smartphones)
- WiMAX
  * Worldwide Interoperability for Microwave Access
  * Up to 45 Mbps downstream / 50km
  * Certain companies are moving away from WiMAX
- Cellular Networks
  * Targeted at smartphones and tablet devices
  * GSM (Global System for Mobile Communications)
  * CDMA (Code Division Multiple Access)
  * 2G: Edge: 135 Kbps downstream
  * 3G: High Speed Packet Access (HSPA+) ~4 Mbps downstream
  * 4G Long Term Evolution (LTE) 50Mbps
  
## 1.4.Z Appendix

### Useful Links
- Difference Between LAN, MAN, and WAN (https://kb.iu.edu/d/agki)
- Verizon Managed WAN Service Level Agreement (SLA) (http://www.verizonenterprise.com/external/service_guide/reg/cp_mwan_sla.pdf)
- Leased Line (https://en.wikipedia.org/wiki/Leased_line)
- Understanding Dedicated Leased Lines vs. Shared Access (http://www.chaffeecountyedc.com/EndUserFiles/33266.pdf)
- Packet vs Circuit Switching (http://bpastudio.csudh.edu/fac/lpress/471/hout/netech/circuitvpacket.htm)
- T-Carrier (https://en.wikipedia.org/wiki/T-carrier)
- E-Carrier (https://en.wikipedia.org/wiki/E-carrier)
- Time-Division Multiplexing (TDM) (https://en.wikipedia.org/wiki/Time-division_multiplexing)
- Point-to-Point Protocol (PPP) (https://en.wikipedia.org/wiki/Point-to-Point_Protocol)
- Use Multilink PPP (http://www.techrepublic.com/blog/data-center/use-multilink-ppp-to-combine-multiple-circuits-into-a-single-circuit-with-a-single-router-interface/)
- Cisco HDLC (https://en.wikipedia.org/wiki/Cisco_HDLC)
- CSU/DSU (https://en.wikipedia.org/wiki/CSU/DSU)
- T1/E1 CSU/DSUs (http://www.adtran.com/web/page/portal/Adtran/group/127)
- Demarcation Point (https://en.wikipedia.org/wiki/Demarcation_point)
- Asynchronous Transfer Mode (ATM) (https://en.wikipedia.org/wiki/Asynchronous_Transfer_Mode)
- A Brief Overview of ATM (http://ccr.sigcomm.org/archive/1995/apr95/ccr-9504-siu.pdf)
- Synchronous Optical Networking (SONET) (https://en.wikipedia.org/wiki/Synchronous_optical_networking)
- Optical Carrier Transmission Rates (https://en.wikipedia.org/wiki/Optical_Carrier_transmission_rates)
- SONET/OC Topology and Cost (https://www.10gea.org/network/sonet-ocx/)
- Wavelength-Division Multiplexing (https://en.wikipedia.org/wiki/Wavelength-division_multiplexing)
- What is Difference Between DWDM and CWDM? (http://www.wisegeek.com/what-is-the-difference-between-dwdm-and-cwdm-optical-technolgies.htm)
- Integrated Services Digital Network (ISDN) (https://en.wikipedia.org/wiki/Integrated_Services_Digital_Network)
- What is ISDN? (http://public.swbell.net/ISDN/overview.html)
- Modem (https://en.wikipedia.org/wiki/Modem)
- Hayes (AT) Command Set (https://en.wikipedia.org/wiki/Hayes_command_set)
- ADSL (https://en.wikipedia.org/wiki/Asymmetric_digital_subscriber_line)
- ADSL Packages (http://www.mweb.co.za/internet-connection/adsl/adsl-packages.aspx)
- Cable Internet Access (https://en.wikipedia.org/wiki/Cable_Internet_access)
- List of Broadband Cable Providers (http://broadbandnow.com/Cable-Providers)
- PPPoE (https://en.wikipedia.org/wiki/Point-to-point_protocol_over_Ethernet)
- DOCSIS Specification (http://docsis.org/)
- Frame Relay (https://en.wikipedia.org/wiki/Frame_Relay)
- Frame Relay Details (http://www.protocols.com/pbook/frame.htm)
- MPLS (https://en.wikipedia.org/wiki/Multiprotocol_Label_Switching)
- MPLS for Dummies (https://www.nanog.org/meetings/nanog49/presentations/Sunday/mpls-nanog49.pdf)
- Metro Ethernet (https://en.wikipedia.org/wiki/Metro_Ethernet)
- Metro Ethernet Forum (MEF) (http://www.metroethernetforum.org/)
- DTE vs. DCE (http://ftp1.digi.com/support/cabling/dte_vs_dce.pdf)
- Satellite Internet Access (https://en.wikipedia.org/wiki/Satellite_Internet_access)
- Hughes Satellite Service (http://www.hughesnet.com/)
- WiMAX (https://en.wikipedia.org/wiki/WiMAX)
- WiMAX Forum (http://www.wimaxforum.org/)
- GSM vs. CDMA: What is the Difference? (http://www.makeuseof.com/tag/gsm-vs-cdma-difference-better/)
- Giz Explains: How Cell Towers Work (http://gizmodo.com/5177322/giz-explains-how-cell-towers-work)
- Ookla Speedtest Mini API (https://www.speedtest.net/mini.php)

## 1.5 Installing and Properly Terminating Various Cable Types and Conenctors using Apropriate Tools

### Study Alerts for Exam
- Recognize Cable and connector form factors
- Associate different cables/connectors with different goals

### Overview
  * Copper cables and connectors
  * Fiber cables and connectors
  * Media converters
  * termination
  * Network Technician Tools
  
### Twisted-Pair Copper Cables
  * Copper conductor
  * Twisting reduces electronic inteference (Cross talk and EMI)
  * Foil shielding: further reduce crosstalk
  * Pinout: Defines meaning of each wire
  
### Twisted Pair Cable Standards
  * Max cable length = 100 M (328 ft); 10 Gbps Ethernet is less
  * Unshielded Twisted Pair (UTP) - Susceptible to EMI
  * Shielded Twisted Pair - Protects against EMI 
  * Twisted Pair Categories
    - CAT 3 = 10 Mbps - Legacy Category
    - CAT 5 = 100 Mbps
    - CAT 5e = 1 Gbps
    - CAT 6/6a = 10 Gbps
    
### Twisted-Pair Wiring Standards
  * 568A and 568B is part of the Electronic Industries Alliance (EIA)/Telecommunications Industry Association (TIA)
  * Network Infrastructure would be compatible with any type provided they follow the standards
  * Cable Types
    - Straight Through Cable - 568B on each side or 568A on each side
    - Crossover Cable - 568A and 568B on each side and not necessaryily used today as switches and routers incorporate the crossover
    - Rollover Cable - 568A and reversal of 568A ion other side

### Coaxial Copper Cables
  * Made up of 4 Layers
    - Outer insulator
    - Shielding wire mesh
    - Inner Insulator
    - Copper core
  * Types of Copper Cables
    - Radio Guide RG-58 (Thinnet)
      * 10 Mbps
      * 185 meters
      * Uses a BNC connector
      * Has been replaced by twisted pair
    - RG-59 and RG-6
      * Typically Used for cable television and cable internet service

### Plenum-grade Cable
  * Traditional cables coated with polyvinyl chloride (PVC) give off toxic fumes when burning
  * PVC vs. Plenum
    - The plenum is an enclosed space used for airflow
    - Usually thought of as the space above a drop ceiling or below a raised floor
    - Plenum grade cable should always be used in a plenum space
    - Plenum-grade cable has a fire-retardent plastic jacket consisting of low-smoke PVC

### Ethernet Standards
  * 100BaseTX
    - 100: Line speed
    - Base: Baseband transmission
    - TX: Cable standard (twisted-pair or fiber)

### Common Connectors
  * Registered Jack RJ-11 (3 pairs)
  * RJ-45/RJ-48 (4 pairs)
  * UTP Coupler (extended patch cables)
  * BNC (British Naval Connector; Bayonet Neill-Concelman)
  * BNC Coupler (Extends cable length)
  * F-Connector
 
### Serial Connector
  * DB-9/RS-232
  * DB-25
  
### Fiber Cables
  * Transmits light instead of electricity
  * Pros: Security, speed, distance
  * Cons: Expensive, termination, flexibility
  * Single mode: One light path; longer distance
  * Multimode: Many light propagation paths; shorter
  * UPC (Ultra Physical Contact): 1G Green + Blue; flat endface
  * APC (Angled Physical Contact): 2G Green, endface polished at 8 degree angle to eliminate airgap at termination point
  
### Fiber Connectors
  * SC - aka subscriber connector, standard connector, squared connector
  * ST aka straight tip
  * LC aka lucid connector
  * MTRJ Media termination recommended jack
  * FC Fiber connector
  * Fiber coupler

### Media Converters
  * Used to allow connectivity between different media technologies
  * Examples
    - Single mode fiber ethernet
    - Multimode fiber to ethernet
    - Fiber to coaxial
    - Single mode to multimode fiber

### Cable Termination
  * Punchdown blocks are used in structural cabling systems
  * 66 and 110 refer to their Western Electric/Bell Model numbers
  * Patch Panel
    - Punchdown/Impact Tool
    
### Network Technician Tools
  * Cable Crimpers
    - Used to attach a connector on the end of the cable
  * Wire Strippers
  * Snips
    - Used to cut and sometimes strip cables
  * Time Domain Reflectometer (TDR)
    - Used to check the continuity of a copper cable
  * Optical Domain Reflectormeter (OTDR)
    - Used to check the continuity of a fiber optic cable
  * Both of the tools above are used to help locate where there is a break in the cable
  * Cable tester
    - Used to test whether a cable is working properly
  * Certifier
    - Used to test and validate whether a cable is ready to handle certain levels of throughput

## 1.5.Z Appendix

### Useful Links
- Microsoft Visio Network Shapes (http://www.visiocafe.com/links.htm)
- STP vs. UTP (http://www.ecmag.com/section/systems/stp-vs-utp)
- Difference Between EIA/TIA 568A and B (http://www.cat-5-cable-company.com/faq-568A-VS-568B.html)
- Pinout (https://en.wikipedia.org/wiki/Pinout)
- Twisted Pair (https://en.wikipedia.org/wiki/Twisted_pair)
- Electromagnetic Interference (https://en.wikipedia.org/wiki/Electromagnetic_interference)
- Crosstalk (Electronics) (https://en.wikipedia.org/wiki/Crosstalk_%28electronics%29)
- What's the Difference Between Ethernet Cables? (http://lifehacker.com/5994163/whats-the-difference-between-these-ethernet-cables-and-will-they-make-my-network-faster)
- What Kind of Cable Should I Use? (http://www.howtogeek.com/70494/what-kind-of-ethernet-cat-5e6a-cable-should-i-use/)
- What are Straight Through and Crossover Cables? (http://www.home-network-help.com/straight.html)
- Ethernet Crossover Cable (https://en.wikipedia.org/wiki/Ethernet_crossover_cable)
- Medium-Dependent Interface (MDI) (https://en.wikipedia.org/wiki/Medium-dependent_interface)
- Rollover Cable (https://en.wikipedia.org/wiki/Rollover_cable)
- Coaxial Cable (https://en.wikipedia.org/wiki/Coaxial_cable)
- RG-59 (https://en.wikipedia.org/wiki/Coaxial_cable)
- Plenum Cable (https://en.wikipedia.org/wiki/Plenum_cable)
- Registered Jack (https://en.wikipedia.org/wiki/Registered_jack)
- Network Adapters and Couplers (http://www.intellinet-network.com/en-US/categories/80-adapters-couplers)
- Single-Mode vs. Multimode Fiber Cable (http://www.multicominc.com/training/technical-resources/single-mode-vs-multi-mode-fiber-optic-cable/)
- UPC or APC? (http://www.belden.com/blog/datacenters/UPC-or-APC.cfm)
- Optical Fiber Connectors (https://en.wikipedia.org/wiki/Optical_fiber_connector)
- Fiber Optic Connector Guide (http://www.cablestogo.com/learning/connector-guides/fiber-networking)
- Media Converters (http://www.blackbox.com/Store/results.aspx/networking/media-converters/n-4294953610)
- 66 Block (https://en.wikipedia.org/wiki/66_block)
- 110 Block (https://en.wikipedia.org/wiki/110_block)
- Punchdown Tool (https://en.wikipedia.org/wiki/Punch_down_tool)
- Network Technician Tool Kits (http://www.lanshack.com/Technicians-Tool-Kits-C208.aspx)
- Things a Network Tech Should Carry to Every Job (http://www.nickh.org/computer/nethings.html)
- Network Tools (http://www.tigerdirect.com/applications/category/category_slc.asp?CatId=1796)
- Fluke Networks Products (http://www.flukenetworks.com/products)

## 1.6 Differentiating Between Common Network Topologies

### Study Alerts for Exam
- Identify which network topology corresponds to a description
- Associate a nteowrk topology with Ethernet standards and Layer 1 devices

### Network Topologies
- Layout of a computer network can be physical or logical
  * Physical = how computers are actually arranged
  * Logical = how computers appear to be connected to the user
  
### Bus Topology
- All of the computers are connected in a straight line
- Referred to shared network conenctivity
- Terminators must be used  at each end of a bus segment to prevent signals from bouncing 
- A single break in the cable would take down the entire network

### Star Topology
- All of the computers are connected through a central connection point (hub)
- A single break in the cable would only take down communication to one computer
- A hub failure would take down the entire network

### Ring Topology
- All of the computers are connected in a circular fashion
- Token ring attempted to prevent the "collision domain" problems with 802.3 Ethernet
- Data is passed around the ring from computer to computer
- A break in the cable would take down the entire network
- Token Ring
  * IEEE 802.5
  * 4-16 Mbps
  * Physical star
  * Logical ring

### Mesh Topology
- All of the computers are connected to all other computers
- Typically used in a WAN environment
- Provides fault tolerance in the event of a connection failure
- Partial vs. Full

### Hybrid Topologies
-  Different types of topologies can be used together to form a hybrid topology

### Network Architectures
- More generally, we can consider a network architecture to be a plan, or blueprint, for a network design
- Point-to-Point
  * One node trnasmits data, and the other node receives it
  * Star, mesh, and logical ring are point-to-point
  * Telco uses point-to-point
    - For example, a voice telephone call
    - Leased line connection
- Point-to-Multipoint
  * Multiple communication paths from a single location to multiple locations
  * The Thinnet bus is point-to-multipoint
  * A hub-and-spoke Frame Relay cloud is point-to-multipoint
  * A WIFI hotspot is another example
  * IP telephony
  
### Client-Server
- Each host acts specifically as a server (resource provider) OR a client (resource receiver)

### Peer-to-Peer
- Every host acts as both a server AND a client

## 1.6.Z Appendix

### Useful Links
- Pluralsight: CompTIA Mobility+ Part 1: Over-the-Air and Network Infrastructure (http://www.pluralsight.com/courses/comptia-mobility-plus-over-the-air-network)
- Pluralsight: Microsoft MTA: Networking Fundamentals Part 1 (http://www.pluralsight.com/courses/networking-fundamentals-pt1)
- Logical vs. Physical Network Topology (http://www.pcmag.com/encyclopedia/term/46301/logical-vs-physical-topology)
- Network Topology (https://en.wikipedia.org/wiki/Network_topology)
- Network Topology Notes (http://network-communications.blogspot.com/2011/06/network-topology-star-bus-mesh-ring.html)
- Network Topology Notes (Another Source) (http://computernetworkingnotes.com/network-technologies/network-topologies.html)
- Token Ring (https://en.wikipedia.org/wiki/Token_ring)
- Star Bus Network Topology (http://thought1.org/nt100/module3/star_bus.html)
- Cisco Guidelines on Fault-Tolerant Networking (http://www.cisco.com/c/en/us/products/collateral/switches/catalyst-4900-series-switches/white_paper_c11-540141.html)
- Introduction to Client/Server Networks (http://compnetworking.about.com/od/basicnetworkingfaqs/a/client-server.htm)
- Client-Server Model (https://en.wikipedia.org/wiki/Client%E2%80%93server_model)
- Peer-to-Peer Model (https://en.wikipedia.org/wiki/Peer-to-peer)
- Point-to-Point Communication (https://en.wikipedia.org/wiki/Point-to-point_(telecommunications))
- Point-to-Multipoint Communication (https://en.wikipedia.org/wiki/Point-to-multipoint_communication)
- Node (Networking) (https://en.wikipedia.org/wiki/Node_(networking))
- Host (network) (https://en.wikipedia.org/wiki/Host_(network))
- Wireshark (http://wireshark.org)
- DHCP: Wireshark Wiki (https://wiki.wireshark.org/DHCP)
- BitTorrent (https://en.wikipedia.org/wiki/BitTorrent)

## 1.7 DIfferentiating Between Common Network Infrastructures

### Study Alerts for Exam
- CompTIA item stems tend to be terse
  * Every word counts
- Eliminate distractors
  * Makes "picky" questions easier to answer correctly
 
### Network Infrastructure
- Network topology: Physical/logical arrangement of network assets
- Network architecture: The design of network assets (hardware and software)
  * Your plans
- Network infrastructure: The network assets themselves

### Wired Network Infrastructures
- Local Area Network (LAN)
  * Area of high speed connectivity contained within a single location
  * Internetwork: Multiple LAN segments seperated by a router
  * Intranet: Resources shared internally througout the LAN (and sometimes MAN and WAN, too!)
- Wide Area Network
  * Two or more LANs that use a service provider to establish network connectivity
  * Business almost always leases the WAN from a service provider
  * Usually a good degree of geogrpahical distance between sites
  * The internet is an example of a world wide public WAN
- Metropolitan Area Network (MAN)
  * Larger internetwork that spans buildings or multiple sites in the same city
  * Sometimes conflated with the Campus Area Network (CAN)
  * Because a service provider is involved, a MAN is really a WAN
- Medianet
  * Cisco technology built into some of their routers and switches that supports QoS for video, voice, and data
  * Media-aware, endpoint-aware, network-aware
  * Viedo Teleconference (VTC)
  * ISDN gateways
  * Session initiation Protocol (SIP): VoIP communications protocol

### Wireless Network Infrastructures
- Wireless Local Area Network (WLAN)
  * IEEE 802.11 standard: brand name Wi-Fi
  * Hotspot: Wireless access point
  * Antenna is key to WLAN design
    - Interference
    - Range (coverage)
  * "Double NAT" is often a problem in home WLANs
    - Certain cases it would be best to bridge the router so that all incoming traffic is going through the router
- Personal Area Network (PAN)
  * Near Field Communication (NFC): Proximity-based networking
  * Bluetooth: Short-wavelength radio-based communications; frange between 1-100M
    - Line-of-sight not necessary
  * Infrared Data Association (IrDA): Uses light and required line-of-sight
  * Concumer products use Bluetooth and IR all the time

### Special-Purpose Network Infrastructures
- SCADA/ICS
  * Industrial Control System (ICS)
  * Supervisory Control and Data Acquisition (SCADA)
  * Distributed Control System: Method for programming RTU/PLC
  * Remote Terminal Unit (RTU)/Programmable logic controller (PLC)
  
## 1.7.Z Appendix

### Useful Links
- Pluralsight: CompTIA Security+ (SY0-401) Compliance and Operational Security (http://www.pluralsight.com/courses/comptia-security-plus-sy0-401-compliance-operational-security)
- Pluralsight: CompTIA A+ Part 2: Networking (http://www.pluralsight.com/courses/comptia-a-plus-networking)
- How is Architecture Different from Infrastructure? (http://www.ebizq.net/blogs/ebizq_forum/2011/03/how-is-architecture-different-from-infrastructure.php)
- LAN, MAN, WAN (http://compnetworking.about.com/od/basicnetworkingconcepts/a/network_types.htm)
- Cisco Medianet Overview (http://www.cisco.com/c/en/us/solutions/collateral/enterprise/enterprise-medianet/qa_C67-511731.html)
- Cisco Medianet Data Sheet (http://www.cisco.com/c/en/us/products/collateral/routers/3900-series-integrated-services-routers-isr/data_sheet_c78-612429.html)
- VisualRoute (http://www.visualroute.com/)
- TRACERT Syntax (https://support.microsoft.com/en-us/kb/162326)
- TRACEROUTE Syntax (http://linux.die.net/man/8/traceroute)
- Double NAT (http://inmethod.com/forum/posts/list/908.page;jsessionid=09BBA9B5DB8375554A35164134EB26C2)
- WLAN Basics (http://www.slideshare.net/wifihead/wlan-basics-2702803)
- IEEE 802.11 Standards (https://standards.ieee.org/about/get/802/802.11.html)
- Infrared Data Association (https://en.wikipedia.org/wiki/Infrared_Data_Association)
- Bluetooth Basics (http://www.bluetooth.com/Pages/Basics.aspx)
- Apple iCloud Tabs (https://support.apple.com/en-us/HT202530)
- Mozilla Firefox Sync (https://support.mozilla.org/en-US/kb/how-do-i-set-up-firefox-sync)
- Google Chrome Tab Sync (https://support.google.com/chrome/answer/2591582?hl=en)
- Personal Area Network (https://en.wikipedia.org/wiki/Personal_area_network)
- Industrial Control System  (https://en.wikipedia.org/wiki/Industrial_control_system)
- SCADA (https://en.wikipedia.org/wiki/SCADA)
- Securing SCADA Networks (http://www.oe.netl.doe.gov/docs/prepare/21stepsbooklet.pdf)
- Key Difference Between SCADA Systems (http://blog.cimation.com/blog/key-differences-between-scada-dcs-and-hmi-systems)
- Telemetry (https://en.wikipedia.org/wiki/Telemetry)
- Banner Grabbing (https://en.wikipedia.org/wiki/Banner_grabbing)
- Google Hacking Database (http://www.exploit-db.com/google-dorks/)
- Internet of Things (IoT) (https://en.wikipedia.org/wiki/Internet_of_Things)
  
## 1.8 Implementing a Network Addressing Scheme

### Study Alerts for Exam
- General properties of IPv4 addresses
- General properties of IPv6 addresses
  * Recognize hexadecimal vs. decimal formats

### Physical Addresses
- MAC Addresses
  * Media Access Control (MAC) hardware addresses (OSI Layer 2)
  * 48 bit total
  * Each pair represents 8 bits
    - This makes sense mathematically as 4 bits give you 16 possible values (hexadecimal is base 16)
  * First 3 parts of the 48 bit MAC address is known as OUI (Organizational Unique Identifier)
  * Last 3 parts of a 48 bit MAC address is unique and assigned by the vendor
  * Address Resolution Protocol (ARP) is the layer 2 protocol that resolves MACs from layer 3 IP addresses
  
### IPv4 Address Basics
- Defined in RFC 791
- Maintained by IANA
- The public address pool is exhausted
- 32-bits = 4.2 billion addresses
- IP addresses need subnet mask to be meaningful
- Default gateway is "near sode" router interface
- A host uses its subnet mask with other computers' IP addresses to check whether they are on the local network or if the connection requires a router

### IPv4 Address Structure
- Each octet can go from o to 255
- 256 combinations

### Classful Addressing
- Class A
  * First Octet: 1-126
  * Classful Mask: 255.0.0.0
  * CIDR Mask: /8
- Class B
  * First Octet: 128-191
  * Classful Mask: 255.255.0.0
  * CIDR Mask: /16
- Class C
  * First Octet: 192-223
  * Classful Mask: 255.255.255.0
  * CIDR Mask: /24
- Class D
  * First Octet: 224-255
- Loopback address: 127.0.0.1
- Classless addressing: Network break at any bit boundary
- 192.168.16.0/27 Example
  * 1 subnet with 30 hosts

### CIDR Notation
- Memorize at least to this point for questions in the exam
- CIDR is a large topic and needs to be looked at in more detail
- 192.168.4.0/24
  * 255.255.255.0
  * 1 subnet and 254 hosts
- Overview on Specific CIDR
  * 1000 0000 = /25 = 2 subnets, 126 hosts
  * 1100 0000 = /26 = 4 subnets, 62 hosts
  * 1110 0000 = /27 = 8 subnets, 30 hosts
  * 1111 0000 = /28 = 16 subnets, 14 hosts
  * 1111 1000 = /29 = 32 subnets, 6 hosts
  * 1111 1100 = /30 = 64 subnets, 2 hosts

### IPv4 Address Transmission Types
- Unicast
- Broadcast
- Multicast

### Revisiting Domains
- Collision
- Broadcast

### Private IP Addresses
- Classful Private IPs
- Class A
  * Range: 10.0.0.0 - 10.255.255.255
  * Default Mask: 255.255.0.0
- Class B
  * Range: 172.16.0.0 - 172.31.255.255
  * Default Mask: 255.255.0.0
- Class C
  * Range: 192.168.0.0 - 192.168.255.255
  * Default Mask: 255.255.255.0
- RFCs 1918, 5737
- APIPA: 169.254.0.0/16 (technically Class B)

### Revisiting NAT and PAT
- NAT serves as a "shim" for IPv4
- Routers and admins maintain the NAT table
- PAT maps protocol ports
- We don't need NAT/PAT for IPv6

### IPv6
- IPv6 History and Basics
  * Finalized in RFC 1883 (1996)
  * 128 bit address space
  * 5*10 to the power of 28 IP addresses for every person on earth
  * Benefits
    - Simplified header structure
    - No broadcasts or packet fragmentation (unicast, multicast, and anycast)
    - Built-in IPSec
    - Co-existence with IPv4 (dual-stack, tunnels)
    
### IPv6 Address Format
- Uses hexadecimal (base 16) numbers for greater range
- 128 bits broken into 64 for network and 64 for node
  * 8 groups of 4 hex digits, with each group representing 16 bits (2 octets)
- Dropped leading zeros and compression
  * Format before - 2001:0db8:45b6:0:0:0:0:1
  * Format after - 2001:db8:45b6::1 
- Auto address generation
- DHCPv6
  * AAAA
- IPv6 Address Types
  * Stateless Address Autoconfiguration (SLAAC)
    - Link-local addresses fs80::/64
    - EUI-64 derives IPv6 address by inserting a fixed value along with the 48-bit MAC address
- Loopback for IPv6 - ::1/128

### IPv6 Transition Protocols
- Dual stack: Run both IPv4 and IPv6 simultaneously
- 4in6: Encapsulate IPv4 traffic in IPv6 tunnels
- 6to4: Requires public IPv4 addresses
- Teredo: Can be used with NAT (written by a Microsoft employee)
- Miredo: *NIX implementation of Teredo
  
## 1.8.Z Appendix

### Useful Links
- MAC Address (https://en.wikipedia.org/wiki/MAC_address)
- MAC Address and OUI Lookup (http://aruljohn.com/mac.pl)
- Hexadecimal (https://en.wikipedia.org/wiki/Hexadecimal)
- Hex to Decimal Converter (http://www.binaryhexconverter.com/hex-to-decimal-converter)
- Binary to Decimal Converter (http://www.binaryhexconverter.com/binary-to-decimal-converter)
- Address Resolution Protocol (ARP) (https://en.wikipedia.org/wiki/Address_Resolution_Protocol)
- Wireshark (https://www.wireshark.org/)
- Ubuntu Linux Desktop (http://www.ubuntu.com/download/desktop)
- RFC 791 (https://www.ietf.org/rfc/rfc791.txt)
- RFC Lookup (https://www.rfc-editor.org/search/rfc_search.php)
- Internet Assigned Numbers Authority (IANA) (http://www.internetassignednumbersauthority.org/)
- IEEE (https://www.ieee.org/index.html)
- IPv4 Address Exhaustion (https://en.wikipedia.org/wiki/IPv4_address_exhaustion)
- Classful vs. Classless IPv4 Addressing (https://learningnetwork.cisco.com/docs/DOC-24528)
- Classful Network (https://en.wikipedia.org/wiki/Classful_network)
- Subnetwork (https://en.wikipedia.org/wiki/Subnetwork)
- Subnet Mask Cheat Sheet (http://www.aelius.com/njh/subnet_sheet.html)
- List of Assigned /8 IPv4 Address Blocks (https://en.wikipedia.org/wiki/List_of_assigned_/8_IPv4_address_blocks)
- Default Gateway (https://en.wikipedia.org/wiki/Default_gateway)
- Classless Inter-Domain Routing (CIDR) (https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing)
- Unicast, Broadcast, and Multicast (http://www.inetdaemon.com/tutorials/internet/ip/addresses/unicast_vs_broadcast.shtml)
- Anycast (https://en.wikipedia.org/wiki/Anycast)
- Collision Domains vs. Broadcast Domains (http://ciscoskills.net/2011/03/30/collision-domains-vs-broadcast-domains/)
- RFC 1918 (https://tools.ietf.org/html/rfc1918)
- RFC 3330 (https://www.rfc-editor.org/rfc/rfc3330.txt)
- Windows PowerShell (https://en.wikipedia.org/wiki/Windows_PowerShell)
- RFC 2460 (https://tools.ietf.org/html/rfc2460)
- Solarwinds Advanced Subnet Calculator (http://www.solarwinds.com/products/freetools/free_subnet_calculator.aspx)
- IPv6: Dual-Stack vs. Tunneling (http://www.networkworld.com/article/2285078/tech-primers/ipv6--dual-stack-where-you-can--tunnel-where-you-must.html)
- IPv6 Transition Mechanisms (https://en.wikipedia.org/wiki/IPv6_transition_mechanisms)
- IPv6 Transition Technologies (http://ipv6.com/articles/gateways/IPv6-Tunnelling.htm)
- Loopback (https://en.wikipedia.org/wiki/Loopback)
- Localhost (https://en.wikipedia.org/wiki/Localhost)
- Cisco CCENT (http://www.cisco.com/web/learning/certifications/entry/ccent/index.html)
- Cisco CCNA (http://www.cisco.com/web/learning/certifications/associate/ccna/index.html)

## 1.9 Understanding Routing Concepts and Protocols

### Study Alerts for Exam
- Identify
  * General characteristics of routing protocols
- Visualize
  * Packet flow to help you solve network problems

### Introduction to Routing
- What's a loopback address?
  * Tests IP data flows for the localhost (diagnostics)
  * IPv4: 127.0.0.1/8
  * IPv6 ::1/128

### Understanding Routing
- Packet transfers between IP subnetworks (broadcast domains)
- OSI Layer 3 IP addresses
- Route path options
  * Static routes: Okay for smallest of internetworks
  * Dynamic routes: Routers build a routing table by communicating with neighboring routers
- Default route: The router's "default gateway"

### Routing vs. Routed Protocols
- Routing protocols are used by routers to calculate best routes to remote networks
  * RIPv2, OSPF, BGP
- Routed protocols represent the data handles by routers
  * TCP/IP suite, with IPv4 and IPv6 in particular

### More Routing Vocabulary
- Convergence: The time it takes for all routers in an internetwork to possess a complete routing table
- Latency: Time it takes for a packet to cross router interfaces
- Administrative distance (AD): Arbitrary that judges precedence of a route (eg. Directly connected route = 1; bad route 100, etc.)
- Maximum Transmission Unit (MTU): The largest data unit that can be passed without dividing it into segments (fragmentation)
- Bandwidth: Link speed

### Routing Loops
- Occurs when a routing protocol algorithm error occurs
- Network traffic forms infinite loop
- Split horizon: Prevents a route learned on one interface from being advertised out same interface
- Poison Reverse: Marks Split Horizon routes with infinite metric

### Distance-Vector Routing Protocols
- Uses hop count as its routing metric
- Routing Information Protocol version 2 (RIPv2)

### Link-State Routing Protocols
- Router builds a map of the internetwork
  * Uses Link-state advertisements (LSAs)
- Metrics: cost values
- Protocol examples:
  * Open shortest Path First (OSFP); used in enterprise networks due to its performance and flexibility
- Intermediate System-to Intermediate System (IS-IS): Uses the Shortest Path Algorithim (SPF); used by ISPs

### Hybrid Routing Protocols
- Takes into account both hop count and cost metrics
- Border Gateway Protocol (BGP): "The routing protocol of the internet
  * Called a Path Vector routing protocol
- Autonomous System (AS): Globally unique identifiers that connect large scale IP networks under the same routing policies

### Advanced Routing Concepts
- Interior and Exterior Gateway Protocols
  * Interior Gateway Protocols (IGPs): Handle routing within an autonomous system (AS, routing domain)
    - This is where distance-vector and link-state routing protocols fit
  * Exterior Gateway Protocol (EGPs): Handle routing between ASs (think: service provider)
  
### Routing High Availability
- Shortest Path Bridging (SPF): IEEE 802.1aq; enables multipath routing
- Virtual Router Redundancy Protocol (VRRP) - IETF standard
- Hot Standby Router Protocol (HSRP) - Cisco proprietary
- Virtual IP (VIP)

### Route Redistribution/Aggregation
- Aggregation: Also called route summarization; intende4d to minimize routing table size (bigger tables impact performance)
- Redistribution: A router injects a route learned with protocol A into protocol B; provides richer route redundancy (3Rs!)

## 1.9.Z Appendix

### Useful Links
- Loopback Address (https://en.wikipedia.org/wiki/Loopback)
- Localhost (https://en.wikipedia.org/wiki/Localhost)
- HOSTS File (https://en.wikipedia.org/wiki/Hosts_(file))
- Protocol Data Units and OSI (https://en.wikipedia.org/wiki/Protocol_data_unit#OSI_model)
- Static vs. Dynamic Routing (http://www.ciscopress.com/articles/article.asp?p=2180210&seqNum=5)
- Static vs. Dynamic Routing (Another reference) (http://www.inetdaemon.com/tutorials/internet/ip/routing/dyamic_vs_static.shtml)
- Distance-Vector Routing Protocol (https://en.wikipedia.org/wiki/Distance-vector_routing_protocol)
- RIPv2 Basics (http://www.techrepublic.com/article/cisco-administration-101-know-the-basics-about-ripv2/)
- Open Shortest Path First (OSPF) (https://en.wikipedia.org/wiki/Open_Shortest_Path_First)
- OSPF White Paper (http://www.cisco.com/c/en/us/td/docs/internetworking/technology/handbook/ito_doc/OSPF.html)
- What is Administrative Distance? (http://www.cisco.com/c/en/us/support/docs/ip/border-gateway-protocol-bgp/15986-admin-distance.html)
- Troubleshooting with Ping and Traceroute (http://blog.pluralsight.com/troubleshoot-ping-traceroute)
- Troubleshooting with Ping (http://www.ghacks.net/2011/05/12/network-troubleshooting-basics-the-ping-command/)
- Border Gateway Protocol (BGP) (https://en.wikipedia.org/wiki/Border_Gateway_Protocol)
- BGP Essentials (http://searchtelecom.techtarget.com/feature/BGP-essentials-The-protocol-that-makes-the-Internet-work)
- Secure Shell (https://en.wikipedia.org/wiki/Secure_Shell)
- PuTTY Freeware (http://www.putty.org/)
- Telnet (https://en.wikipedia.org/wiki/Telnet)
- VyOS (http://vyos.net/wiki/Main_Page)
- Interior Gateway Protocol (https://en.wikipedia.org/wiki/Interior_gateway_protocol)
- Exterior Gateway  Protocol (https://en.wikipedia.org/wiki/Exterior_Gateway_Protocol)
- Virtual Router Redundancy Protocol (https://en.wikipedia.org/wiki/Virtual_Router_Redundancy_Protocol)
- Hot Standby Router Protocol (https://en.wikipedia.org/wiki/Hot_Standby_Router_Protocol)
- RFC 2281 (HSRP) (https://tools.ietf.org/html/rfc2281)
- HSRP vs. VRRP (https://supportforums.cisco.com/discussion/12236121/what-difference-between-hsrp-and-vrrp)
- Comparing HSRP and VRRP (http://www.routerfreak.com/comparing-hsrp-versus-vrrp-same-thing-only-different/)
- Virtual IP Address (https://en.wikipedia.org/wiki/Virtual_IP_address)
- Route Summarization (http://www.orbit-computer-solutions.com/IP-Address---Route-Summarization-Example-_2.php)
- Advanced IP Addressing/Route Summarization (http://www.ciscopress.com/articles/article.asp?p=174107&seqNum=3)
- More on Route Summarization (http://resources.intenseschool.com/ccna-prep-route-summarization-a-need-for-a-routing-table/)
- Redistributing Routing Protocols (http://www.cisco.com/c/en/us/support/docs/ip/enhanced-interior-gateway-routing-protocol-eigrp/8606-redist.html)
- Route Redistribution Explained (https://supportforums.cisco.com/document/12015996/route-redistribution-explained)

## 1.10 Introducing Unified Communication Technologies

### Study Alerts for Exam
- Recognize
  * UC vocabulary terms and business use case
- Visualize
  * Audio/video packet flow among all the UC components

### Defining Unified Communications
- Unified Communications
  * Integration of real time, enterprise, communication services such as instant messaging (chat), presence information, voice (including IP telephony), mobility features (including extension mobility and single number reash), audio, web & video conferencing, fixed mobile convergence (FMC), desktop sharing, data sharing (including web-connected electronic interactive whiteboards), call control and speech recognition with non-real-time communication services such as unified messaging (integrated voicemail, e-mail, SMS and fax)
  
### UC Value Proposition
- Can retire expensive analog PBX and leased lines
- Enhanced collaboration
  * Presence, IM, Web conferencing
- With IP telephony, avoid long distance PSTN charges
- Gives business reach to everyone, everywhere
  * Can get business calls on your mobile phone
- Improved business results at lower costs (in the long term)

### Unified Communications Terminology
- (IP) Telephony: audio and/or video
- Voice over IP (VOIP): Transmitting audio and video over IP networks
- A/V conferencing: Remote teams/remote presentations
- Instant Messaging: Real-time chat
- Presence: Reveals online status
- Codec: Coder/Decoder; G.711 (PCM 64Kbps audio) and H.264 (compressed video)
- IP transmissions
  * Unicast
  * Multicast

### UC Protocol Stack
- Session Initiation Protocol (SIP): VoIP signaling protocol; can be trunked across WAN connections
  * Low overhead, HTTP-like behaviour
- Real-Time transport protocol (RTP): Carries voice and interactive video
  * Transport layer; UDP instead of TCP
- TLS (SRTP): Encrypts SIP traffic
- DiffServ or DS: QoS architecture model
- Extensible Messaging and Presence Protocol (XMPP): Open-source UC platform (Jabber)

### UC Components
- VoIP phone/soft phone
- Access switch
- UC server(s)
- UC gateway
- IP or analog PBX
- Edge router

### UC Hardware
- IP soft phone
- VoIP gateway/integrated services router
- UC management software
- Analog PBX

### Quality of Service QoS
- ITU-T has a subjective call quality index called Mean Opinion Score (MOS)
- ITU-T now moving toward the E-Model, which is more quantitative
- Network engineers use either DSCP or CoS to "mark" packets with priority levels
  * Layer 4: Segment
  * Layer 3: Packet
  * Layer 2: Frame
  * layer 1: Bits
- Differentiated Service Code Point (DSCP, sometimes DiffServ): Layer 3; 6 bits of the type of service (ToS) field of a VoIP packet header
- Class of Service (CoS): Layer2; present in 802.1Q VLAN frame

## 1.10.Z Appendix

### Useful Links
- Pluralsight: Cisco CCNA Voice: Voice Overview and Lab Setup (http://www.pluralsight.com/courses/cisco-ccna-voice-overview)
- Pluralsight: Lync Server 2013: Introduction to Enterprise Voice and Unified Messaging (http://www.pluralsight.com/courses/lync-2013-enterprise-voice)
- Definition: Use Case (https://en.wikipedia.org/wiki/Use_case)
- Definition: Unified Communications (https://en.wikipedia.org/wiki/Unified_communications)
- Definition: Value Proposition (https://en.wikipedia.org/wiki/Value_proposition)
- Definition: Voice over IP (https://en.wikipedia.org/wiki/Voice_over_IP)
- VoIP Basics (http://www.tns.com/voip.asp)
- ITU-T (http://www.itu.int/en/ITU-T/Pages/default.aspx)
- IEEE 802.1X (https://en.wikipedia.org/wiki/IEEE_802.1X)
- IEEE 802.1Q (https://en.wikipedia.org/wiki/IEEE_802.1Q)
- Cisco WebEx (http://www.webex.com/)
- GoToMeeting (http://www.gotomeeting.com/online/start)
- BlueJeans (http://bluejeans.com/)
- Skype for Business (http://www.skype.com/en/business/)
- VoIP Protocols and Standards (http://www.protocols.com/pbook/voip.htm)
- Session Initiation Protocol (SIP) (https://en.wikipedia.org/wiki/Session_Initiation_Protocol)
- Real-Time Transport Protocol (RTP) (https://en.wikipedia.org/wiki/Real-time_Transport_Protocol)
- Secure RTP (https://en.wikipedia.org/wiki/Secure_Real-time_Transport_Protocol)
- Transport Layer Security (TLS) (https://en.wikipedia.org/wiki/Transport_Layer_Security)
- Wireshark Sample Captures (https://wiki.wireshark.org/SampleCaptures)
- Dia Diagram Editor (http://sourceforge.net/projects/dia-installer/)
- The XMPP Standards Foundation (https://xmpp.org/)
- Selecting the Right VoIP Phone System (http://www.voipsupply.com/buying-voip-phone-system)
- IP Phone Buying Guide (http://www.voiplink.com/voip-articles/ip-phone-buying-guide)
- DSCP vs. CoS (https://learningnetwork.cisco.com/thread/44413)
- Difference Between DSCP and CoS (https://elhallak.wordpress.com/2011/08/07/what-is-the-difference-between-cos-ip-precedence-and-dscp/)
- Type of Service (https://en.wikipedia.org/wiki/Type_of_service)
- Cisco IP Communicator (http://www.cisco.com/c/en/us/products/collaboration-endpoints/ip-communicator/index.html)
- IP Softphone (https://en.wikipedia.org/wiki/Softphone)
- VoIP Components (https://technet.microsoft.com/en-us/library/bb663730(v=office.12).aspx)
- Comparing Analog and Digital Voice Systems (http://www.shoretelsky.com/resources/learn/analog-phone-system-vs-digital-phone-system/)
- Private Branch Exchange (PBX) (https://en.wikipedia.org/wiki/Business_telephone_system#Private_branch_exchange)
- 3CX VoIP Gateway (http://www.3cx.com/pbx/voip-gateway/)
- Mean Opinion Score (MOS) (https://en.wikipedia.org/wiki/Mean_opinion_score)
- The E-Model Tutorial (https://www.itu.int/ITU-T/studygroups/com12/emodelv1/tut.htm)

## 1.11 Comparing Cloud and Virtualization Technologies

### Study Alerts for Exam
- Understand the major cloud computing models
- Memorize Some of the picky protocol details of SANs

### Virtualization
- Hardware virtualization
- Host: Running a hypervisor
  * Part of a CPU feature set
  * Microsoft Hyper-V
  * VMWare vSphere/EXSi
- Guest: The nested OS
  * "borrows" host hardware
- Lots of business benefits

### Virtual Networks
- Bridged: VM appears on same network as host
- NAT: VM "hides" behind host's IP address
- Host to Host: Internal private network
- Software-Defined Networking (SDN): Seperation of ocntrol plane from data plane

### Storage Area Networks (SANs)
- Network-Attached Storage (NAS): File-level access to storage using CIFS and NFS
  * the cost effective option
- Storage Area Network (SAN): Block-level access to storage
- You can easily virtualize iSCSI
- Some hypervisors even have virtual fibre Channel adapters

### Protocol Encapsulation
- Fibre Channel: High-speed (16Gbps) storage architecture
  * Expensive
- iSCSI: SCSI storage commands transmitted over full-duplex Ethernet
  * Cheap
- Jumbo frames: Ethernet frames are normally 1500 bytes (payload), but the Jumbo Frame spec allows MTUs of 9000 bytes

### Cloud Concepts
- What is cloud computing?
  * Service on demand/on tap
  * On-demand self-service
  * Resource pooling
  * Broad access
  * Rapid elasticity

### Cloud Service Models
- SaaS
  * Aimed at end users
  * Examples: Dropbox, Office 365
- PaaS
  * Aimed at developers
  * May overlap with SaaS and IaaS
  * Examples: AWS, Azure, Google Cloud
- Iaas
  * Infrastructure as a Service
  * Aimed at IT pros
  * AWS, Azure, Google Cloud

### Cloud Delivery Models
- Public Cloud
  * All customers have same access
  * Dropbox
- Private Cloud
  * Business builds its own cloud infrastructure
  * Expensive
- Hybrid Cloud
  * Integrate public cloud services into private cloud
  * System Center and MS Azure

### Cloud Computing Practical Considerations
- Community cloud: Two or more organizations "pitch in" to create their own hybrid cloud (possible concerns of security)
- Remote access via SSH (TCP 22) or RDP (TCP 3389)
- Monitoring: built-in or third party network analyzer
  * Not to be confused with a protocol analyzer
  * Amazon Web Services (AWS) allows Nagios Network Analyzer

## 1.11.Z Appendix

### Useful Links
- Pluralsight: CompTIA Cloud Essentials (http://www.pluralsight.com/courses/comptia-cloud-essentials)
- Pluralsight: Understanding the Difference Between Microsoft Azure and Amazon Web Services (http://www.pluralsight.com/courses/understanding-microsoft-azure-amazon-aws)
- Pluralsight: ComptIA Storage+ Part 1 (http://www.pluralsight.com/courses/comptia-storage-plus-pt1-storage-fundamentals)
- Definition: Virtualization (https://en.wikipedia.org/wiki/Virtualization)
- Virtualization Basics (https://www.vmware.com/virtualization/virtualization-basics/what-is-virtualization)
- Definition: Hypervisor (https://en.wikipedia.org/wiki/Hypervisor)
- VMware: (https://www.vmware.com/)
- Oracle VM VirtualBox (https://www.virtualbox.org/)
- Citrix XenServer (http://www.citrix.com/products/xenserver/overview.html)
- Microsoft Hyper-V (http://www.microsoft.com/en-us/server-cloud/solutions/virtualization.aspx)
- x86 Virtualization - (https://en.wikipedia.org/wiki/X86_virtualization)
- VMware Virtual Networking Concepts (https://www.vmware.com/files/pdf/virtual_networking_concepts.pdf)
- Software-Defined Networking (SDN) (https://en.wikipedia.org/wiki/Software-defined_networking)
- Difference Between Control Plan and Data Plane (http://sdntutorials.com/difference-between-control-plane-and-data-plane/)
- NAS and SAN Overview (http://www.nas-san.com/differ.html)
- Fibre Channel (https://en.wikipedia.org/wiki/Fibre_Channel)
- Hyper-V Virtual Fibre Channel Overview (https://technet.microsoft.com/en-us/library/hh831413.asp)
- iSCSI Basics (https://www.thomas-krenn.com/en/wiki/ISCSI_Basics)
- iSCSI SANs Compared (http://www.tomshardware.com/reviews/adaptec-enhance-technology,1802-2.html)
- Microsoft iSCSI Initiator Step-by-Step Guide (https://technet.microsoft.com/en-us/library/ee338476(v=ws.10).aspx)
- SCSI Initiator and Target (https://en.wikipedia.org/wiki/SCSI_initiator_and_target)
- Windows Server 2012 R2: iSCSI Target (http://blogs.technet.com/b/filecab/archive/2013/07/31/iscsi-target-server-in-windows-server-2012-r2.aspx)
- Microsoft's Perspective of Cloud Computing: (https://technet.microsoft.com/en-us/gg521165.aspx)
- What is Cloud Computing? (http://whatiscloud.com/cloud_characteristics/multi_tenancy)
- Understanding the Cloud Computing Stack: (http://www.rackspace.com/knowledge_center/whitepaper/understanding-the-cloud-computing-stack-saas-paas-iaas)
- Definition: Cloud Computing: (https://en.wikipedia.org/wiki/Cloud_computing)
- Cloud Service Models: http://searchcloudcomputing.techtarget.com/definition/SPI-model
- The Four Primary Cloud Deployment Models: (http://cloudtweaks.com/2012/07/4-primary-cloud-deployment-models/)
- Cloud Deployment Models: (http://www.awesomecloud.com/channel-partners/resources/how-to-sell-cloud-computing/deployment-models/#.VSglYO7F8bw)
- Amazon Web Services: (AWS) (https://aws.amazon.com/)
- Microsoft Azure: (https://azure.microsoft.com/en-us/)
- Google Cloud Platform: (https://cloud.google.com/)
- Microsoft Private Cloud White Paper (https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=1&cad=rja&uact=8&ved=0CDwQFjAA&url=http%3A%2F%2Fwww.microsoft.com%2Fclick%2Fservices%2FRedirect2.ashx%3FCR_EAC%3D300035806&ei=DiYoVcKNLtPnoASd84CoDQ&usg=AFQjCNHtrwOqWBGnv4apnARbTA2SSBWpnQ&sig2=_zGHBoIr6me0u9rR6YY4Qg&bvm=bv.90491159,d.aWw)
- Architecting a Microsoft Private Cloud (https://technet.microsoft.com/en-us/magazine/hh127072.aspx)
- Microsoft System Center 2012 R2 (http://www.microsoft.com/en-us/server-cloud/products/system-center-2012-r2/)
- Remote Desktop Protocol (RDP) (https://en.wikipedia.org/wiki/Remote_Desktop_Protocol)
- Nagios Network Analyzer (http://www.nagios.com/products/nagios-network-analyzer)

## 1.12 Implementing a Basic Network

### Network Design Basics
- Request for Proposal (RFP)
- Top Down Network Design
  * instead of starting with hardware, begin with business requirments and technical needs, wants, and constraints
  * What are the technical challenges?
  * Proposed solution
  * Implementation
- Network design requirements understanding of project management best practices
  * PMI Project Management Professional (PMP)
- importance of documentation/tools

### Device Types and Requirements
- What kind of Ethernet will you run?
  * 1000BaseTX to desktop
  * 1000Base-SR for multimode fiber trunk/core runs
  * 10Gbase-SR for SAN
- What's going on in your cable runs? (airflow, plenum-grade cable)
- Are you buying or leeasing your hardware?
- How compatible is your physical plant with Wi-Fi?

### Network Design Limitations
- Whereis your service provider demarc? Do you need an extension?
- How robust is the conduit system within your building? Between buildings?
- What needs for compatibility do you have?
  * Switches and routers from different manufacturers
  * Windows, OS X, and Linux desktops

### Network Design Considerations
- How to maintain "clean access" with guest users (wireless and wired)
  * Network Access Control (NAC)
  * VLAN design (guest, remediation VLANs)
- Securely supporting remote access users
  * On-demand or "always on" VPN solutions
- Physical security

### Intermediate Distribution Frame (IDF)
- Power Strip
- Patch panel (copper, fiber)
- Access/distribution switches (Layer 3, STP)
- UPS
- Top-of-rack vs. End-of-row uplink/aggregation

### Main Distribution Frame (MDF)
- DWDM/multi-mode fiber vertical run
- Fiber patch panel to aggregate from IDF
- FCoE SAN

## 1.12.Z Appendix

### Useful Links
- Pluralsight: Cisco CCNA Wireless Design and Troubleshooting: (http://www.pluralsight.com/courses/cisco-ccna-wireless-design-troubleshooting)
- Pluralsight: Cisco CCNP Security: Secure Design Principles: (http://www.pluralsight.com/courses/cisco-ccnp-security-secure-design-principles)
- Pluralsight: Project+: (http://www.pluralsight.com/courses/comptia-project-plus-pt1)
- Pluralsight: PMP: (http://www.pluralsight.com/courses/pmp-introduction-project-management-pmp-exam)
- Definition: SOHO: (http://www.webopedia.com/TERM/S/SOHO.html)
- Sample Request for Proposal (RFP): (http://www.qando.net/wp-content/uploads/rfp_web_sample.pdf)
- Another Sample RFP: (http://www.aia.org/aiaucmp/groups/ek_public/documents/pdf/aiap037331.pdf)
- Sample Network Design Proposal: (http://normcoleman.norkris.com/Samples/HappyHavenDayCareCenter-NetworkDesignProposal2.pdf)
- Top-Down Network Design: (http://www.pearsonitcertification.com/articles/article.aspx?p=1686038)
- Greenfield Project: (https://en.wikipedia.org/wiki/Greenfield_project)
- Definition: DWDM: (http://www.webopedia.com/TERM/D/DWDM.html)
- Single-Mode vs. Multi-Mode Optical Fiber: (http://www.multicominc.com/training/technical-resources/single-mode-vs-multi-mode-fiber-optic-cable/)
- Gigabit Interface Converter (GBIC): (https://en.wikipedia.org/wiki/Gigabit_interface_converter)
- Understanding Ethernet Nomenclature: (http://www.brocade.com/downloads/documents/technical_briefs/Ethernet_Nomenclature_GA-TB-357.pdf)
- Limitations Affecting Equipment Installations: (http://www.ciscopress.com/articles/article.asp?p=355876&seqNum=2)
- Microsoft Visi:o (https://products.office.com/en-us/visio/flowchart-software)
- Dia Diagram Editor: (http://sourceforge.net/projects/dia-installer/)
- OmniGraffle: (https://www.omnigroup.com/omnigraffle)
- Lowell Vanderpool: - YouTube (https://www.youtube.com/user/vanderl2796)
- Demarcation Point: (https://en.wikipedia.org/wiki/Demarcation_point)
- Demarc Extension: (https://en.wikipedia.org/wiki/Demarcation_point#Demarc_extension)
- Network Access Control: (https://en.wikipedia.org/wiki/Network_Access_Control)
- Cisco NAC Appliance: (http://www.cisco.com/c/en/us/products/security/nac-appliance-clean-access/index.html)
- Bring Your Own Device: (https://en.wikipedia.org/wiki/Bring_your_own_device)
- IEEE 802.1Q: (https://en.wikipedia.org/wiki/IEEE_802.1Q)
- HID Proximity Card Readers: (https://www.hidglobal.com/products/readers/hid-proximity)
- CIDR Notation TutorialL: (http://compnetworking.about.com/od/workingwithipaddresses/a/cidr_notation.htm)
- Solarwinds IP Calculator: (http://www.solarwinds.com/products/freetools/free_subnet_calculator.aspx)
- Intermediate Distribution Frame (https://en.wikipedia.org/wiki/Intermediate_distribution_frame)
- Main Distribution Frame (https://en.wikipedia.org/wiki/Main_distribution_frame)
- UPS Selector Tool (http://www.apc.com/tools/ups_selector/)
- Top-of-Rack vs. End-of-Row Designs (http://bradhedlund.com/2009/04/05/top-of-rack-vs-end-of-row-data-center-designs/)
- Cisco Catalyst 6500 Series Data Center Switches (http://www.cisco.com/c/en/us/products/switches/catalyst-6500-series-switches/index.html)



