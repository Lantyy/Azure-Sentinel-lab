# Azure-Sentinel-lab
# About Me
Hi! I'm Miles. 

# This Project
This is a instructional step by step process to building a functional **Azure Sentinel lab** for defensive security acting as a honey pot.

My purpose for this lab is to learn more about Security Monitoring and Detection Engineering.

# Virtual Machines
This lab consists of:

  ~ **Kali:** This is the offensive machine that will be used to propagate different forms of attacks.
	
  ~ **pfsense:** This will be the firewall for controlling inbound and outbound traffic, only accessible and visible in the VM private network.
	
  ~ **Security Onion:** This will be the all-in-one IDS, Security Monitoring and Log Management solution.
	
  ~ **Splunk:** This is an additional SIEM that will be used in addition and comparison to Kibana on Security Onion.
	
  ~ **Windows DC:** This is a windows domain controller that will have two windows machines connected to it.
	
  ~ **Windows 7 & Windows *XP*:** These windows machine will vary based on individual needs.
	
  ~ **Ubuntu/Centos/Metasploitable/DVWA/Vulnhub machines:** All these are potential linux machines that can be added to the network for exploitation, detection, or monitoring purposes.


# Network Design
[![Topology]](https://github.com/Lantyy/Azure-Sentinel-lab/blob/52e7f69bb609269f35fac12f7980db602ad726b1/Azure%20lab%20topology.jpg)https://github.com/Lantyy/Azure-Sentinel-lab/blob/52e7f69bb609269f35fac12f7980db602ad726b1/Azure%20lab%20topology.jpg
