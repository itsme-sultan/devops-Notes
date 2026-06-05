# Networking Notes  
-**CDN** (Content delivery network) : server which serve static data like images and videos. CDN caches copies of your content across multiple servers worldwide.  
When a user requests your site, the CDN serves it from the server closest to them, reducing latency and improving speed.

-**Cache**: Its temporary data center use store static data  
-**Edge location** : location where cache dadte is stored

**Internet Protocal** -  
  There is total 4.3 billion ipv4 address. Ipv4 is limited and not enough for all the devices thats why we have ipv6 address.  
  ipv6 128 bits alphanumeric number consist of Eight groups of four hexadecimal digits separated by colons.  

  ipv6 is a bit complex and difficul to rememeber. Hence they find a way to to continue using ipv4 address.  
  This is how concept of subneting is intoducesd.  
  
**Subnet:**  Dividing large network into small network  

**CIDR (Classless Inter-Domain Routing):**  
its a compact way to write IP address ranges and their network masks.  
2<sup>32-n</sup>
if n=4 the CIDR notation will be /4
if n=28 the cidr notation will be /28, total number of ip address will be 16  
    Network address : first ip address in that subnet  
    Broadcast address : last ip address in that subnet  
    only 14 ip address will be available for use for VIDR notation /28  
e.g: for subnet 192.168.1.0/28  
Network ip address : 192.168.1.0  
broadcast ip address :192.168.1.15  
First Usable IP:192.168.1.1  
Last Usable IP : 192.168.1.14

  
