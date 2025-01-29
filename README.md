<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Using Group Policy to change Client wallpapers </h1>
In this project, I utilize Group policy as well as file shares to alter user backgrounds remotely. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Microsoft Powershell
- Group Policy Managment Services
  

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Windows Server 2022 Datacenter


<h2>Actions and Observations</h2>

<p>
<img width="1680" alt="Screenshot 2025-01-29 at 3 30 01 PM" src="https://github.com/user-attachments/assets/4a87ef45-227b-4114-8212-c5b76db65d62" />
</p>
<p>
For this project, I chose this picture of a big smiley face to put on all my fake clients wallpapers. I will be using a domain controller and a client computer from previous labs.
</p>
<br />

<p>
<img width="776" alt="Screenshot 2025-01-29 at 3 20 54 PM" src="https://github.com/user-attachments/assets/cf7f461e-c692-4289-a69a-0a648f730cfd" />
</p>
<p>
From my domain controller, I set up a new folder in the C: drive to make sure all my users can access the picture. I then give it all the permissions it needs and copy the Network Path. 
</p>
<br />

<p>
<img width="1680" alt="Screenshot 2025-01-29 at 3 24 02 PM" src="https://github.com/user-attachments/assets/c2352650-da13-47bf-95b2-afea430b5191" />
</p>
<p>
Next, I set up a new Group Policy object and begin to edit. I go to User Configuration > Administrative Templates > Desktop > Desktop and configure everything else from there. I make sure to also add the title of the image after pasting the network path. 
</p>
<br />

<p>
<img width="475" alt="Screenshot 2025-01-29 at 3 26 20 PM" src="https://github.com/user-attachments/assets/e2f2c7c6-660f-4eda-b9d7-0906d5fff757" />
</p>
<p>
The final step is to force the policy to update using Windows Powershell. I change to one of my fake clients in my domain (bac.vol) to use the gpupdate /force command.
</p>
<br />

<p>
</p>
<p> 
<img width="1680" alt="Screenshot 2025-01-29 at 4 15 00 PM" src="https://github.com/user-attachments/assets/84cf994f-6d9f-4d60-be43-b65f41bbedd7" /> 
</p>
Now, when I log back into bac.vol, I see the big smiley face on the background!
</p>
<br />

