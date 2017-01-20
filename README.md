# network-handbook README File
---
# My Notes  



### CompTIA+ Certification  

Entry level certification

### Comptia Network + Objectives N10-006
  
- See PDF
- Navigate to Pearson VUE in For test takers tab (https://home.pearsonvue.com/)
- CompTIA blueprint will list the metadata of the exam
- Not all multiple choice questions
- Passing is 720 and above from scale 100-900

### 1. Network Architecture for CompTIA Network

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

### Objective 1.1 - Explain the Functions and Applications of Various Network Devices 
- Core connectivity devices
- Security devices
- Special purpose devices

#### Hub
- Works at OSI Layer 1 (Physical)
- Hubs are multiport repeaters
  * Regenerate the signal  
- One big collision domain
- Good for network diagnostics and nothing else
- Understanding network hubs -> (http://www.techiwarehouse.com/engine/5ea76190/Understading-Networking-Hubs/)
- Bridges -> (http://compnetworking.about.com/cs/internetworking/g/bldef_bridge.htm)

#### Switch
- Successor to the bridge
- Works at OSI Layer 2 (Data Link)
  * Can also function at OSI Layer 3 (Network)
- Switches store an in-memory MAC (aka media access control) table and provide dedicated bandwidth to each port (collision domain)
- Network Switch -> (https://en.wikipedia.org/wiki/Network_switch)
- Difference Between Hubs, Switches, and Routers -> (http://www.webopedia.com/DidYouKnow/Hardware_Software/router_switch_hub.asp)

#### Router
- Operates at OSI Layer 3 (Network)
- Seperate entire networks
- Modular design (especially Cisco)

#### Wireless Acess Point
- Provides IEEE 802.11 connectivity
- Many support Power over Ethernet (PoE)
  * IEEE 802.af specifies 15.4W power
- Wireless LAN controllers
  * Centralized management of many WAPs
  
#### Ethernet Domains

- Hub
  * One collision domain
- Switch
  * Four collision domains
- Router
  * Four broadcast and collision domains

#### Configuring a Router

