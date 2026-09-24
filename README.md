# Name - Osmonov Erjan
# Student ID - 240141017
# Course and selection - COMCEH24
# Date - 24.09.2026
# Instructor - Mr. Tabrej Khan

# Visible Layers - Ethernet, IP, TCP
# Source IP - 145.254.160.237
# Destination IP - 65.208.228.223
# TCP source port - 3372
# TCP destionation port - http
# TCP flags - 5

# Original - http - The original http is 8080 
# Modified 1 - 8080 - We've changed the destination port to 8080
# Modified 2 - 8035 - We've changed the destionation port to 8035

# Questions:

# 1. What does rdpcap() return?
# - It returns a packet list, a collectoin of captured packets

# 2. Why does packets[3] select the fourth packet?
# Pythons uses zero based indexing, starting from 0, so packet[3] is actualy 4th one

# 3. What does p.show() display?
# The fourth captured packet's layers, fields and values in certain way

# 4. What is the purpose of the slash operator?
# In scapy / is used to stack layers into one packet

# 5. How does IP()/TCP() differ from IP()/UDP()/DNS()?
# First one creates ip packet with tcp layer, the second one creates ip packet with udp and dns layers

# 6. Why check TCP in p before p[TCP]?
# To check if the packet contains the tcp layer, otherwise it might cause an error

# 7. Does modifying dport transmit a packet? Explain.
# No, it only changes the packet in memory, you ahve to send it to transmit

# 8. Why copy a captured packet before modifying it?
# To have a copy of an original file, in case of corrupting or etc

# 9. Which layer contains payload bytes here?
# The RAW layer contains the payload

# 10. Why must an IP address be written as a string?
# It is represented as text in scapy.

# Index 1
# Layers - Ethernet, IP, TCP, 
# Src to dst - 145.254.160.237 -> 65.208.228.223
# Protocol and ports - TCP protocol, ports src 3372, dst 80
# Flags or payload - Flag S (SYN), no payload

# Index 7
# Layers - Ethernet, IP, TCP, 
# Src to dst - 145.254.160.237 -> 65.208.228.223
# Protocol and ports - TCP protocol, ports src 3372, dst 80
# Flags or payload - Flag A (ACK), no payload

# Index 8
# Layers - Ethernet, IP, TCP, RAW 
# Src to dst - 65.208.228.223 -> 145.254.160.237
# Protocol and ports - TCP protocol, ports src http, dst 3372
# Flags or payload - Flag A (ACK), payload contains a web/http content
