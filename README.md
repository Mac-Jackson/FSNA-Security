<p align="center">
<img src="https://github.com/user-attachments/assets/1c681a56-318d-4614-a8c0-ef2a32be3425" alt="Security Logo"/>
</p>

<h1>Configure SSH & Disable Telnet</h1>
This Lab tutorial outlines the implementation of Secure Remote Management, Secure Shell, and the Disablement of Telnet.<br />


<h2>Networking Technologies Used</h2>

- SSH (Secure Shell) Version 2
- RSA Cryptographic Keys
- VTY Lines
- Domain Name System (DNS)


<h2>Environments Used </h2>

- Command-Line Interface (CLI)
- Cisco IOS Router or Switch


<h2>Tools Used </h2>

- Cisco Packet Tracer

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1  Configure SSH on a Cisco IOS Router or Switch
- Step 2  Add a Domain Name to the device (FSNA.Local)
- Step 3  Generate the RSA Crypto Keys - 1024 bit minimum, 2048 recommended
- Step 4  Enable SSH Version 2
<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://github.com/user-attachments/assets/8b054e88-c23a-4a79-ad2c-d4ebc72947b4" height="80%" width="80%" alt="FSNA-Security"/>
</p>
<p>
 Configure SSH And Disable Telnet
 (config)#ip domain-name fsna.local
 (config)#crypto key generate rsa (Modulus: 2048)
 (config)#ip ssh version 2
 (config)#line vty 0 15
 (config-line)#transport input ssh
 (config-line)#transport output ssh
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/28fb114e-8191-4f99-b32c-8e49a117e9fd" height="80%" width="80%" alt="FSNA-Security"/>
</p>
<p>
Enable SSH version 2
</p>
<br />


<p>
<img src="https://github.com/user-attachments/assets/70c39df2-3ab6-48fe-87c7-4677a796bf48" height="80%" width="80%" alt="FSNA-Security"/>
</p>
<p>
Lock Down for no Telnet Access.
</p>
<br />


