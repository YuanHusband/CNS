# Homework_03
CNS Elkhan Bagirov 14SEP23

### Lab Overview
Using SCAP benchmarks, this lab entails setting up a Linux host, installing the SCAP Compliance Checker (SCC) application, and performing automated security assessments. I must present documentation of their Linux distribution preference, SCC installation procedure, and scan results, including overall scores and compliance statistics. The lab concludes by uploading the findings to my GitHub repository, along with a screenshot of SCC in use.

### Linux Distribution Used

I used the RHEL7 (Red Hat Enterprise Linux v7) Linux distribution by adjusting the Vagrantfile config file.

![rhel7_config](https://github.com/YuanHusband/CNS/assets/90392600/9de4cfe8-172f-4403-9252-61c0e2e94189)

### SCC Installation

I installed the SCC tool by finding the RHEL7 version of the tool on the DOC Cyber Exchange SCAP page. I then used the "wget" command with the link to this download. I also unzipped the downloaded file.

![scc_wget](https://github.com/YuanHusband/CNS/assets/90392600/6b3acfa8-fab8-4065-a3ec-a8e478037aa2)

Preceding this, I had to install the "unzip" package: it was not included in this Linux distribution. I then added it to the binary of the OS with the rpm command.

![scc_unzip](https://github.com/YuanHusband/CNS/assets/90392600/9b197b1e-2ea2-4564-bdd6-2d110fdd9073)

### SCC Scan Results

Overall Score: 34.38%

Controls Failed: 105

Controls Passed: 55

CAT I Frequencies: 5 Failed, 5 Unchecked, 15 Passed

Below is a screenshot from the all settings report.

![allsettingsreport](https://github.com/YuanHusband/CNS/assets/90392600/c8e1343f-a8a6-456b-80e2-d6b2a8ae64e6)

Below is a screenshot of the CAT I findings.

![cat1findings](https://github.com/YuanHusband/CNS/assets/90392600/5132a30a-d5dd-4d2b-b5c5-0037753fa920)

### Screenshot of SCC Tool Running

Below is the version of the SCC Tool.

![scc_version](https://github.com/YuanHusband/CNS/assets/90392600/0bc5ae73-f16f-4f73-8a0b-f46d5180a474)

Below is the SCC Tool finishing its scan in command line.

![scc_scanresults](https://github.com/YuanHusband/CNS/assets/90392600/7d8e1d2a-ede7-4be6-a52d-38b06d46e031)
