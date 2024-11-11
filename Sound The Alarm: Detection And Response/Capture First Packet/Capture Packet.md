# Capture Packets

## This lab consists of using tcpdump to capture network traffic

### Scenario

You are a network analyst who needs to use tcpdump to capture and analyze live network traffic from a Linux virtual machine.

```bash
sudo ifconfig
    identify the interfaces that are available
sudo tcpdump -D

sudo tcpdump -i eth0 -v -c5
    -i eth0: Capture data specifically from the eth0 interface.
    -v: Display detailed packet data.
    -c5: Capture 5 packets of data.

In the example data at the start of the packet output, tcpdump reported that it was listening on the eth0 interface, and it provided information on the link type and the capture size in bytes:
tcpdump: listening on eth0, link-type EN10MB (Ethernet), capture size 262144 bytes
On the next line, the first field is the packet's timestamp, followed by the protocol type, IP:
22:24:18.910372 IP
The verbose option, -v, has provided more details about the IP packet fields, such as TOS, TTL, offset, flags, internal protocol type (in this case, TCP (6)), and the length of the outer IP packet in bytes:
(tos 0x0, ttl 64, id 5802, offset 0, flags [DF], proto TCP (6), length 134)
The specific details about these fields are beyond the scope of this lab. But you should know that these are properties that relate to the IP network packet.

In the next section, the data shows the systems that are communicating with each other:
7acb26dc1f44.5000 > nginx-us-east1-c.c.qwiklab

sudo tcpdump -i eth0 -nn -c9 port 80 -w capture.pcap &

This command will run tcpdump in the background with the following options:
-i eth0: Capture data from the eth0 interface.
-nn: Do not attempt to resolve IP addresses or ports to names.This is best practice from a security perspective, as the lookup data may not be valid. It also prevents malicious actors from being alerted to an investigation.
-c9: Capture 9 packets of data and then exit.
port 80: Filter only port 80 traffic. This is the default HTTP port.
-w capture.pcap: Save the captured data to the named file.
&: This is an instruction to the Bash shell to run the command in the background.

&: This is an instruction to the Bash shell to run the command in the background

curl opensource.google.com
ls -l capture.pcap

sudo tcpdump -nn -r capture.pcap -v
sudo tcpdump -nn -r capture.pcap -X
```
