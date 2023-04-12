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

- Now let's wait for the deployment to finish.

<p>
<img src="https://i.imgur.com/s02pbGe.png" height="80%" width="80%">
</p>

- Once it says completed, follow these steps to check the network topology and make sure that the 2 VMs is in the same Virtual Network.

<p>
<img src="https://i.imgur.com/dtFyZGO.png" height="80%" width="80%">
</p>

<p>
<img src="https://i.imgur.com/uKQvyZQ.png" height="80%" width="80%">
</p>

<p>
<img src="https://i.imgur.com/zUiwzpD.png" height="80%" width="80%">
</p>

- Now let's connect to our VM. If you're using macOS, download Microsoft Remote Desktop in the app store, if you are in Windows, use Remote Desktop.

<p>
<img src="https://i.imgur.com/k9wlVaL.png" height="80%" width="80%">
</p>

- Let's connect to Client-1. Follow these steps.

<p>
<img src="https://i.imgur.com/lDTMo9Q.png" height="80%" width="80%">
</p>

<p>
<img src="https://i.imgur.com/0HnJymp.png" height="80%" width="80%">
</p>

<p>
<img src="https://i.imgur.com/CvGtyQs.png" height="80%" width="80%">
</p>

<p>
<img src="https://i.imgur.com/tsv6oT5.png" height="80%" width="80%">
</p>

<p>
<img src="https://i.imgur.com/GhEP1Pc.png" height="80%" width="80%">
</p>

<p>
<img src="https://i.imgur.com/So1oViW.png" height="80%" width="80%">
</p>

- Let's wait for the VM to login.

<p>
<img src="https://i.imgur.com/QjTKNaf.png" height="80%" width="80%">
</p>

- Select <ins>No</ins> to everything.

<p>
<img src="https://i.imgur.com/X9aB03b.png" height="80%" width="80%">
</p>

- Go to Azure portal and copy the Private IP Address of DC-1.

<p>
<img src="https://i.imgur.com/70bJ3b3.png" height="80%" width="80%">
</p>

- Open <ins>Command Prompt</ins> and we will ping DC-1. It should say <ins>request time out</ins>. We will configure DC-1 and allow ICMP traffic.

<p>
<img src="https://i.imgur.com/D8dri9w.png" height="80%" width="80%">
</p>

- Connect to DC-1 using the public IP Address.

<p>
<img src="https://i.imgur.com/Yz69AEJ.png" height="80%" width="80%">
</p>

- Add a new PC to Microsoft Remote Desktop and connect to DC-1.

<p>
<img src="https://i.imgur.com/0EtZVxN.png" height="80%" width="80%">
</p>

<p>
<img src="https://i.imgur.com/R04PPsr.png" height="80%" width="80%">
</p>

- Enter the username and password you created for DC-1 VM.

<p>
<img src="https://i.imgur.com/S9YVAJN.png" height="80%" width="80%">
</p>

- Click <ins>Continue</ins>

<p>
<img src="https://i.imgur.com/9V47Zwc.png" height="80%" width="80%">
</p>

- We should be seeing this screen after we login to DC-1.

<p>
<img src="https://i.imgur.com/RcKkGCq.png" height="80%" width="80%">
</p>

- To allow ICMP traffic, click <ins>Start</ins> and type <ins>wf.msc</ins>.

<p>
<img src="https://i.imgur.com/EwxtJQW.png" height="80%" width="80%">
</p>

- Open it and enable this 2 items by right clicking on the item and choosing <ins>Enable Rule</ins>.

<p>
<img src="https://i.imgur.com/w5o7oQx.png" height="80%" width="80%">
</p>

- Once we enabled those 2 items, it should look like this.

<p>
<img src="https://i.imgur.com/P0pk0WP.png" height="80%" width="80%">
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
