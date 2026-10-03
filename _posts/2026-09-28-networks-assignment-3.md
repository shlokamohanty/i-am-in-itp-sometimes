---
layout: post
title: assignment three and readings
subtitle: ""
date: 2026-09-28
tags: networks-ongoing
---

![wireshark](/i-am-in-itp-sometimes/assets/images/wireshark.jpg)

When I was searching up ```http```, it showed me ```http2``` and ```http3```. I don't know the difference between ```http2``` and ```http3```. I did have around 

32 ```http``` packets.

When I filtered for ```ssh``` I didn't have any results.

I didn't have results for  ```icmp``` but I had results for  ```icmpv6 ```. I'm not sure what the difference between the two is. I had about 242 packets.

![icmpv6](/i-am-in-itp-sometimes/assets/images/icmpv6.jpg)

I looked up ```dns``` which was around 134 packets. I had none for  ```dnsserver```.

I had none for ```smtp```.

In trying to answer this question: 'How much is from remote hosts attempting  to access ports or services you don’t have open?'

I came across 'endpoints' in Wireshark.

Again, I'm not exactly sure, if I entirely get it. But this was helpful.

[https://www.geeksforgeeks.org/ethical-hacking/endpoints-in-wireshark/](https://www.geeksforgeeks.org/ethical-hacking/endpoints-in-wireshark/)

![endpoints](/i-am-in-itp-sometimes/assets/images/endpoints.jpg)

---

### What We Should Know about DNS

> The DNS, which stands for Domain Name System, is a hierarchical decentralized naming system for devices(computers, smartphones, etc), services, or other resources connected to the Internet or a private network.

> All devices which are connected to the Internet have IP addresses. Users can access devices if they know the device’s IP address, but sometimes IP addresses are changed by a system.

> The authoritative name servers that serve the DNS root zone, commonly known as the “root servers”, are a network of hundreds of servers in many countries around the world. The Domain Name System(DNS) is composed of the root servers which are managing TLD(Top Level Domain ex: .com, .edu, .net, .org etc) and name servers.

> First, a user inputs a domain on a web browser’s address bar. The browser calls a function which is called Resolver. The resolver sends a request to a DNS server saying that  “I would like to access google.com, so tell me the domain’s IP address.”

### Internet as a public utility?

> While John Perry Barlow’s _Declaration of Independence of Cyberspace_ might have suggested that the internet was a magical space that transcended borders and governments, the internet has very real and physical infrastructure.