# Homework_04
CNS Elkhan Bagirov 28SEP23

### Lab Overview
I created regular user accounts in Active Directory, tested their functionality, set a new PowerShell execution policy on the domain controller, created and ran custom PowerShell scripts, and executed a provided script to make changes to Active Directory. I documented my actions and provided screenshots as evidence.

### Creating AD Users (2)

I created a user using the Server Manager GUI, specifically the Active Directory Users and Computers.

Below is a screenshot of the "Member Of" and "Account" tabs for the user.

![MembersOf_genuser](https://github.com/YuanHusband/CNS/assets/90392600/a4671c17-42f2-4b88-916d-a6f88db1390a)
![Account_genuser](https://github.com/YuanHusband/CNS/assets/90392600/fe2f98d3-f65c-410b-86a9-5664f92f7595)

### Logon w/ User Account (3)

 After user creation, windows needed to set up and the login session of the new user was now available. Below is proof of the login session by going to the top of the settings application.
 
 ![logon_session_information](https://github.com/YuanHusband/CNS/assets/90392600/a503ea24-b17d-4e8a-98a4-2bf5ef6bfd9c)

 ### Changing Powershell Permissions (4.1)

We adjusted the LocalMachine and CurrentUser scopes to have the "AllSigned" execution policy. This augments the security by requiring that all scripts be signed by a trusted source prior to running. Doing this on the LocalMachine scope makes the scripts on the machine be verified. By adding in the CurrentUser redundancy, it ensures that each user's scripts also must be signed. Our group thinks we should be protected from ourselves.

 ![ExecutionPolicy](https://github.com/YuanHusband/CNS/assets/90392600/59ddc893-a022-453a-a69d-c7efb6163fe5)

 ### Test Powershell Script Execution (4.2)

 I created a Powershell Script that does a basic greeting outwards with the source code found in the HW_04 folder of the repository.

 Below is a screenshot of the command used to run the script and the output of the script.

 ![script_output](https://github.com/YuanHusband/CNS/assets/90392600/cddcfe68-bfee-441c-8cf2-3ae0b066398e)

 ### Create More AD Objects (4.3)

We were definitely more than a little skeptical of BadBlood. We read that it fills the domain with thousands of objects and different results in producing domains, users, groups, computers, and permissions.

Below is the opening clause, not too inviting....
![badblood muck](https://github.com/YuanHusband/CNS/assets/90392600/90bd69d0-bd2d-42c6-a94c-8b04944db622)

Then, we took the plunge and observed it running, for a while.

![BadBlood stuff and things](https://github.com/YuanHusband/CNS/assets/90392600/9f030b22-19fa-4385-b7e6-c18b0cd3c6c6)

Below shows the augmentation in number of those previous categories. There are way more branches and users. The domain feels lived in!

![Proof of BadBlood](https://github.com/YuanHusband/CNS/assets/90392600/90515ea4-8772-4dd9-8e28-59e7b55a7298)
