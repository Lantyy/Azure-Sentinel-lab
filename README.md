# Azure-Sentinel-lab

![Title](https://github.com/Lantyy/Azure-Sentinel-lab/assets/122828853/5af6a030-c3ce-4fa8-ab6f-7d7c1c3b1cfe)

# This Project
This is a instructional step by step process to building a functional **Azure Sentinel lab** for defensive security acting as a honey pot.

My purpose for this lab is to learn more about Security Monitoring and Detection Engineering.

# Virtual Machines / Tools
This lab consists of virtual machines created within the Azure Cloud:

  ~ **Windows 10** ~ This Windows machine will be made vulnerable acting as a honey pot.

  ~ **Log Analytics Workspace** ~ This will be the log repository used to ingest logs from the Windows VM, then sent to the SIEM (Sentinel).
	
  ~ **Azure Sentinel** ~ This is a SIEM used to display & map the attacker data on a geographic world map.
	
# Network Design
![Azure lab topology](https://github.com/Lantyy/Azure-Sentinel-lab/assets/122828853/39cb1d35-4c1d-4c2e-8e7f-a6f595aa9886)

# Lab Creation Steps


Created a Windows 10 'honeypot' Virtual Machine within Portal.Azure 
![Screenshot 2023-08-20 (1)](https://github.com/Lantyy/Azure-Sentinel-lab/assets/122828853/c5603f8a-306d-45f7-ad36-65c2616e7654)


Created a Log Analytics Workspace within Portal.Azure
![Screenshot 2023-08-20 (2)](https://github.com/Lantyy/Azure-Sentinel-lab/assets/122828853/c6c42d27-d51d-4f62-9451-402b44b65dff)


Connected the Log Analytics Workspace to the Windows 10 Virtual Machine.
![Screenshot 2023-08-20 (3)](https://github.com/Lantyy/Azure-Sentinel-lab/assets/122828853/b2ac725c-dec1-47bd-87ef-3004fde74d17)


Connected Azure Sentinel to the Windows 10 Virtual Machine.
![Screenshot 2023-08-20 (4)](https://github.com/Lantyy/Azure-Sentinel-lab/assets/122828853/7d50a23b-3bc9-4601-9e5c-76094c965435)


Logged into the Windows 10 Virtual Machine using RDP.
![Screenshot 2023-08-20 (5)](https://github.com/Lantyy/Azure-Sentinel-lab/assets/122828853/a7ee8d70-02ad-4270-b109-2150e2d4e16d)


Disabled the Firewall on the Windows 10 Virtual Machine 'honeypot'
![Screenshot 2023-08-20 (6)](https://github.com/Lantyy/Azure-Sentinel-lab/assets/122828853/86d67ace-bda9-4eef-8782-4653be4e1353)


Implemented a custom PowerShell script from Github to look up the attackers geolocation information using an API.
![Screenshot 2023-08-20 (7)](https://github.com/Lantyy/Azure-Sentinel-lab/assets/122828853/a2bf4be8-e55c-4b39-9060-bba8185a9cdf)
![Screenshot 2023-08-20 (8)](https://github.com/Lantyy/Azure-Sentinel-lab/assets/122828853/9f4fb38b-07bc-4e24-9796-befc012b1d08)




  ~ 
  ~  
  # Lab Conclusion

Credit: This lab was created by Josh Madakor, I followed the steps used in his YouTube video to create and replicate this lab. 
Link - https://www.youtube.com/watch?v=RoZeVbbZ0o0
Github Script used - https://github.com/joshmadakor1/Sentinel-Lab/blob/main/Custom_Security_Log_Exporter.ps1
  
