# Task 4.1 - Networking fundamentals  
  
### Topology 1  
  
Topology 1 was created. IP addresses were assigned according to the table:  
| PC n 	| IP address 	|
|-	|-	|
| PC0 	| 192.168.0.1 	|
| PC1 	| 192.168.0.2 	|
| PC2 	| 192.168.0.3 	|
| PC3 	| 192.168.0.4 	|
  
SIMPLE PDU (Protocol Data Unit) was created and resulted in succesful delivery.  
![Topology 1](screenshots/4.1.1-2.png)  
  
Pinging from one workstation to another works as well.  
While stations have theirs IPs set this behaviour won't change.  
  
![Topology 1-hub](screenshots/4.1.1.png)  
  
Simulation showed all the animation of ICMP packets being re-transmitted from the hub and receiving the answer from targeted PC.  
ICMP packets belong to OSI Layer 3, as shown in PDU information windows for a specific packet.  
  
![](screenshots/4.1.2.png)  
  
***
  
### Topology 2.  
  
This topology uses *switch* instead of hub. Switches incorporate the ability to send packets directly to the IP address, because they store the a simple routing table of the connected workstation and their MAC addresses to its ports. Thus reducing network traffic and network equipment loads.  
  
![Switch is present](screenshots/4.1.3.png)  
  
***
  
### Topology 3  
  
Another topology was built. IP addresses were assigned, gateways set and router ports were turned on. This configuration allows to connect different networks into one cluster, thus expanding coverage and keeping network traffic within limits. Also routers allow fast network scalability. And in case there are many routes from one network to another routers can determine the best route to destination. It is possible by having metric characteristics in routing tables.  
  
![Router is present](screenshots/4.1.4.png)  
  
Router is able to share a single IP address for the whole network and mask its infrastructure from external access, which in turn enhances security.  
  
***  
**Navigation:**  
[Previous: Task 3.1](https://github.com/frost9i/DevOps_online_Kharkiv_2020Q42021Q1/blob/main/m3/task3.1/README.md) | [Next: Task 4.2](https://github.com/frost9i/DevOps_online_Kharkiv_2020Q42021Q1/blob/main/m4/task4.2/README.md)  
  