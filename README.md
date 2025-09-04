<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial provides a detailed overview of the post-installation configuration process for the open-source help desk ticketing system, osTicket. In this phase, we will take the system from its initial setup to a fully operational help desk system, ready for handling real-world support tickets..<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Cloud Compute, used to host the osTicket installation)
- Remote Desktop: Secure access to the virtual machine hosting osTicket for configuration and management purposes.
- Internet Information Services (IIS) Web server software that hosts the osTicket web application on Windows.

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

In this step, we will configure important components within osTicket to ensure it functions effectively. These components include:
</br>

- Roles: Assign roles to different agents, such as Admins and Support Staff, to manage access and permissions.
- SLAs (Service Level Agreements): Configure SLAs to ensure timely ticket resolutions based on severity.
- Departments: Create various departments (e.g., IT, Customer Support) to handle tickets based on the type of request.
- Teams: Configure teams that handle specific types of support, such as Level I or Level II support.
- Agents (Workers): Add agents who will manage and resolve tickets.
- Users (Customers): Add the users who will submit tickets to the help desk.
- Help Desk Topics: Define help topics to categorize tickets based on the issues users may encounter.


<h2>Configure Roles</h2>

<p>
<img width="957" height="348" alt="Screenshot 2025-09-03 225105" src="https://github.com/user-attachments/assets/c0ea6584-d957-4608-a7ea-a66e154d924f" />
<img width="959" height="387" alt="Screenshot 2025-09-03 230208" src="https://github.com/user-attachments/assets/569833d6-e22b-478a-9682-cd7369165caf" />

</p>
<p>
  
This area of osTicket contains different levels of access we can create & configure for each individuals and groups/departments.

To Create  
- Navigate to: Admin Panel -> Agents -> Roles
- Create a new "Supreme Admin" role
- Assign full administrative control permission.

</p>
<br />

<h2>Configure SLA</h2>
<h3> Service Level Agreements </h3>
<br />

<p> An SLA defines the agreed service standards between a provider and client. It sets clear expectations, outlines performance targets (e.g., uptime, response time), ensures accountability, builds trust, and provides a basis for conflict resolution if targets aren’t met.</p>
<br />

<p>
<img width="961" height="298" alt="Screenshot 2025-09-03 233143" src="https://github.com/user-attachments/assets/360f3b98-3a1b-4071-bf1d-85fce7706479" />
<img width="960" height="382" alt="Screenshot 2025-09-03 234610" src="https://github.com/user-attachments/assets/88c17632-421b-4f41-841c-48a57236113f" />
<img width="959" height="424" alt="image" src="https://github.com/user-attachments/assets/b9173f07-88ba-4d48-a25a-3441f1e57af6" />

</p>
<p>
  
For this showcase we will create the following SLA's
  
Admin Panel -> Manage -> SLA
- Sev-A (Grace Period: 1 hour, Schedule: 24/7)
- Sev-B (Grace Period: 4 hours, Schedule: 24/7)
- Sev-C (Grace Period: 8 hours, Business Hours)

</p>
<br />



<h2>Configure Departments</h2>
<h3> Here we can configure Ticket Visibility, Help Desk vs SysAdmins, vs Networking
</h3>
<br />

<p>
<img width="958" height="885" alt="image" src="https://github.com/user-attachments/assets/46256fe4-93ac-4a32-8010-958fc92ca9ba" />

</p>
<p>

- Navigate to: Admin Panel -> Agents -> Departments
- Create a department called "System Administrators" to handle high-priority system-level issues.

Here we can also configure department SLA's, Dept manager, add Agents, ticket assignment visibilty, alerts etc
</p>
<br />

<h2>Configure Teams</h2>
<h3> Group people from different departments into one team for a specifc set of task
</h3>
<br />

- Navigate to: Admin Panel -> Agents -> Teams
- Create a Team called "Online Banking" to handle issues from an Online banking host.

</p>
<br />

<h3> Configure Ticket Creation: Allow anyone to create tickets without having an account
</h3>
<br />
<p>
<img width="948" height="684" alt="Screenshot 2025-09-04 002339" src="https://github.com/user-attachments/assets/187ebb49-3855-4c1a-b800-1b5fce5b6d94" />
</p>

<p>
  
- Navigate to: Admin Panel -> Settings -> User Settings
- UNCHECK :Registration Required: Require registration and login to create tickets 

Here we can also manage password policies and login requirements 
</p>
<br />

<h2>Configure Agents (Employees)</h2>
<h3> Here we can add Managers, Adminstrators, IT Helpdesk Agents, HR etc
</h3>
<br />

<p>
<img width="733" height="485" alt="Screenshot 2025-09-04 003103" src="https://github.com/user-attachments/assets/f282036c-bf10-41e2-a567-fd30e66c2e00" />
<img width="816" height="326" alt="Screenshot 2025-09-04 003117" src="https://github.com/user-attachments/assets/5bb5369e-f95d-4b61-bb6f-0f47520dbf9a" />


</p>
<p>

- Admin Panel -> Agents -> Add New
  - Jane (Dept: SysAdmins)
  - John (Dept: Support)
  - Jeff (Dept: Support)
  


Here we can also configure Status(Roles), Access privileges, Teams and Departments. Alongside setting first login password policies and resetting passwords.
</p>
<br />
