# SME-Network-Architecture-Design-and-Implementation
This project aims to design, build, and test a Small-medium business network (SME) using Cisco Packet Tracer

Network Architecture Contents:

Network -

The SME hosts three departments, Engineering, Sales, and Management. The Engineering group initially has 300 computers; these are divided into 260 staff computers. The remaining 40 are production servers. These are deployed in groups of 5, i.e., 8 groups. Each group has two servers deployed in hot-swap load-balancing; the remaining three are used for service production. Using this basic production unit, the service can scale (add more prod units), and there is resilience since both load balancers and production are duplicated. The customer load is divided equally among the Prod servers, while the load balancers are run in hot-standby. I.e., there is only one serving the customers, but if that fails or needs to be shut down for maintenance, the other takes over directly.   

 
![Network-design](https://github.com/user-attachments/assets/5f8039a5-61d0-4e72-8ff1-7f75bb54dfa7)

The sales group consists of a back-office of around 10 people; here 4 are technical writers working on documentation and adaptation of documentation, 4 are working as customer support (close cooperation with Engineering group and customers), the last 2 are salespeople that work in the office. In addition to the back-office, the company has around 20 contracted salespeople travelling the world (these are rotated back to the office once every few years). The contracted salespeople are responsible for buying their laptops and peripherals, but they need to set up VPN connections to the main office to do their internal work. Hence, the network for the sales group has four different types of use; writing (4 computers), customer-support (4 computers), visiting-sales (30 computers, each salesperson has a physical desktop in the office), and a VPN server (using an SPU deployment just as in production to ensure operations). The VPN traffic is moderate, at most 30 customers/h. However, they generate around 10Mbps in/out traffic when they are active (using remote desktop). Once a remote salesperson connects, they can start a remote desktop connection to their on-site desktop.  

The management consists of a small team of five people; Chief Executive Officer (CEO), Technical Lead (TL, engineering manager), Sales Lead (SL, sales manager), Economic officer, and a secretary. Each has a computer or two for (CEO, TL, and SL).  

In addition to this, some shared resources cover all/some of the groups; 10 printers cover all groups, 2 file servers cover sales and management.  

 

 
