# Networking and Content Delivery
## Notes 05

### Keypoints
- Networks are two or more client machines that are connected together to share resources
-  OSI Model (Open Systems Interconnection) has 7 layers:
  (7)Application:  Software that is requesting or recieving network communications. This is the layer that users interact with the software app directly (eg. email, web browser)
  (6) Presentation: translates software encoding and human readable format (DOC,JPG) 
  (5) Session: Creates logical connection between the software endpoints. Creates, manages, and terminates connections between local and remote apps (HTTP (80), FTP (21) )
  (4) Transport: segments traffic for better transmission between hosts. (TCP, UDP)
  (3) Network: configures packets for intra- and inter- subnet communications. Provides the procedural means of transerring packets of data from one node to another, connected in different networks. 
  (2) Data Link: Provides node-to-node data transfer between two connected nodes (MAC Address)
  (1) Physical: Converts data into appropriate format (hubs, )
 - OSI Model demonstrates the route of communication between the network

### 7.02 Computer Networking
- Computer Network is the interconnection of multiple devices using multiple mediums to communicate between two different devices. These devices are called Network Devices ( Hub, Router, Switch, etc)
- Protocols are a set of rules that define how two networks can communicate. (eg. TCP, IP, UDP, ARP, DHCP, FTP)
- IP Address (Internet Protocol Address): network address of the system across the network
- IANA (Internet Assigned Numbers Authority) assigns IPv4 (32-bits) for each device on the Internet. Some are assigned IPv6.
- Classless Inter-Domain Routing (CIDR) : consists of IP address, a slash, and a number that represents how many bits of routing prefix. ( eg. 192.0.2.0/24 ). The last number of the CIDR address represents 24 fixed (unchangeable) bits. The internet's IP address is 0.0.0.0/0
- Ports are a channel in white data can be sent or received to an application.
- Socket: IP Address and Port number together
- DNS: Domain Name System is the website URL
- ARP: Address Resolution Protocol is used to convert IP into a physical address/ RARP is the opposite
- Three layers of the internet are: Application layer ( URL, HTTPS), Transport Layer: communication over networks, Network layer: provides data route

### Understanding TCP/IP Addressing and subnet basics
- TCP/IP has the ability to connect networks all around the Internet.
- Subnet mask is used to divide IP address in two parts (one part identifies computer, other identifies network.
### Amazon VPC
- Amazon Virtual Private Cloud lets you isolate a section of the AWS Cloud and use it to launch resources in a private network. You have the ability to chose your own IP Address range and have full control over your networks, subnets and route tables.
- you  can launch EC2 instances in your VPC and access across multiple AZ's in the same Region
- Elastic Network Interfaces: AWS ENIs attach virtual network cards to your instances which helps facilitate network connectivity for those instances. Cannot detach primary network interface from an instance.
- VPC Route Tables: table that has a set of routes/rules that Determines where information from your subnet or gateway is headed. Each subnet in your VPC must be associated with a route table. Subnet can't have multiple tables, but tables can be associated with multiple subnets.
- Internet Gateway allows communication between your VPC and the internet. Internet Gateway alows NAT (Network Address Translation) and internet routable traffic.
- can also enable VPC sharing

### AWS Direct Connect
- Helps you connect to a data center even if you are far away from a data center
- AWS PrivateLink helps you connect your VPC without requiring a internet gateway, NAT or AWS Direct Connect.
- AWS Transit Gateways: connects VPC's and on-premise networks through a central hub, simplifies your network.
- Security Groups act as firewall for your instance to control inbound and outbound data.
- Network Access Control Lists (ACL) is extra security layer for your VPC that controls traffic in and out of subnets.

### Amazon CloudFront
- CloudFront is a content delivery network that delivers data, media and applications with low latency and high speed. Delivers content through network data centers ( edge centers).
- Using CloudFront is cost effective and fast.
