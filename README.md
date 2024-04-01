<h1>Azure Sentinel MAP with LIVE CYBER ATTACKS </h1>

<h2>Description</h2>
I utilized Azure Sentinel by connecting it to a virtual machine serving as a honeypot. During this process, I monitored live RDP Brute Force attacks from various global locations. To trace the origins of these attacks, I employed a custom PowerShell script to retrieve the attackers' geolocation data and then displayed it on the Azure Sentinel Map.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Azure Sentinel</b> 
- <b>Powershell</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

<h2>Program walk-through:</h2>

<p align="center">
Create a honeypot virtual machine in Azure with all open ports: <br/>
<img src="https://i.imgur.com/ipfmU03.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create a log analytics workspace:  <br/>
<img src="https://i.imgur.com/Ibg79C8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Store all window security event data: <br/>
<img src="https://i.imgur.com/Ibg79C8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Connect honeypot to log analytics workspace:  <br/>
<img src="https://i.imgur.com/IsdoPg5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Grab event for incorrect login attempt:  <br/>
<img src="https://i.imgur.com/bskz0jE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Allow ICMP Requests:  <br/>
<img src="https://i.imgur.com/HZQyr7y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Ran powershell script that auto logs geolocation via API:  <br/>
<img src="https://i.imgur.com/ES5nCMq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Ensured logging was working in the script:  <br/>
<img src="https://i.ibb.co/zSHzYth/image.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Created a custom log in sentinel:  <br/>
<img src="https://i.ibb.co/W28x3d7/image.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Connect Azure to logging information and correctly extract the info:  <br/>
<img src="https://i.ibb.co/vj4ts8b/im33333age.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
 <img src="https://i.ibb.co/6XTPNhv/ima22222ge.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Watch as the attacks come in:  <br/>
<img src="https://i.imgur.com/ipfmU03.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>

