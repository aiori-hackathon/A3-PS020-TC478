# AIORI-3 Hackathon: SRv6 Automated Path Failover Simulation

**Author:** Purushottam Dattatray Lokhande
**Project Introduction Video:** https://youtube.com/shorts/8BPljv1aMzc?si=smfUOnd0O37zsrJC  A3-PS020-TC478

## Overview
This repository contains the final network demonstration for the AIORI-3 Hackathon. It features an IPv6 network topology with simulated Segment Routing (SRv6) traffic engineering and automated failover rerouting.





**Project Demonstration:** 

## Simulation Logic
To provide a stable and visual proof-of-concept, explicit SRv6 paths are modeled using Administrative Distance (AD) floating static routes to demonstrate primary and backup policy switching. 
- **Primary Path (Metric 10):** R1 -> R2 -> R3 -> R5
- **Backup Path (Metric 20):** R1 -> R4 -> R5


## Submission Artifacts
* `SRv6_Failover_Demo.pkt`: The live Cisco Packet Tracer simulation workspace demonstrating the automated failover.
* `Proposed-structure-hackathon.pdf`: Technical documentation, including routing table proofs and continuous ping metrics.
* `failover_demo.mp4`: Live screen capture of the zero-downtime path recovery.
* `auto_demo.py`: Experimental Mininet SDN script for native Linux environments.
