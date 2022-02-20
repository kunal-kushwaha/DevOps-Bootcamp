## Introduction 

**Network** in simple words means computers connected together.

**Internet** is a collection of these computer networks.

_Image to be added_

**How did it start?**
It all started from ARPA: Advanced Research Projects Agency

_Image to be added_

## Client-Server Architecture

**World Wide Web (WWW):** The world wide web commonly known as the web, is an information system where documents and other web resources are identified by UR:s, which may be interlinked by hyperlinks and are accessible over the internet.

_Internet Society_ are responsible for creating these protocols.

_Image to be added_

## Protocols

**Protocol** is a set of rules or procedures for transmitting data between electronic devices, such as computers.

**Some Basic Protocols:**
- `TCP - Transmission Control Protocols`
   It ensures that the data will reach its destination and not get corrupted on the way
- `UDP - User Datagram Protocols`
   It is a lightweight data transport protocol.
   It provides a mechanism to detect corrupt data in packets, but it does not attempt to solve other problems that arise with packets, such as lost or out of order packets.
- `HTTP - Hyper Text Transfer Protocol`
   It is an application-layer protocol for transmitting hypermedia documents, such as HTML.
   Is used by web browsers, this is the data which be being transferred between clients and servers.


An **IP address** is a unique address that identifies a device on the internet or a local network.

Every single device on the internet that can communicate with each other, they have an IP address.

**Format of IP Address** <br/>
X.X.X.X <br/>
| <br/>
It can have values between 0-25

_To check IP address of our own computer:_ `curl ifconfig.me -s`

_Image to be added_

- Modem assigns these IP addresses through DHCP
- Modem/Router will decide who requested it. It is done by using NAT - Network Access Translator
- IP Address decides which device to send the data whereas Port numbers are used to identify which application made that request
- Ports are basically 16 bit numbers
- All HTTP stuffs happens at port 80
- MongoDB port - 27017
- `0 - 1023` --> Reserved Ports <br/>
  `1024 - 49152` --> Registered for applications <br/>
   Remaining is for our use
   
**Speed:**
- `1 mbps` 1000000 bits/s
- `1 gbps` 10^9 bits/s
- `1 kbps` 1000 bits/s

**How computers get connected?** <br/>
Physically: Optical Fibre Cables, Coaxical Cables
Wireless: Bluetooth, WiFi, 4G, LTE, 5G

[submarinecable.com](submarincecable.com)

## LAN, MAN, WAN
- `LAN` Local Area Network <br/>
   It interconnects computer within a limited area such as a residence, school, university etc 
- `MAN` Metropolitan Area Network <br/>
   It interconnects users with computer resources in a geographic region of the size of a metropolitan areas such as cities.
- `WAN` Wide Area Network
   It extends over large geographic area such as countries.
   
**SONET:** Synchronous Optical Networking
**Frame relay:** A wave for connecting local area network to the wide area like internet

## MODEM, ROUTER

**Modem** is a combined device for modulation and demodulation. It is used to convert digital to analog and vice-versa.

**Router** is a device that forwards data packets between computer network.

**ISP:** Internet Service Provider are companies that provide us access to the internet
TIER-1: TATA, TIER-2: Airtel, Idea

## Topologies

