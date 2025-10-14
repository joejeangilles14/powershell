<p align="center">
<img src="https://github.com/user-attachments/assets/994e5afb-bec5-4370-8cdd-aa1da7c30dcb" />
</p>

<h1>Creating Users with Powershell</h1>
This tutorial explores deploying an Active Directory environment, from creation and management to deactivation and removal.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Powershell

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)
- Windows Server 2022

<h2>High-Level Deployment and Configuration Steps</h2>

- Setup Remote Desktop for non-administrative users on Client-1 
- Create users and attempt to log into client-1 with one of the users

<h2>Configuration Steps</h2>

<p>
<img src="https://github.com/user-attachments/assets/864f4d7f-442f-4831-a295-141254b6d33f" />
</p>
<p>
To launch Client-1 and DC-1 virtual machines, go to Azure's virtual machines section and choose both, select Yes then connect to both VMs.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/dd78dd1a-8b33-4adf-a183-dd110145df49" />
</p>
<p>
Right-click the Start menu in the client-1 virtual machine and choose System.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/78a61ec5-e67a-4276-9c15-caf04aca41ac" />
</p>
<p>
Scroll down and select Remote Desktop.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/e8ce86b6-2692-487d-b139-9396ef37f313" />
</p>
<p>
Under User Accounts, click on "Select Users that can remotely access this PC".
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/040b99e8-88ed-45dc-9ad7-138cea325ed6" />
</p>
<p>
Select Add.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/c11cffbe-bd27-40f5-ba1e-f5e40258ba34" />
</p>
<p>
To pick the object names, enter Domain Users. Then, click Check Names and click OK.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/9b146ab0-0e29-4497-90fa-c4026353cb50" />
</p>
<p>
Click OK.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/5e8d0379-e177-4f5e-a3ac-ad38864570e1" />
</p>
<p>
Switch to DC-1, look for Windows Powershell ISE in DC-1, then right-click and select "Run as administrator."
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/cba97577-f78e-4c3a-be0b-080c34db5404" />
</p>
<p>
Select Yes.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/5ea57d76-8406-4fb9-8605-e50a6c68880d" />
</p>
<p>
In Windows Powershell ISE, click on the arrow drop down next to Script.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/5ea57d76-8406-4fb9-8605-e50a6c68880d" />
</p>
<p>
Ten thousand random users with the password of Password1 will be created by the script I used.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/1a42663a-58a2-4958-b22a-13c20c0e1103" />
</p>
<p>
Click Run Script.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/bf5391b6-dc25-4c39-ad20-eea61b5e6f9b" />
</p>
<p>
The script ran successfully.
</p>
<br />

<p>
<img width="1720" height="1402" alt="image" src="https://github.com/user-attachments/assets/03c1ea5a-0621-4da0-9503-01b569b78a1f" />
</p>
<p>
Search for "Active Directory Users and Computers".
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/3deb8639-54ab-4183-8600-77423beb696a" />
</p>
<p>
The new users were retrieved.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/959cdb1d-4ff4-45dc-b123-15ba5cd7ff32" />
</p>
<p>
Right-click on the _EMPLOYEES organizational unit and select Refresh.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/ea0d3070-803c-433b-af2f-93f6205058d7" />
</p>
<p>
Click on the Start menu and sign out.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/757e5d57-886f-4f4d-ad26-36303bedbada" />
</p>
<p>
Back in Microsoft Remote Desktop, type in mydomain.com\[insert random client name] and connect (I used bas.fufu). Password1 is the pasword for any of the users.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/eb31b053-ba6f-403e-aabb-87139ae9882a" />
</p>
<p>
Once I have successfully logged in as bas.fufu, I opened command prompt to verify.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/59064f5c-d49f-4793-8f4d-30153b04593c" />
<img src="https://github.com/user-attachments/assets/fdeea379-5b7c-4407-a759-05ad5bfefd45" />
</p>
<p>
Open File Explorer, click on This PC, click on the C-drive and go to the Users folder.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/02fbebec-8876-4bd5-89d7-3443ab7e4747" />
</p>
<p>
Because bas.fufu isn't an admin, he cannot access the labuser folder.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/61cdaf6f-4875-48f1-a1f1-0b885b15a8b2" />
</p>
<p>
To conclude this lab, go to the Virtual Machines section in Azure and select both VMs and stop them by selecting the three dots on the top right. Then click Yes.
</p>
<br />
