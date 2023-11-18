## 📚 Desain VLAN

**Author:** Ceb  
**Date:** November 18, 2023

### Model Network Hierarhy
Suatu pendekatan untuk membuat infrastruktur jaringan. Memanfaatkan desain model hirarki dapat memudahkan **proses manajemen** dan **proses expansi** di masa mendatang.    
Model ini membagi 3 layer yang masing masing memiliki fungsi spesifik
1. **Access Layer**, The Access Layer is the entry point for end-user devices, providing network access to devices such as computers, printers, and IP phones. There are principles in this Layer   
    - Port density and user connectivity are priorities.
    - VLAN assignment and basic security features (e.g., port security) are implemented at this layer.
    - Typically uses switches to provide connectivity to end devices.
    - Segmentation of user groups into different VLANs is common.

2. **Distribusi Layer**, The Distribution Layer aggregates traffic from the Access Layer and provides connectivity to the Core Layer. It is responsible for implementing policies, routing between VLANs, and filtering traffic.
    - Aggregates and filters traffic to ensure efficient communication between different parts of the network.
    - Implements routing, access control lists (ACLs), and other policies.
    - Provides a level of isolation and segmentation between different parts of the network.
    - Enhances network security and manages broadcast domains.

3. **Core Layer**, The Core Layer is the high-speed backbone of the network, responsible for fast and efficient packet switching between different parts of the network
    - Designed for high-speed, low-latency forwarding of traffic.
    - Redundancy and high availability are critical to prevent network disruptions.
    - Typically uses routers or high-capacity switches.
    - Avoids unnecessary processing and complexity to ensure rapid packet forwarding.
  
The hierarchical model follows the "pervasive" design principle, meaning that each layer's design principles apply uniformly throughout the network. It also emphasizes the separation of concerns, allowing each layer to focus on specific functions. This modular and layered approach makes the network easier to design, implement, and manage, and it provides scalability for future growth.

### Fitur-Fitur Switch 
<p align="center">
    <img witdh="150" height="150" src="https://github.com/Arsneaz/EduVault/assets/96061442/2e077f47-8593-41c0-b915-af1d85cdbe57">
</p>

