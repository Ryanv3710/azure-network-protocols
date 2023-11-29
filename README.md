<p align="center">
<img src="https://i.imgur.com/EaYjLa3.png" alt="process of DNS"/>
</p>

<h1Accessing DNS through A-name --> CNAME -- > DNS cache exercises</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Windows Powershell ISE (admin)
- command line
  


<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Windows (Windows Server 2022 Datacenter Azure Edition)


<h2>Requirements</h2>

- Have completed active directory lab
- Connect to DC-1 & Client-1 as domain.com\jane_admin 


<h2>A-Record exercise</h2>

<p>
<img src="https://i.imgur.com/i1qFUwz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Were going to attempt to ping 'mainframe' but it doesnt exist so the ping request will fail. These are the sequential steps a computer takes to find what it is your requesting

  <ul>
    <li>1. Check local cache </li>
    <li>2. Check host file</li>
    <li>3. Check DNS</li>
  </ul>
  all three steps were atttempted and could not located 'mainframe' 
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
