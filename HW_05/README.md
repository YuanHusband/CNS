# Homework_04
CNS Elkhan Bagirov 28SEP23

### HW Overview

This homework delves into SSH authentication and security. It includes SSH basics, key-based authentication, and simulated password cracking.

### Learning More About SSH

Step 6 of exercise 10.2 entailed displaying currently logged in users on "serverb." The output displays a log of the root user's access.

![10 2_step6](https://github.com/YuanHusband/CNS/assets/90392600/af68cf28-900a-410c-bdee-5b34bd6e7d22)

Step 12 of exercise 10.2 is an execution of a command remotely. Uniquely, we are not accessing the interactive shell and are instead tacking the command at the end of the "ssh" command.

![10 2_step12](https://github.com/YuanHusband/CNS/assets/90392600/b2fe360b-8c85-47ea-9f6f-6a60a661f02e)

Step 4 of exercise 10.4 has us send a public key out to a user on a different machine.

![10 4_step4](https://github.com/YuanHusband/CNS/assets/90392600/dd5b9a9a-5ddd-431b-a6b9-1fe349e96f13)

Step 9 of exercise 10.4 demonstrates the ability for another user to try to gain access to the private key. A passphrase protects the private key. 

![10 4_step9](https://github.com/YuanHusband/CNS/assets/90392600/90155a24-f896-4648-a397-99977f4e9ff2)

### Applying Key-Based Authentication

I first generated a local public key.

![keygen](https://github.com/YuanHusband/CNS/assets/90392600/2a98652a-2fc2-4c7d-916b-516fdaf1970e)

Then, I used an alternative method than the redhat academy ssh-copy-id to move this public key over (command was not Windows supported). I got the information of the public key below.

![gettingpublicsshkey](https://github.com/YuanHusband/CNS/assets/90392600/fc34f8e8-8b13-42b8-8e23-1c185865f789)

I then SSHed into the jumpbox and created a text document under ~/.ssh. I added the public key from before (copy-paste).

![authorized_key_creation](https://github.com/YuanHusband/CNS/assets/90392600/8ba4ae48-eeeb-4b28-822a-fc8bdc5a980a)

Below demonstrates the ability to SSH into the jumpbox without a password: a successful key-based authentication!

![keybasedlogin](https://github.com/YuanHusband/CNS/assets/90392600/94f89315-2608-4070-8b0d-8526ebf68172)

 ### Brute Forcing Passwords


