---
services: Network
platforms: java
author: selvasingh
---

## Getting Started with Network - Manage Internet Facing Load Balancer - in Java ##


  Azure Network sample for managing Internet facing load balancers -
 
  High-level ...
 
  - Create an Internet facing load balancer that receives network traffic on
    port 80 &amp; 443 and sends load-balanced traffic to two virtual machines
 
  - Create NAT rules for SSH and TELNET access to virtual
    machines behind the load balancer
 
  - Create health probes
 
  Details ...
 
  Create an Internet facing load balancer with ...
  - A frontend public IP address
  - Two backend address pools which contain network interfaces for the virtual
    machines to receive HTTP and HTTPS network traffic from the load balancer
  - Two load balancing rules for HTTP and HTTPS to map public ports on the load
    balancer to ports in the backend address pool
  - Two probes which contain HTTP and HTTPS health probes used to check availability
    of virtual machines in the backend address pool
  - Two inbound NAT rules which contain rules that map a public port on the load
    balancer to a port for a specific virtual machine in the backend address pool
  - this provides direct VM connectivity for SSH to port 22 and TELNET to port 23
 
  Create two network interfaces in the frontend subnet ...
  - And associate network interfaces to backend pools and NAT rules
 
  Create two virtual machines in the frontend subnet ...
  - And assign network interfaces
 
  Update an existing load balancer, configure TCP idle timeout
  Create another load balancer
  Remove an existing load balancer
 

## Running this Sample ##

To run this sample:

Set the environment variable `AZURE_AUTH_LOCATION` with the full path for an auth file. See [how to create an auth file](https://github.com/Azure/azure-sdk-for-java/blob/master/AUTH.md).

    git clone https://github.com/Azure-Samples/network-java-manage-internet-facing-load-balancers.git

    cd network-java-manage-internet-facing-load-balancers

    mvn clean compile exec:java

## More information ##

[http://azure.com/java](http://azure.com/java)

If you don't have a Microsoft Azure subscription you can get a FREE trial account [here](http://go.microsoft.com/fwlink/?LinkId=330212)

---

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.