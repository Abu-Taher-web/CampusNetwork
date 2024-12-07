# Campus Network Design Project

This project demonstrates a network topology designed and implemented in Cisco Packet Tracer. The network consists of three main segments: ICT Building, CSE Department, and Math Department, with interconnectivity across departments enabled via routers and DHCP services.
## Watch the Demo Video

[![Watch the video](https://img.youtube.com/vi/ahmNo4FhRBI/0.jpg)](https://youtu.be/ahmNo4FhRBI?si=J_5PS0tcSHtgy9mu)

## **Network Overview**

### **1. ICT Building**
- **Devices**:
  - **DHCP Server**: `192.168.1.2`
  - **DNS Server**: `192.168.1.3`
  - **Web Server**: `192.168.1.4`
  - **Switch**: Connecting all servers and PCs in the ICT Building.
  - **PCs**: `PC0`, `PC1`
- **Key Feature**:
  - DHCP server provides IP addresses dynamically for the network.

### **2. CSE Department**
- **Devices**:
  - **Switch**: Connecting the router to PCs.
  - **PCs**: `PC2`, `PC3`
- **Key Feature**:
  - Receives IP addresses from the DHCP server located in the ICT Building.

### **3. Math Department**
- **Devices**:
  - **Switch**: Connecting the router to PCs.
  - **PCs**: `PC4`, `PC5`
- **Key Feature**:
  - Also receives IP addresses from the DHCP server in the ICT Building.

## **Inter-Department Connectivity**
- The network uses **three routers** to connect the departments:
  - **Router7**: Connects the ICT Building and CSE Department through a serial link (`10.10.10.0/30`).
  - **Router9**: Connects the CSE Department and Math Department through another serial link (`20.0.0.0/30`).

## **IP Addressing**
- **ICT Building Network**: `192.168.1.0/24`
- **CSE Department Network**: `192.168.2.0/24`
- **Math Department Network**: `192.168.3.0/24`
- **WAN Links**:
  - Between ICT Building and CSE Department: `10.10.10.0/30`
  - Between CSE Department and Math Department: `20.0.0.0/30`

## **Features Implemented**
1. **Dynamic IP Allocation**:
   - The DHCP server in the ICT Building assigns IP addresses to PCs in all departments.
2. **DNS Services**:
   - The DNS server in the ICT Building resolves domain names within the network.
3. **Web Server**:
   - Hosts a sample webpage accessible across all departments.
4. **Routing**:
   - Configured static or dynamic routing on routers to enable inter-department communication.
5. **RIP Protocol**:
   - Implemented RIP protocol for dynamic communication between routers

## **Usage Instructions**
1. Open the project file in Cisco Packet Tracer.
2. Verify the IP configuration of all devices:
   - Check if PCs in all departments have received IP addresses from the DHCP server.
   - Test connectivity using `ping` commands between PCs across departments.
3. Access the web server by typing its IP address (`192.168.1.4`) in any PC's browser.

## **Future Improvements**
- Implement a backup DHCP server for redundancy.
- Introduce VLANs for better segmentation and security.
- Add more departments and scale the topology.

## **Credits**
- **Designed by**: Abu Taher
