# Analyze Packets

## This lab consists of assessing and analyzing network traffic in order to learn what type of traffic is being sent to and from systems on the networks

### Scenario

In this scenario, you’re a security analyst investigating traffic to a website.

You’ll analyze a network packet capture file that contains traffic data related to a user connecting to an internet site. The ability to filter network traffic using packet sniffers to gather relevant information is an essential skill as a security analyst.
You must filter the data in order to:

- identify the source and destination IP addresses involved in this web browsing session
- examine the protocols that are used when the user makes the connection to the website
- analyze some of the data packets to identify the type of information sent and received by the systems that connect to each other when the network data is captured.

```bash
.pcap file extension for wireshark packet capture files

No. : The index number of the packet in this packet capture file
Time: The timestamp of the packet
Source: The source IP address
Destination: The destination IP address
Protocol: The protocol contained in the packet
Length: The total length of the packet
Info: Some infomation about the data in the packet (the payload) as interpreted by Wireshark

ip.addr == 142.250.1.139

The upper section of this window contains subtrees where Wireshark will provide you with an analysis of the various parts of the network packet. The lower section of the window contains the raw packet data displayed in hexadecimal and ASCII text. There is also placeholder text for fields where the character data does not apply, as indicated by the dot (“.”).

first subtree in packet (Frame)
    This provides you with details about the overall network packet, or frame, including the frame length and the arrival time of the packet. At this level, you’re viewing information about the entire packet of data.

Ethernet 2
    This item contains details about the packet at the Ethernet level, including the source and destination MAC addresses and the type of internal protocol that the Ethernet packet contains.
    when you filter by MAC address with eth.addr, this is where you will look

internet protocol version 4
    This provides packet data about the Internet Protocol (IP) data contained in the Ethernet packet. It contains information such as the source and destination IP addresses and the Internal Protocol (for example, TCP or UDP), which is carried inside the IP packet.

transmission control protocol
    This provides detailed information about the TCP packet, including the source and destination TCP ports, the TCP sequence numbers, and the TCP flags.

TCP flags

ip.src == 142.250.1.139
ip.dst == 142.250.1.139
eth.addr == 42:01:ac:15:e0:02

Domain Name System
    Queries
        shows lookup for sites
    Answers
        The Answers data includes the name that was queried (opensource.google.com) and the addresses that are associated with that name.

udp.port == 53

tcp.port == 80

tcp contains "curl"
    This filters to packets containing web requests made with the curl command in this sample packet capture file.
```