- **Bus Topology:** <br/>
  a. They are connected through a single cable known as backbone cable.<br/>
  b. If one part gets broken entire system will fail. <br/>
  c. Only 1 person at a time can send information. <br/>
  d. It is mainly used in 802.3 (ethernet) and 802.4 standard networks.
  
  ![image](https://user-images.githubusercontent.com/74575612/151399039-ec286d6b-99d3-4b97-ae66-8df9cc0160c7.png)

  
- **Ring Topology:** <br/>
  a. Ring Topology is like bus topology, but with connected ends. <br/>
  b. It's unidirectional, the data flows in one direction. <br/>
  c. It has no terminated ends. <br/>
  d. Every system communicates with one another. <br/>
  e. If one of the cables break we won't be able to send data. <br/>
  f. A lot of unnecessary calls are made. <br/>
  g. The data in a ring topology flow in a clockwise direction.
  
  ![image](https://user-images.githubusercontent.com/74575612/151399571-87d95804-5218-46f7-9e2c-994ac278e012.png)

  
- **Star Topology:** <br/>
  a. It is an arrangement of the network in which every node is connected to the central hub, switch or a central computer. <br/>
  b. There will be one central device that will be connected to all computers <br/>
  c. If central device fails, then the system will go down. <br/>
  d. The central computer is known as a _server_, and the peripheral devices attached to the server are known as _clients._ <br/>
  e. Coaxical cable or RJ-45 cables are used to connect the computers. <br/>
  
  ![image](https://user-images.githubusercontent.com/74575612/151400158-40a2e57e-4865-4d10-97a6-4d305b8bb614.png)

- **Tree Topology:** <br/>
  a. It combines the characterisitcs of bus topology and star topology. <br/>
  b. A tree topology is a type of structure in which all the computers are connected with each other in hierarchical fashion. <br/>
  c. The top most node in the tree topology is known as a root node, and all other nodes are the descendants of the root node. <br/>
  
  ![image](https://user-images.githubusercontent.com/74575612/151400777-7fb41cba-c91a-42d6-8dcc-954ce44ac3f9.png)

- **Mesh Topology:** <br/>
  a. Mesh Topology is an arrangement of the network in which computers are interconnected with each other through various redundant connections. <br/>
  b. Every single computer will be connected to every single computer. <br/>
  c. It is mainly used for WAN implementations where communication failures are a critical concern. It is mainly used for wireless networks. <br/>
  d. Internet is an example of the mesh topology. <br/>
  e. Expensive and Scalability issues <br/>

![image](https://user-images.githubusercontent.com/74575612/151401537-134221c4-f6cd-4940-8470-dff60f78eb5a.png)

- **Hybrid Topology:** <br/>
  a. The combination of various different topologies is known as Hybrid topology. <br/>
  b. It is a connection between different links and nodes to transfer the data. <br/>
  
  ![image](https://user-images.githubusercontent.com/74575612/151401937-2b88d5c6-3bee-4d90-94a3-3e38bf70e9ee.png)

## TCP/IP Model
It is basically known as **Internet Protocol Suite** <br/>

There are 5 layers:
- Application Layer
- Transport Layer
- Network Layer
- Datalink Layer
- Physical Layer

## Structure of Network OSI Model
There are seven layers in OSI Model:

![image](https://user-images.githubusercontent.com/74575612/151403496-2d28ecce-f65f-473a-abdc-6d84ad8aed13.png)

| Layers             | Description |
| ------------------ | ----------- |
| Application Layer  | Implemented in software, it is just the application like browser, chat apps etc. |
| Presentation Layer | It converts those messages, data into binary format. Encoding, Encryption happends, provides Abstraction, Compression and Translation. |
| Session Layer      | It helps in setting up and managing the connections and enables sending and receiving of data followed by terminationo of connected session. Authentication and Authorization takes place. |
| Transport Layer    | Data receieved from session layer is divided into small data units called segment. Every segment has source and destination's port as well as sequence number. Flow Control & Error Control. |
| Network Layer      | The transmission of the received data segments from one computer to another that is located in different network. IP addressing  done here is called Logical Addressing. Routing is performed and Load Balancing is done. |
| Datalink Layer     | Physical addressing is done here. Mac addresses are physical address. Now, these addresses of sender and receiver are assigned to packets called frames. |
| Physical Layer     | Hardwares like Cables, Wires, etc. |

![image](https://user-images.githubusercontent.com/74575612/151405962-3de83226-de93-4582-b653-869fc1a7e4c1.png)

**Mac Address:** It is a 12 digit alphanumeric number of network interface of computer.

## Client-Server Architecture
- A server is basically a system that controls the website you are hosting.
- The application has two parts: Client part and Server part <br/>
  These are known as processes and they communicate through each other.
- Clients are the ones who are using/cosuming these resources like we making a request to google.
- Data Center is a collection of huge number of computers. It may have static IP addresses. They have good internet connection and high upload speed.

Command: `ping google.com`

**ping** measures the round trip time for messages send from the originating host to the destination computer and are echoed back.

![image](https://user-images.githubusercontent.com/74575612/151407044-1bc6b86b-f18d-4b9a-8960-501f9cce76ab.png)

## Peer-To-Peer Architecture:
- Peer-To-Peer network is a network in which all the computers are linked together with equal privileges and resposibilities for processing the data.
- It is useful for small environments, usually up to 10 computers.
- It has no dedicated server.
- Here, every single computer can be termed as a client as well as a server.
- The key advantage is we can scale it rapidly.
- Special permissions are assigned to each computer for sharing the resources, but this can lead to a problem if the computer with the resource is down.

![image](https://user-images.githubusercontent.com/74575612/151407582-043b0a38-7fe6-4818-95c1-cff4c00dd473.png)

## Repeater
A repeater is a dynamic network device used to reproduce the signals when they transmit over a greater distance so that the signal’s strength remains equal. It can be used to create an Ethernet network. A repeater that occurs as the first layer of the OSI layer is the physical layer.

**Features of Repeater:**
- These repeaters are linked to each other at the physical layer.
- It sends the signals for the unsteady areas to enlarge the system signals.
- These repeaters can eliminate the distance between two devices.

**Advantages of Repeater:**
- These repeaters are cost-effective and easy to use.
- The repeater provides the stabiility of the signals.

**Disadvantages of Repeaters:**
- They cannot connect two distinct networks.
- While amplifying the signals, the repeaters also amplify the level of noise in those signals.

## Hub
Hubs are networking devices operating at a physical layer of the OSI Model that are used to connect multiple devices in a network. They are generally used to connect computers in a LAN.

A hub has many ports in it. <br/>

A computer which intends to be connected to the network is plugged in to one of these ports. When a data frame arrives at a port, it is broadcast to every other port, without considering whether it is destined for a particular destination device or not.

**Features of Hub:**
- A hub operates in the physical layer of the OSI model.
- A hub cannot filter data, It only sends message to all ports.
- It primarily broadcasts messages. So, the collision domain of all nodes connected through the hub stays one.
- Collisions may occurs during setup of transmission when more than one computer's place data simultaneously in the corresponding ports.

**Types of Hubs:**
- **Active Hubs:** amplify and regenerate the incoming electrical signals before broadcasting them <br/>
  They have their own power supply and serves both as a repeater as well as connecting centre. Due to their regenerating capabilities, they can extend the maximum distance between nodes, thus increasing the size of LAN.
  
- **Passive Hubs:** connects nodes in a star configuration by collecting wiring from nodes. <br/>
  They broadcast signals onto the network without amplifying or regenerating them. As they cannot extend the distance between nodes, they limit the size of the LAN.

- **Intelligent Hubs:** are active hubs that provide additional network management facilities. <br/>
They can perform a variety of functions of more intelligent network devices like network management, switching, providing flexible data rates etc.

## Bridges
Bridges are used to connect two subnetworks that use interchangeable protocols. It combines two LANs to form an extended LAN.

The main difference between the bridge and repeater is that the bridge has a penetrating efficiency.

**Working of Bridges:**
A bridge accepts all the packets and amplifies all of them to the other side. The bridges are intelligent devices that allow the passing of only selective packets from them. <br/>

A bridge only passes those packets addressed from a node in one network to another node in the other network.

![image](https://user-images.githubusercontent.com/74575612/151418045-6ce1f5ea-1284-488e-b22b-2079edc1c297.png)

- A bridge receives all the packets or frame from both LAN (segment) A and B.
- A bridge builds a table of addresses from which it can identify that the packets are sent from which LAN (or segment) to which LAN.
- The bridge reads the send and discards all packets from LAN A sent to a computer on LAN A and that packets from LAN A send to a computer on LAN B are retransmitted to LAN B.
- The packets from LAN B are considered in the same method.

**Types of Bridges:**
- **Transparent Bridges:** These are the bridges in which the stations are completely unaware of the bridge's existence. i.e. whether or not a bridge is added or deleted from the network, reconfiguration of the stations is unnecessary. <br/>
  These bridges makes use of two processes; bridge forwarding and bridge learning.
 
- **Source Routing Bridges:** In these bridges, routing id performed by source stations and the frame specifies which route to follow. <br/>
  The host can discover frame by sending a special frame called _discovery frame_, which spreads through the entire network using all possible paths to destination.

**Uses of Bridges:**
- Bridges are used to divide large busy networks into multiple smaller and interconnected networks to improve performance.
- Bridges also can increase the physical size of a network.
- Bridges are also used to connect a LAN segment through a synchronous modem relation to another LAN segment at a remote area.

## Switches
Switches are networking devices operating at layer 2 or a data link layer of the OSI model. They connect devices in a network and use packet switching to send, receive or forward data packets or data frames over the network. <br/>

A switch has many ports, to which computers are plugged in. When a data frame arrives at any port of a network switch, it examines the destination address, performs necessary checks and sends the frame to the corresponding device(s).It supports unicast, multicast as well as broadcast communications.

**Features of Switches:**
- A switch operates in the layer 2, i.e. data link layer of the OSI model.
- It is an intelligent network device that can be conceived as a multiport network bridge.
- It uses MAC addresses to send data packets to selected destination ports.
- It uses packet switching technique to receive and forward data packets from the source to the destination device.
- It supports unicase, multicast and broadcast communications.
- Switches are active devices, equipped with network software and network management capabilities.
- Switches can perform some error checking before forwarding data to the destined port.
- The number of ports is higher -24/48.

**Types of Switches:**
- **Unmanages Switch:** These are inexpensive switches commonly used in home networks and small businesses. They can be set up by simply plugging in to the network, after which they instantly start operating.

- **Managed Switch:** These are costly switches that are used in organisations with large and complex networks, since they can be customized to augment the functionalities of a standard switch.

- **LAN Swithch:** LAN switches connects devices in the internal LAN of an organization. They are also referred as Ethernet switches or data switches. These switches are particularly helpful in reducing network congestion or bottlenecks. They allocate bandwidth in a manner so that there is no overlapping of data packets in a network.

- **PoE Switch:** switches are used in PoE Gogabit Ethernets. PoE technology combine data and power transmission over the same cable so that devices connected to it can receive both electricity as well as data over the same line. PoE switches offer greater flexibility and simplifies the cabling connections

## Router
A router is a device like switch that routes data packets based on their IP addresses. It is mainly a network layer device. Routers normally connects LAN and WANs together and have a dynamically updating routing table based on which they make decisions on routing the data packets. 

## Gateway
 gateway is a network node that forms a passage between two networks operating with different transmission protocols. The most common type of gateways, the network gateway operates at layer 3, i.e. network layer of the OSI (open systems interconnection) model. <br/>
 
It acts as the entry – exit point for a network since all traffic that flows across the networks should pass through the gateway. Only the internal traffic between the nodes of a LAN does not pass through the gateway.

**Features of Gateway:**
- Gateway is located at the boundary of a network and manages all data that inflows or outflows from that network.
- It forms a passage between two different networks operating with different transmission protocols.
- A gateway operates as a protocol converter, providing compatibility between the different protocols used in the two different networks.
- It also stores information about the routing paths of the communicating networks.
- It uses packet switching technique to transmit data across the networks.

**Brouter:**
A brouter is a networking device that functions both as a bridge and a router. It can forward data between networks (serving as a bridge), but can also route data to individual systems within a network (serving as a router). <br/>

It operates either at Data link layer or a Network layer. <br/>
It stores routing table when it is configured as a router and stores MAC address when configured as a bridge. <br/>

It works on more than one broadcast domain when it is configured as a router and It works on single broadcast domain when configured as a bridge.

## TCP/IP (Web Protocols)
- **HTTP:** Hyper Text Transfer Protocol
- **DHCP:** Dynamic Host Control Protocol
- **FTP:** File Transfer Protocol
- **SMTP:** Simple Mail Transfer Protocol, _used to send email_
- **POP3 & IMAC:** _used to receive email_
- **SSH:** Secure Shell
- **VNC:** Virtual Network Computing

**Telnet:** terminal immutation that enables the user to remote host/device using telnet
**UDP:** Stateless connection

## Process, Threads, Sockets, Ports

![image](https://user-images.githubusercontent.com/74575612/151605723-81095217-a07a-4834-8efd-320e4f0f8910.png)


**Process:** is the instance of a computer program that is being executed by one or many threads.

**Thread:** is a single sequence stream within a process. Threads have same properties as of the process so they are called as light weight process.

**Socket:** is one endpoint of a two way communication link between two programs running on the netwo.
The socket mechanisk provies a means of inter-proces communication (IPC) by establishing named contact point between which the communiation take place.

**Port:** is a physical docking point using which an external device can be connected to the computer. It can also be programmatic docking point through which information flows from a program to the computer or over the Internet. <br/>

A network port which is provided by the Transport Layer protocols of Internet Protocol suite, such as Transmission Control Protocol (TCP) and User Diagram Protocol (UDP) is a number which serving endpoint communication between two computers.

IP Address tells us which device we are working with while ports tell us which application we are working with.

Their may be possibility of many processes of single application is running like opening up many tabs in chrome when the response is coming back how it will know which tab to give the data. This can be resolved using EPHEMERAL PORTS.

## HTTP (Hyper Text Transfer Protocol):
- It is a client server protocol and it tells us how we request this data from the server and also tells us how the server sends back to the client.
- When a client makes a request to the server, it is known as an _HTTP Request_. <br/>
  When a server sends back response to the client, it is known as _HTTP Response_.
- These are application layer protocols
- HTTP uses TCP
- It is a stateless protocol; server will not store any information about client by default.

**Method** is basically tells the server what to do

**HTTP Methods**
- **GET:** It means we are requesting some data
- **POST:** Client gives some data to the server like web forms
- **PUT:** Puts data at a specific location.
- **DELETE:** To delete data from the user

**Error/Status Code:** When we send a request to the server, we need some sort of a way to know whether the request is successful or not. <br/>
For this there exists STATUS CODE: <br/>
Ex: 200 - request was successful <br/>
    404 - not found <br/>
    400 - bad request <br/>
    500 - internal server error <br/>

1XX - Informational Category <br/>
2XX - Success Code <br/>
3XX - Redirecting Purpose <br/>
4XX - Client Error <br/>
5XX - Server Error <br/>

## Cookies
- Cookies are files, generally from the visited webpages, which are stored on a user's computer. They hold a small amount of data, specific to a particular client and website, and can be accessed either by the web server or the client computer which can be usernames, password, session token, etc.

- When we visit the web page for the first time, the cookie is set and whenever we make a new request, in the request header a cookie will be sent. <br/>
Then the server will look into the database and identify the state.

**Types of Cookies:**
- **Session Cookies:** hese are mainly used by online shops and allows you to keep items in your basket when shopping online. These cookies expire after a specific time or when the browser is closed.
- **Permanent Cookies:** These remain in operation, even when you have closed the browser. They remember your login details and password so you don’t have to type them in every time you use the site. It is recommended that you delete these type of cookies after a specific time.
- **Third-Party Cookies:** These are installed by third parties for collecting certain information. For example: Google Maps.

## DNS (Domain Name System)
DNS is a directory service that provides a mapping between the name of a host on the network and its numerical address. <br/>

![image](https://user-images.githubusercontent.com/74575612/151667029-dae60cbe-6549-4f6f-a9c9-0e687bb9f03c.png)

![image](https://user-images.githubusercontent.com/74575612/151667233-2e194c15-6001-4d30-8891-ce7687b079cc.png)

**Top Level Domain:** They are like organisation specific Ex: .com for commercial, .edu for education, .uk, .in --> country specific <br/>
These are managed by ICANN INTERNET CORPORATION FOR ASSIGNED NAMES AND NUMBERS

![image](https://user-images.githubusercontent.com/74575612/151667816-3b59b16d-16d4-4803-a9d9-103448fb2515.png)

command: dig google.com <br/>
man dig

## Transport Layer
- Data transferred between one computer to another is done by using Network Layer
- Transport layer is a layer which lies over devices.
- The role of the transport layer is to take the data from the network to application.

  Network Layer: Network <--> Network <br/>
  Transport Layer: Network <--> Abstraction <br/>
- Provides Abstraction
- Located on the devices
- Data Travels in Packets 

  ![image](https://user-images.githubusercontent.com/74575612/151668310-88f49866-d7d8-437f-aa20-151453260b32.png)

- Transport Layer will attach these socket part numbers to that packets
- Transport Layer also takes control of congestion control
- Congestion control algorithms are built in TCP

## Checksum
![image](https://user-images.githubusercontent.com/74575612/151673054-e98720a3-d0e1-4938-a368-c5af04b3eee4.png)


## Timers
![image](https://user-images.githubusercontent.com/74575612/151672670-22dd7e1a-4b9f-4bab-9ee2-4003b1b8e487.png)

## UDP (User Datagram Protocol)
The User Datagram Protocol (UDP) is simplest Transport Layer communication protocol available of the TCP/IP protocol suite. It involves minimum amount of communication mechanism. UDP is said to be an unreliable transport protocol but it uses IP services which provides best effort delivery mechanism.

**Features:**
- UDP is good protocol for data flowing in one direction
- UDP is simple and suitable for query based communications
- UDP is not connection oriented.
- UDP does not provide congestion control mechanism.
- ![image](https://user-images.githubusercontent.com/74575612/151672367-f8c6abcd-7dc4-4171-9493-d65d6769a9e6.png)

UDP header contains four main parameters:
- Source Port: This 16 bits information is used to identify the source port of the packet.
- Destination Port: This 16 bits information, is used identify application level service on destination machine.
- Length: It is 16-bits field and minimum value is 8-byte.
- Checksum: This field stores the checksum value generated by the sender before sending. IPv4 has this field as optional so when checksum field does not contain any value it is made 0 and all its bits are set to zero.

## TCP (Transmission Control Protocol)
It is a transport layer protocol that facilitates the transmission of packets from source to destination. It is a connection-oriented protocol that means it establishes the connection prior to the communication that occurs between the computing devices in a network. <br/>

This protocol is used with an IP protocol, so together, they are referred to as a TCP/IP.

The main functionality of the TCP is to take the data from the application layer. Then it divides the data into a several packets, provides numbering to these packets, and finally transmits these packets to the destination.

The TCP, on the other side, will reassemble the packets and transmits them to the application layer.

Takes control of: 
- when data does not arrive
- maintains the order of data (using sequence number)

**Features:**
- Connection Oriented
- Error Control
- Congestion Control
- Full Duplex

## Three Way Handshake
![image](https://user-images.githubusercontent.com/74575612/151673213-5072d8b2-f42d-4d31-8b05-e948e0f4434e.png)

## TCP (Network Layer)
- In Network Layer we work with routers
- Every router has a network address
- Every router will check whether the packet is for that router, if not then it will forward that using forward table in routing table.

![image](https://user-images.githubusercontent.com/74575612/151671965-1fb8d95a-c488-41f2-9403-bde73571db59.png)

## Control Plane
The control plane is a set of services within the network that perform traffic management functions, including security, routing, load balancing, and analysis.

It is used to build these routing tables:
- Routers --> Nodes
- Links --> Edges

There are two types of Routing used to create tables
1. **Static Routing**
    - Adding address manually
    - It's not adaptive
 
2. **Dynamic Routing**
    - When there is a change in network it will evolve accordingly.
  
## IP (Internt Protocol)
IP stands for Internet Protocol. It is defined in the TCP/IP model used for sending the packets from source to destination.

The main task of IP is to deliver the packets from source to the destination based on the IP addresses available in the packet headers. 

An IP protocol provides the connectionless service, which is accompanied by two transport protocols, i.e., TCP/IP and UDP/IP, so internet protocol is also known as TCP/IP or UDP/IP.

The first version of IP was IPv4. After IPv4, IPv6 came into the market.

## Packets
A packet is a small amount of data sent over a network, such as a LAN or the Internet.

A packet is made up of 2 parts:
- Header: tells the packet where it's going & other housekeeping. It is of 20 bytes
- The data the packet is carrying

**Time To Live:** It is a number after hat number of hops, the packet doesn't reach, then it will leave.


## IPv4 V/S IPv6

| IPv4                           | IPv6                            |
| ------------------------------ | ------------------------------- |
| It has a 32 bit address length | It has a 128 bit address length |
| It supports manual and DHCP address configuration | It supports auto and renumbering address configuration |
| In IPv4 end to end, connection integrity is unachievable | In IPv6 end to end, connection integrity is achievable |
| The security feature is dependent on application | IPSEC is an inbuilt security feature in the IPv6 protocol |
| Address representation of IPv4 is in decimal | Address representation of IPv6 is in hexadecimal |
| In IPv4 checksum field is available | In IPv6 checksum field is not available |
| It has broadcast message transition scheme | In IPv6 multicase and anycast message transmission scheme is available |
| In IPv4 encryption and authentication facility not provided | In IPv6 encryption and authentication are provided |
| IPv4 has a header of 20-60 bytes | IPv6 has header of 40 bytes fixed. |

## Middle Boxes
- They are extra devices that also interact with IP packets.
- Mostly, it will be in network layer but it can also be in transport layer as well.
- It filters out IP Packets based on various rules:
  - Address
  - Modify Packets
  - Port Numbers
  - Flags
  - Protocols

**Types of Firewall:**
- Connected to global internet
- Your local network

**Stateless Firewall:** doesn't maintain a state

**Stateful Firewall:** see the packet and maintain its state, more efficient

## NAT (Network Address Translation)
It is a method of mapping an IP Address space into another by modifying network address information in the IP header of packets while they are in transit across a traffic routing device.

## TCP (Data Link Layer)
Data Link Layer is second layer of OSI Layered Model. <br/>

The data packets that we receive from the network layer. The data link layer is responsible to send these oackets over a physical link.

![image](https://user-images.githubusercontent.com/74575612/151670203-0960ff9b-5f5a-49a7-a20e-6bf54ed34dba.png)

**DHCP:** Dyynamic Host Configuration Tool

In Data Link Layer, the devices communicate with each other using Data Link Layer Address

Let's say device 1 needs to send something to device 4, first it will loop up in its cache. If it does not have then it will ask all other devicees.

This is known as **ARP Cache (Address Resolution Protocol)**

Frame consists of:
- DLLA of sender
- IP Address of destination

**MAC:** Media Access Control

**NOTE:**
Transport --> Segment <br/>
Network --> Packet <br/>
Data Link --> Frames <br/>
