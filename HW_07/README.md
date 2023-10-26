# Homework_07
CNS Elkhan Bagirov 26OCT23

### Research a Vulnerable Service: MemuPlay

https://www.exploit-db.com/exploits/46437

I wanted to research vulnerabilities within an application-based service. On the exploit database, I narrowed results to verified sources of vulnerable apps. I chose Memu Play, an android emulator for PC (primarily for gaming purposes). The operating system required is Windows 7 and above with software version 6.0.7 being verified but future versions also including the vulnerability.

The vulnerability within Memu Play is insecure file permissions. To exploit this, malicious actors can escalate privileges from a baseline: local, low privilege access with restart capabilities. An attack vector would be to replace the MemuService.exe file within the directory with a malicious file that connects back to attacker's system to give higher privileges. This executable would run upon a restart of the victim's machine and the reverse shell opens and confirms authority.

The software could defend against this by restricting file permissions and performing regular security auditing. This is why cyber students from just "chmod 777"-ing everything.

### Locate Vulnerability Information

The vulnerability (CVE) related to this exploit is CVE-2018-20621 which details this issue as a vulnerable binary. Privilege escalation can occur through replacing the binary with a malicious binary. Code can then be run as Authority/System.

The weakness (CWE) related to this CVE is CWE-732 named Incorrect Permission Assignment for Critical Resource. In other words, the resource is given permission settings beyond the intended actors. This is a critical weakness when looking at execution data, which is the subject for the MemuPlay exploit!

