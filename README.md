Network Packet Sniffer:

This Python program utilizes the Scapy library to sniff and analyze network packets in real-time. Here's how it works:

Importing Scapy: The program starts by importing the scapy.all module, which provides comprehensive tools for packet manipulation.

Packet Callback Function: The packet_callback function is defined to handle each captured packet. It checks if the packet contains an IP layer (scapy.IP) and extracts relevant information such as source and destination IP addresses (src_ip, dst_ip) and the protocol (protocol).

Printing Packet Information: The program prints out the source IP, destination IP, and protocol of each captured packet.

Payload Analysis: If the packet contains a TCP or UDP layer (scapy.TCP or scapy.UDP), it attempts to extract and decode the payload. If decoding is successful, it prints the payload type (TCP Payload or UDP Payload); otherwise, it indicates that the payload decoding was unsuccessful.

Start Sniffing Function: The start_sniffing function initiates the packet sniffing process using the scapy.sniff method. It sets store=False to prevent storing packets in memory and specifies the packet callback function (prn=packet_callback) to handle each captured packet.

Execution: Finally, the program calls the start_sniffing function to begin sniffing network packets.

Note: Ensure that you have the necessary permissions to sniff network traffic, as this program requires elevated privileges. Additionally, handle the captured data with caution, as it may contain sensitive information
