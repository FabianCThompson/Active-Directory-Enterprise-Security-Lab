Domain: Identity & Access Management

Objective: Master Active Directory (AD) to manage users, groups, policies, and security configuration in a Windows enterprise environment.

Key Outcomes:

Create Organizational Units (OUs) and user accounts.
Configure domain-level and OU-level Group Policies.
Enforce security policies (password complexity, access control
Lab Setup

Topology:

Windows Server: 192.168.1.10

![Screenshot 2025-06-04 190150](https://github.com/user-attachments/assets/a0139dda-8440-44fb-a945-a633e4c10682)

Domain: campus.edu


Tools used:

Active Directory Users & Computers (dsa.msc)
Group Policy Management Console
Command Prompt (net user, gpupdate)
Lab Tasks

Task 1: Create Organizational Units & User Accounts
Open Active Directory Users and Computers via dsa.msc.

![Screenshot 2025-06-05 105936](https://github.com/user-attachments/assets/d4e2daa7-b75e-4ce9-af94-deaa02c8381b)

Right-click domain (campus.edu) → New → Organizational Unit.
Name: Minecraft (example OU).
![Screenshot 2025-06-05 104517](https://github.com/user-attachments/assets/2863c7f9-72f6-4769-9b06-b3768da367e7)![Screenshot 2025-06-05 104952](https://github.com/user-attachments/assets/3c0e7b7a-008b-47fe-afaa-da702855b1f2)




Create users inside Minecraft OU:
Right-click OU → New → User.
Usernames: creeper, zombie, steve.
Password: P@ssw0rd (uncheck "User must change password at next logon")

![Screenshot 2025-06-05 110608](https://github.com/user-attachments/assets/e44d18d7-e816-4938-b568-cbb318772e60)

![Screenshot 2025-06-05 110939](https://github.com/user-attachments/assets/665072b7-5609-4a40-aeb5-92b14a7b306b)
![Screenshot 2025-06-05 111023](https://github.com/user-attachments/assets/26519fa9-d3f1-40b9-b9f1-8ce39e66802d)
![ci1un1mb](https://github.com/user-attachments/assets/0e860cbb-1879-4188-b050-6d6e3fefb0fb)

Why This Matters:

Organizational Units mirror organizational structure (e.g., Finance, IT). Policies applied to an Organizational Unit affect all contained objects.

Task 2: Set Domain-Level Password Policy
Open Group Policy Management → Expand Forest: campus.edu → Domains → campus.edu.
![Screenshot 2025-06-05 114332](https://github.com/user-attachments/assets/d3eaeb2d-6e8b-4fb9-970b-3c67391bdba5)


Edit Default Domain Policy.
![Screenshot 2025-06-05 115031](https://github.com/user-attachments/assets/a21c93e1-33b3-4772-bd9c-62b4ea2df859)


Navigate to: Computer Configuration → Policies → Security Settings → Account Policies → Password Policy.
![5lyxq8yi](https://github.com/user-attachments/assets/9c19b782-3eb3-4595-b868-5a0e42fe8de7)


Set the Minimum password length to 10 characters
![Screenshot 2025-06-05 115655](https://github.com/user-attachments/assets/b79ce92d-0b97-4a08-b37c-f21f301e8745)



Now we need to refresh the group policy in the Command Prompt
![Screenshot 2025-06-05 120133](https://github.com/user-attachments/assets/a522cdef-bc19-498d-b5b3-4f9cc27706c5)



Security Impact:

Domain-level policies enforce baseline security (e.g., password complexity) across all users.





F
