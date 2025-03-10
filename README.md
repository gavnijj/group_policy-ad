<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Group Policy and Managing Accounts</h1>
This tutorial outlines how to deal with account lockouts, the enabling and disabling of accounts, and observing logs.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Dealing with Account Lockouts
- Enabling and Disabling Accounts
- Observing Logs
- Step 4

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/LHFFkwf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The domain controller needs a Account Lockout Policy that controls when an account is locked after multiple failed login attempts, how long the account remains locked, and how the lockout counter is reset. To do this: 1. open the the Group Management Console(GPMC) in the Domain Controller 2. Create or edit a Group Policy Object 3. Navigate to Account Lockout Policies 5. Configure Policies 6. Link GPO to an Organizational Unit 7. Update Group Policy. The above picture defines the Account Lockout Policy as 5 invalid attempts before the Account is locked for 30 minutes an the invalid attempts counter resets after 10 minutes. 
</p>
<br />

<p>
<img src="https://i.imgur.com/3eeudp0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the Active Directory Users and Computer window you can disable , reset password, or add to a group an account that is connected to the Domain Controller. 
</p>
<br />

<p>
<img src="https://i.imgur.com/uO8FN4Y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Can observe the logs in the Domain Controller by opening the eventvwr.msc window. The security logs show the type of event IDs that have been goin on in the Domain Controller. If you see suspicious activity or many log in attempts from an account, you can disable the account to prevent access into the Domain Controller.
</p>
<br />
