
<img src="https://i.imgur.com/EaYjLa3.png" alt="process of DNS"/>
</p>

<h1>Accessing DNS through A-name --> CNAME -- > DNS cache exercises</h1>
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
<img src="https://i.imgur.com/RCOyWMU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open server managaer and by clicking 'tools' tab you'll scrow down to and click DNS
</p>
<br />

<p>
<img src="https://i.imgur.com/YD7epMl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
We'll be taking a look in the Forward Lookup Zones in mydomain.com and see the A records already created
</p>
<br />


<p>
<img src="https://i.imgur.com/5doUgiW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Manually create a A-Name record for 'mainframe' so it can be located and be able to be pinged
</p>
<br />


<p>
<img src="https://i.imgur.com/17lxx1n.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
As far as the IP address goes; you can set it to whatever but I went ahead and set it to the IP address of DC-1
</p>
<br />


<p>
<img src="https://i.imgur.com/hNAMB1v.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
You can now ping 'mainframe' and returned the A-Record we created which is mainframe.mydomain.com
</p>
<br />

<p>
<img src="https://i.imgur.com/otaf3GS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go back to DC-1 and change the IP address to 8.8.8.8, notice it still pings the previous address. That is due to it still being in the local cache.
</p>
<br />

<p>
<img src="https://i.imgur.com/VUtCpt7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

  By flushing the DNS it will now ping the latest IP 
</p>
<br />
