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

Created a Windows 10 'honeypot' Virtual Machine within the Azure portal.
![Screenshot 2023-08-20 (1)](https://github.com/Lantyy/Azure-Sentinel-lab/assets/122828853/c5603f8a-306d-45f7-ad36-65c2616e7654)


Created a Log Analytics Workspace within the Azure portal.
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


Created a 'custom log' within Log Analytics Workspace to bring in the custom logs.
![Screenshot 2023-08-20 (9)](https://github.com/Lantyy/Azure-Sentinel-lab/assets/122828853/ccf2681f-6c42-4b81-b7b2-f331a1a80a7c)


Implemented custom fields/extract fields from the raw custom log data.
![Screenshot 2023-08-20 (10)](https://github.com/Lantyy/Azure-Sentinel-lab/assets/122828853/a6262f74-cc9d-488b-8550-bb5bcd2a1702)


Created a "workspace" in Sentinel and filtered the dashboard to plot the failed Remote Desktop login attempts on map by Latitude and Longitude.
![Screenshot 2023-08-20 (11)](https://github.com/Lantyy/Azure-Sentinel-lab/assets/122828853/3fbc5a93-9421-405c-a41a-703390ad11d6)


**Final Map Check**
TBD


# Lab Final Thoughts & Takeaways
In creating and deploying this lab I learned that the internet is a very volatile place. Bots/hackers will stop at nothing to access host computer's data. Even to the extent to Brute Force attack a computer that they may never gain access to. Keeping a strong password, restricting RDP access and keeping a Firewall up to date is paramount to keeping a network secure as aging firewalls present a security risk for an environment. Also, SIEMs (Microsoft Sentinel in this case) can be a very useful tool to display raw data to a readable and presentable format. This can be a great tool to gain more incite for everyday Security Analyst threat detection efforts.

Credit: This lab was created by Josh Madakor, I followed the steps used in his YouTube video to create and replicate this lab. 

~ Lab YouTube Link - https://www.youtube.com/watch?v=RoZeVbbZ0o0

~ GitHub Script used - https://github.com/joshmadakor1/Sentinel-Lab/blob/main/Custom_Security_Log_Exporter.ps1
  
