# Active-Directory

<h2>Description</h2>
In this lab, I created a sample Active Directory and connected it to a client virtual machine.  I configured it to allow network access and assign IP addresses to users connected to the domain.  I also used a script to provision a large amount of user accounts from a text file.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Active Directory</b> 
- <b>PowerShell</b>
- <b>Windows Server</b>
- <Oracle VirtualBox</b>

<h2>Environments Used </h2>

- <b>Windows 10</b>

<h2>Program walk-through:</h2>

<p align="center">
1. This is the server after configuring all of the settings. <br/>
<img src="https://i.imgur.com/xKtmbGi.png" height="80%" width="80%" alt="Active Directory Steps"/>
<br />
<br />
2. I created a domain called mydomain.com to communicate to.  I also set myself as an administrator.  <br/>
<img src="https://i.imgur.com/1DBdZfw.png" height="80%" width="80%" alt="Active Directory Steps"/>
<br />
<br />
3. I configured the Remote Access settings using NAT to allow the client virtual machine to communicate with the Domain Controller for Internet access.  The up arrow next to DOMAINCONTROLLER shows that it has been configured.  <br/>
<img src="https://i.imgur.com/lg6Iz4y.png" height="80%" width="80%" alt="Active Directory Steps"/>
<br />
<br />
4. Next, I set up a DHCP server in order to grant clients an IP address to allow Internet access.  I set the scope to 100-200, so any IP addresses between 172.16.0.100 and 172.16.0.200 can be used.  <br/>
<img src="https://i.imgur.com/9yORpf7.png" height="80%" width="80%" alt="Active Directory Steps"/>
<br />
<br />
5. After that, I ran a PowerShell script to create a large number of user accounts from a text file containing first and last names.  <br/>
<img src="https://i.imgur.com/t9bpnXC.png" height="80%" width="80%" alt="Active Directory Steps"/>
<br />
<br />
6. With everything configured properly in Server Manager, I ran a second virtual machine to function as a client.  As you can see, it is connected to mydomain.com and is given an IP address.  I pinged google.com to show that the client has access to the Internet.  <br/>
<img src="https://i.imgur.com/Eq0g2br.png" height="80%" width="80%" alt="Active Directory Steps"/>
<br />
<br />
7. By checking DHCP, you can see that a lease has been created upon the client joining the server.  <br/>
<img src="https://i.imgur.com/spdXmy8.png" height="80%" width="80%" alt="Active Directory Steps"/>
<br />
<br />
8. In Active Directory Users and Computers, it now shows that the computer that the virtual machine is on is a part of the domain.  <br/>
<img src="https://i.imgur.com/QkOfDfb.png" height="80%" width="80%" alt="Active Directory Steps"/>
</p>
