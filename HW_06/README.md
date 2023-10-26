# Homework_07
CNS Elkhan Bagirov 26OCT23

### Research a Vulnerable Service: MemuPlay

https://www.exploit-db.com/exploits/46437

I wanted to research vulnerabilities within an application-based service. On the exploit database, I narrowed results to verified sources of vulnerable apps. I chose Memu Play, an android emulator for PC (primarily for gaming purposes). The operating system required is Windows 7 and above with software version 6.0.7 being verified but future versions also including the vulnerability.

The vulnerability within Memu Play is insecure file permissions. To exploit this, malicious actors can escalate privileges from a baseline: local, low privilege access with restart capabilities. An attack vector would be to replace the MemuService.exe file within the directory with a malicious file that connects back to attacker's system to give higher privileges. This executable would run upon a restart of the victim's machine and the reverse shell opens and confirms authority.

The software could defend against this by restricting file permissions and performing regular security auditing. This is why cyber students from just "chmod 777"-ing everything.
