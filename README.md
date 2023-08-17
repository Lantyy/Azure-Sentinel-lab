# Azure-Sentinel-lab

# This Project
This is a instructional step by step process to building a functional **Azure Sentinel lab** for defensive security acting as a honey pot.

My purpose for this lab is to learn more about Security Monitoring and Detection Engineering.

# Virtual Machines
This lab consists of:

  ~ **Kali:** This is the offensive machine that will be used to propagate different forms of attacks.
	
  ~ **pfsense:** This will be the firewall for controlling inbound and outbound traffic, only accessible and visible in the VM private network.
	
  ~ **Splunk:** This is an additional SIEM that will be used in addition and comparison to Kibana on Security Onion.
	
  ~ **Windows DC:** This is a windows domain controller that will have two windows machines connected to it.
	
  ~ **Windows 7 & Windows *XP*:** These windows machine will vary based on individual needs.
	
  ~ **Ubuntu/Centos/Metasploitable/DVWA/Vulnhub machines:** All these are potential linux machines that can be added to the network for exploitation, detection, or monitoring purposes.


# Network Design
![Azure lab topology](https://github.com/Lantyy/Azure-Sentinel-lab/assets/122828853/39cb1d35-4c1d-4c2e-8e7f-a6f595aa9886)
