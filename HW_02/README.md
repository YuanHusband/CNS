# Homework_02
CNS Elkhan Bagirov 7SEP23

### Lab Overview
My Docker container investigation journey continues with this homework. The first step is to use HostA as a template from the Docker Compose file. Next, based on my investigation, select a fresh Docker image for the "attacker" computer from Docker Hub. This new container will be added to my Docker Compose file after being configured as necessary. To guarantee this new configuration's operation, including network connectivity and service access, I'll build, deploy, and test it afterward.

Below, I changed the docker-compose.yml to include the new attacker and image.

![dockercomposeml (codechange)](https://github.com/YuanHusband/CNS/assets/90392600/8791ffc3-3d0e-4d45-ae28-145f287e0873)

I then docksh'd into the attacker host and tried pinging the different hosts on the network (only unable to ping internal hosts of router because of firewall).

![pinging and docksh results](https://github.com/YuanHusband/CNS/assets/90392600/6b24ef60-1317-45b3-a557-52361e3b36c2)

Finally, I tested the functionality of this image in providing a easily comprised web app that I logged into with default user and password.

![Network Service Access](https://github.com/YuanHusband/CNS/assets/90392600/cc011320-a94f-4505-837c-8d4b9a251db3)

![Network Service Access_login](https://github.com/YuanHusband/CNS/assets/90392600/edb2f172-f53c-4205-99cb-a4f10732969b)


### Configure the Network
This tutorial allowed me to establish port forwarding using the Vagrantfile. I used the template and tutorial to change the config for the vm network to be hosted on 4567. From here, I accessed this file from the browser at the local host : portnumber (127.0.0.1/4567).
![image](https://github.com/YuanHusband/CNS/assets/90392600/9c1f4ec3-8c54-4e7a-97bc-cb73a63daf69)
![Web_capture](https://github.com/YuanHusband/CNS/assets/90392600/7a7d401c-fbdb-4d7e-9f13-08a6b5021ec3)

### Shell Provisioner
Users can run shell scripts on a virtual machine while it is being provisioned using Vagrant's Shell provisioner. This provisioner is helpful for executing commands and configuring settings. The Vagrantfile allows users to define inline shell scripts or specify a path to external shell script file (as done in Homework 1). It is a flexible choice that works by establishing an SSH connection to the target computer.   

File Format: No specific file format (follows syntax of shell language on machine)  
Key Terms Associated: Inline Commands, Shell Script File, Provisioning, SSH

### File Provisioner
![image](https://github.com/YuanHusband/CNS/assets/90392600/1f70da1e-c08d-4657-9f8f-f1bf59cc9949)
