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
