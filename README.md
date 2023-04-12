<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>Deployment and Configuration Steps</h2>

<p>
1. Login to Microsoft Azure.
</p>

<p>
2. We need to create our <ins>Resource Groups</ins> and our <ins>Virtual Machines</ins>. We need to create 2 VMs, one for Domain Controller and one for the Client. Follow these steps.
</p>

<p>
<img src="https://i.imgur.com/a22W79v.png" height="80%" width="80%" />
</p>

<p>
<img src="https://i.imgur.com/3VBzNP8.png" height="80%" width="80%">
</p>

<p>
<img src="https://i.imgur.com/H3mWQTV.png" height="80%" width="80%">
</p>

<p>
<img src="https://i.imgur.com/aCHISDF.png" height="80%" width="80%">
</p>

<p>
<img src="https://i.imgur.com/BNS0O4r.png" height="80%" width="80%">
</p>

<p>
<img src="https://i.imgur.com/JtMWEv6.png" height="80%" width="80%">
</p>

<p>
<img src="https://i.imgur.com/94mdwrq.png" height="80%" width="80%">
</p>

<p>
<img src="https://i.imgur.com/nx9Q0tJ.png" height="80%" width="80%">
</p>

<p>
<img src="https://i.imgur.com/Np6rNXq.png" height="80%" width="80%">
</p>

<p>
<img src="https://i.imgur.com/wFfGn8n.png" height="80%" width="80%">
</p>

- Wait for the VM to get deployed. After receiving a notification saying it is deployed, follow these steps.

<p>
<img src="https://i.imgur.com/9mEfCQC.png" height="80%" width="80%">
</p>

<p>
<img src="https://i.imgur.com/aRk3SRF.png" height="80%" width="80%">
</p>

<p>
<img src="https://i.imgur.com/hDPKhtr.png" height="80%" width="80%">
</p>

<p>
<img src="https://i.imgur.com/WplKSxb.png" height="80%" width="80%">
</p>

<p>
<img src="https://i.imgur.com/wO5VHW8.png" height="80%" width="80%">
</p>

<p>
<img src="https://i.imgur.com/bo5c20M.png" height="80%" width="80%">
</p>

<p>
<img src="https://i.imgur.com/SUU3xsY.png" height="80%" width="80%">
</p>

- Now we need to set the IP Address to static, we are changing it to static so that the IP Address remains the same and it will not change.

<p>
<img src="https://i.imgur.com/I0T8Ydu.png" height="80%" width="80%">
</p>

<p>
3. Let's create our 2nd VM. Follow these steps.
</p>

<p>
<img src="https://i.imgur.com/QfWCQBJ.png" height="80%" width="80%">
</p>

<p>
<img src="https://i.imgur.com/C1nn6IX.png" height="80%" width="80%">
</p>

<p>
<img src="https://i.imgur.com/I8VpS6k.png" height="80%" width="80%">
</p>

<p>
<img src="https://i.imgur.com/YbffiFV.png" height="80%" width="80%">
</p>

<p>
<img src="https://i.imgur.com/ZtSCVFd.png" height="80%" width="80%">
</p>

- Scroll to the top page and click <ins>Networking</ins>.

<p>
<img src="https://i.imgur.com/4p4ek3c.png" height="80%" width="80%">
</p>

<p>
<img src="https://i.imgur.com/EIZrZ9k.png" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
<p>
<img src="" height="80%" width="80%">
</p>
