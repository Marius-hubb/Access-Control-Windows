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
 <p align="center">Creating a New Organizational Unit inside Server Manager
  <br/> Start-->Server Manager  
<br/>
<img src="https://i.imgur.com/7tnHM8w.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
 <p align="center">Tools-->Active Directory Users and Computers
<br/>
<img src="https://i.imgur.com/XFQbd4H.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
 <p align="center">Creating a New Organizational Unit
<br/>
<img src="https://i.imgur.com/kmbUOzx.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
 <p align="center">Setting NetworkAdmin as a new organizational unit
<br/>
<img src="https://i.imgur.com/WUyVxmZ.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
 <p align="center">Creating a new user IT Head inside the new organizational unit NetworkAdmin
<br/>
<img src="https://i.imgur.com/fvtwwDN.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />  
 <p align="center">Specifying the name IT Head and a password
<br/>
<img src="https://i.imgur.com/WHIfgmO.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/j8lnuAL.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
 <p align="center">Creating a new group TechSupport within the NetworkAdmin Organizational Unit.
  <br /> Right-click NetworkAdmin Organizational Unit-->New--> Group.
<br/>
<img src="https://i.imgur.com/w7K0IOm.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br /> 
 <p align="center">Naming TechSupport as the new group within the NetworkAdmin Organizational Unit.
<br/>
<img src="https://i.imgur.com/GkfKC27.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br /> 
<p align="center">Adding the User IT Head to the TechSupport group.
<br/>
<img src="https://i.imgur.com/whE7vAD.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/FFFyDzw.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/Njs6l5a.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br /> 
 <p align="center">Creating a new Computer01 inside the FinanceOU Organizational Unit.
  <br/> Right-click FinanceOU Organizational Unit-->New-->Computer
<br/>
<img src="https://i.imgur.com/iCjMLVb.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br /> 
 <p align="center">Creating a detailed report of all computer objects in the domain:<br/>
  get-adcomputer -filter * | out-file C:\useraccounts.txt 
<br/>
<img src="https://i.imgur.com/QELOpZW.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br /> 
 <p align="center">By opening useraccounts.txt We can view the newly created Computer01  
<br/>
<img src="https://i.imgur.com/TUbMWxW.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
 <p align="center">We will modify the existing GPO to set password requirements.
<br />Windows Administrative Tools-->Group Policy Management.
<br/>
<img src="https://i.imgur.com/nj72gQd.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
 <p align="center">Click to edit the Default Domain Policy
<br/>
<img src="https://i.imgur.com/5Yhu6li.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
<p align="center">Setting the Password Policy
<br/>
<img src="https://i.imgur.com/Blv572f.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
<p align="center">Generating a report of password policy settings:
 <br/>gpresult /H C:\passwords-policy-settings.html
<br/>
<img src="https://i.imgur.com/1SMZSdt.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
 <p align="center">Once we open the html file we can view the detailed report on the implemented account policies.
<br/>
<img src="https://i.imgur.com/UDUeNrD.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
