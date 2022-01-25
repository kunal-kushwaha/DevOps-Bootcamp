# [Computer Networking](https://www.youtube.com/watch?v=IPvYjXCsTg8) Notes

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
