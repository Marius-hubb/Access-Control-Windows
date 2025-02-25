<h1>Implementing Access Controls in Windows Machine </h1>

 ## [Video Demonstration (5:27)](https://drive.google.com/file/d/1_NYhGg34o7ZQ53rsRDEikki-nwYnda92/view?usp=sharing)

<h2>Description</h2>

This lab demonstrates the implementation of access control policies in Windows machine.<br />

<h2>Lab walk-through:</h2>

<p align="center">Before implementing access control policies, we will first examine the properties of the current Administrator account. <br/> Start-->right-click Windows PowerShell-->More--> Run as administrator.
<br/>
<p align="center"><img src="https://i.imgur.com/jHP3Z02.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<p align="center">Typing whoami /user to display the details regarding Security ID (SID) and other additional information of the current user.
<br/>
<img src="https://i.imgur.com/YkgTU8p.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<p align="center"> Displaying detailed user account information using: get-aduser -identity administrator -properties *
<br/>
<img src="https://i.imgur.com/afCAera.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
 <p align="center">Start-->Server Manager  
<br/>
<img src="https://i.imgur.com/7tnHM8w.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
 <p align="center">Tools-->Active Directory Users and Computers
<br/>
<img src="https://i.imgur.com/XFQbd4H.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
