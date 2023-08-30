# Homework_01
CNS Elkhan Bagirov 30AUG23

### Provision a Virtual Machine
This tutorial walked me through provisioning. It started off with creating a provisioning script instead of embedding all the provisioning in the Vagrantfile. Instead, we just put the script within the Vagrantfile. This specific provisioning deployed a local webserver.
![image](https://github.com/YuanHusband/CNS/assets/90392600/4583e8f2-629d-41e7-a9b8-2d2b628549ea)
![terminal_capture](https://github.com/YuanHusband/CNS/assets/90392600/82ff6631-e40a-40ea-9902-cece75b5a5b5)

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
