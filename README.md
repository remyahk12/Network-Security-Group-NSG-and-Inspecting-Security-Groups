<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>Step 1 :Creating the Resource Group in Azure VM</h2>
<img src ="https://github.com/user-attachments/assets/de722a43-3029-4c2e-9a9c-e85912e29525"height="80%" width="80%" />

<h2>Step 2 : Creating Windows VM in the resource group created with a new virtual network and subnet</h2>
<img src ="https://github.com/user-attachments/assets/746cf11c-ceb0-427f-825c-f16de6f9e046" height ="80%" width ="80%" />

<h2>Step 3 : Create a Linux (Ubuntu) VM
While creating the VM, select the previously created Resource Group and Virtual Network—the Virtual Network MUST BE THE SAME.
</h2>
<img src ="https://github.com/user-attachments/assets/3bc033ae-6ed8-414f-96ef-292a5df4e85a" height ="80%" width ="80%" />

<h1>Observing ICMP Traffic</h1>
<h2>Step 1:Use Remote Desktop to connect to your Windows 10 Virtual Machine .Within the Windows 10 Virtual Machine, Install Wireshark
Open Wireshark and start packet capture

<h2>Actions and Observations</h2>
</h2>
<img src="https://github.com/user-attachments/assets/0900afce-8ddc-453e-a4ed-3e85ddb77779" height ="80%" width ="80%" />
<h2>Within Wireshark, filter for ICMP traffic only
Retrieve the private IP address of the Ubuntu VM (linux-vm) and attempt to ping it from within the Windows 10 VM
Observe ping requests and replies within WireShark
</h2>
<img src ="https://github.com/user-attachments/assets/fb0538e7-34a1-467d-a2ee-16d1fc096a94"  height ="80%" width ="80%" />
<h2><b>Configuring a Firewall [Network Security Group]</b></h2>
<h3>Step 1:Initiate a perpetual/non-stop ping from your Windows 10 VM to your Ubuntu VM
</h3>
<img src="https://github.com/user-attachments/assets/60694a14-f70f-4fe5-8219-401ca449522b"
 height ="80%" width ="80%" />
 <h3>Step 2:Open the Network Security Group your Ubuntu VM is using and disable incoming (inbound) ICMP traffic
</h3>
<img src="https://github.com/user-attachments/assets/c4e15dcf-a4ca-4e70-ac41-a2498b5380e4"

 height ="80%" width ="80%" />
 <h3>Step 3:Back in the Windows 10 VM, observe the ICMP traffic in WireShark and the command line Ping activity
</h3>
<img src="https://github.com/user-attachments/assets/bd8dc660-584d-42d5-b269-63c85b5ddd37"
height ="80%" width ="80%" />
<h3>Step 4:Re-enable ICMP traffic for the Network Security Group your Ubuntu VM is
</h3>
<img src="https://github.com/user-attachments/assets/f1915771-cb28-4742-827f-bfbd183a6d72"

height ="80%" width ="80%" />
<h3>Step 5:Back in the Windows 10 VM, observe the ICMP traffic in WireShark and the command line Ping activity 
</h3>
<img src="https://github.com/user-attachments/assets/93c98dbb-7aea-4628-aa5a-1004b71b9771"


height ="80%" width ="80%" />








<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
