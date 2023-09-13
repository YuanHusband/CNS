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


### Exploring Docker Images

The GCC Container  

Organization: Search Docker Hub for approved GCC images.  
Options: Specify the source code, options, and output directory to tailor the compilation.  
Uniqueness: Compile C and C++ programs in a secluded environment.  

Redmine Container  

Organization: Redmine communities and project management groups frequently maintain them.  
Options: include mounting disks for data durability and configuring utilizing environment variables.  
Uniqueness: Rapid installation of the Redmine project management system without the need for manual configuration.  

### Chosen Docker Image: vulnerable/web-dvwa

Organization: "vulnerables" on Docker Hub maintain this site.  
Options: Choose your own level of complexity, explore online vulnerabilities, or use the docker run command.  
Uniqueness: Insecure on purpose, not for use with public servers but for security training.  

### dockps Output

Below is the output to a dockps command, displaying the container names and IDs.
![dockps result](https://github.com/YuanHusband/CNS/assets/90392600/867dd10d-0cee-42a5-ac47-13125a66d612)
