# AIORI-3 Hackathon: SRv6 Automated Path Failover Simulation


**Project Introduction Video:** 

https://youtube.com/shorts/8BPljv1aMzc?si=smfUOnd0O37zsrJC  A3-PS020-TC478


## Overview
This repository contains the final network demonstration for the AIORI-3 Hackathon. It features an IPv6 network topology with simulated Segment Routing (SRv6) traffic engineering and automated failover rerouting.

## Problem Statement
Modern networks require high availability and strict traffic engineering to ensure Quality of Service (QoS). Traditional dynamic routing protocols often suffer from convergence delays during link failures, leading to packet loss. This project demonstrates a traffic steering mechanism that pre-calculates primary and backup paths to eliminate downtime during unexpected network outages.

## Network Topology & Design
The simulation utilizes a 5-router diamond topology serving as the core transit network between two endpoints (PC1 and PC5). 
* **Edge Routers:** R1 (Source) and R5 (Destination) handle the path steering logic.
* **Transit Routers:** R2, R3, and R4 act as the provider core forwarding the IPv6 traffic.

## Technology Stack
* **Simulation Environment:** Cisco Packet Tracer
* **Protocols:** IPv6, Static Routing, ICMPv6
* **Experimental / SDN:** Python (Mininet/FRRouting scripts for native Linux environments)

## Future Enhancements
While the current simulation relies on reactive routing metrics, future iterations will integrate a hybrid network diagnostic engine to monitor traffic patterns and interface health. This allows the system to proactively steer the SRv6 path before a hard link failure occurs.



##

**Project Demonstration Results and Working Video:**

https://drive.google.com/file/d/1Iex-H56wQw4wvJ3ZzDbC6UuMgZHYtzwh/view?usp=drive_link


## Simulation Logic
To provide a stable and visual proof-of-concept, explicit SRv6 paths are modeled using Administrative Distance (AD) floating static routes to demonstrate primary and backup policy switching. 
- **Primary Path (Metric 10):** R1 -> R2 -> R3 -> R5
- **Backup Path (Metric 20):** R1 -> R4 -> R5


## Submission Artifacts
* `SRv6_Failover_Demo.pkt`: The live Cisco Packet Tracer simulation workspace demonstrating the automated failover.
* `Proposed-structure-hackathon.pdf`: Technical documentation, including routing table proofs and continuous ping metrics.
* `failover_demo.mp4`: Live screen capture of the zero-downtime path recovery.
* `auto_demo.py`: Experimental Mininet SDN script for native Linux environments.
