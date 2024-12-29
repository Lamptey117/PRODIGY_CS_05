# PRODIGY_CS_05
Network Packet analyzer
  Network Packet Analyzer Project

Project Overview

This project is a simple Python-based network packet analyzer designed to capture and analyze network packets. The primary focus is on understanding network traffic by displaying details such as source and destination IP addresses, protocols, and payload data.

Features

Captures live network traffic.

Displays essential packet details like IP addresses, protocols, and payloads.

Educational and lightweight tool for learning about network traffic analysis.

Prerequisites

Python 3.x installed on your system.

Administrative/root privileges to capture network packets.

Ethical and legal usage of this tool.

Required Libraries

scapy

Installation: Run the following command:

pip install scapy

How to Run

Clone or download this repository to your local machine.

Install the required library (scapy).

Open a terminal and navigate to the folder containing the script.

Run the script using:

sudo python packet_sniffer.py

Note: Replace sudo with Run as Administrator on Windows.

File Structure

.
├── packet_sniffer.py    # Python script for the network analyzer
└── README.md            # Project documentation

Code Explanation

packet_sniffer.py

This script uses the scapy library to capture and display packet details:

sniff(): A function from Scapy that captures packets based on provided filters.

process_packet(): Custom function to extract and display key packet details.

Example Code Snippet

from scapy.all import sniff

def process_packet(packet):
    if packet.haslayer("IP"):
        print(f"Source: {packet['IP'].src}, Destination: {packet['IP'].dst}, Protocol: {packet.proto}")

sniff(filter="ip", prn=process_packet, count=10)  # Captures 10 packets

Ethical Guidelines

This tool must only be used in environments where you have explicit permission to monitor network traffic. Unauthorized use of packet sniffing tools is illegal and unethical.

Legal Disclaimer

This project is intended for educational purposes only. The authors are not responsible for any misuse or illegal activities conducted using this program. Always ensure you have proper authorization before using network analysis tools.

References

Scapy Documentation

Wireshark Network Analysis Basics

Future Enhancements

Add support for additional protocols such as TCP and UDP.

Implement real-time packet filtering based on user-defined criteria.

Create a GUI for easier packet analysis.

