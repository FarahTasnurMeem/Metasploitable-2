# Metasploitable-2


Vulnerability Assessment and Exploitation:

**Goal A: Assess the vulnerabilities in Metasploitable 2 and exploit them using Metasploit.**

1. Perform a network scan using Nmap to identify open ports:
![image](https://github.com/user-attachments/assets/f624d463-bba4-4403-9dac-81274e8fd40f)


 **2. Using vulnerability scanners like Nessus or OpenVAS to identify known vulnerabilities.**
 ![image](https://github.com/user-attachments/assets/a62279b1-6e03-4fef-8ee8-ad1c89c35203)

 After discovering the open port 21 running vsFTPd 2.3.4 in my Nmap scan, I further investigated the vulnerability by reviewing the Nessus report. The Nessus scan flagged this specific version of vsFTPd as vulnerable due to the known backdoor in version 2.3.4, which allows for remote command execution.

Based on this information, I decided to exploit the vulnerability using Metasploit. Here’s the step-by-step process:

Reviewing Nessus Report: The Nessus scan confirmed that vsFTPd 2.3.4 was running on port 21 of the target machine, 192.168.4.54. The report highlighted the vsFTPd 2.3.4 backdoor vulnerability, which I knew could be exploited to gain root access.

Researching the Exploit: I researched the vulnerability further and identified the vsftpd_234_backdoor Metasploit exploit as an appropriate method to gain access to the system.

Using Metasploit: With the vulnerability confirmed by both Nmap and Nessus, I moved forward with Metasploit. I used the search vsftpd command to locate the correct exploit module for this backdoor and configured the module with the target IP 192.168.4.54.

Running the Exploit: After setting the parameters in Metasploit, I ran the exploit, which successfully triggered the backdoor on the vsFTPd 2.3.4 service, granting me root access.

Verifying Success: Finally, I ran the whoami command to confirm that I had gained root access to the target machine."
**Exploit vulnerabilities using Metasploit:**

![image](https://github.com/user-attachments/assets/9169ff96-232c-4246-bb52-4e14a0ea64d6)

![image](https://github.com/user-attachments/assets/00324f6d-2737-4117-982e-7513958ac631)


**Detailed report on each vulnerability from Nessus is uploaded and its exploitation process.**

**Learning Outcome:** hands-on experience with scanning, exploitation, and report generation.

**Post-Exploitation with Metasploit:**

Goal: After successfully exploiting Metasploitable 2, I will focus on post-exploitation activities.
Steps:
Gain a shell using Metasploit.

Explore the target system to gather sensitive information (e.g., passwords, flags).
Use tools like Meterpreter to escalate privileges and pivot within the network.
Install persistence mechanisms.
Learning Outcome: This will help you understand how attackers maintain access to compromised systems.
Automated Vulnerability Scanning and Exploitation Script:

Goal: Develop a script that automatically scans and exploits vulnerabilities in Metasploitable 2.
Steps:
Use Nmap for port scanning.
Implement vulnerability scanning with tools like Nikto or OpenVAS.
Automatically exploit found vulnerabilities using Metasploit's APIs or scripting.
Learning Outcome: This will teach you automation, scripting, and API usage in penetration testing.
Brute Force Attack on Metasploitable 2 Services:

Goal: Launch brute force attacks on Metasploitable 2's exposed services (e.g., SSH, FTP, HTTP).
Steps:
Use tools like Hydra or Burp Suite to brute-force credentials for services like SSH, FTP, or web applications.
Analyze the effectiveness of different password lists.
Learning Outcome: You will learn how brute force attacks work and how to mitigate them.
Network Sniffing and MITM Attacks:

Goal: Perform a Man-in-the-Middle (MITM) attack on the Metasploitable 2 machine.
Steps:
Use tools like Wireshark and Ettercap to intercept network traffic.
Analyze unencrypted traffic and extract sensitive information (e.g., credentials).
Demonstrate the dangers of unencrypted communication and how to prevent MITM attacks.
Learning Outcome: You'll understand network traffic analysis, MITM attacks, and how to secure network communications.
Web Application Testing on Metasploitable 2:

Goal: Test the vulnerable web application hosted on Metasploitable 2.
Steps:
Use Burp Suite to scan for common web application vulnerabilities (e.g., SQL injection, XSS).
Exploit these vulnerabilities to gain unauthorized access or exfiltrate data.
Assess the web application’s defenses against common attack vectors.
Learning Outcome: You’ll gain practical experience in web application security and vulnerability exploitation.
Capture the Flag (CTF) Challenge:

Goal: Create a CTF-style challenge based on Metasploitable 2.
Steps:
Set up a range of challenges within Metasploitable 2, each focusing on a different exploitation technique.
Have users attempt to find flags by exploiting the machine.
Learning Outcome: You'll enhance your ability to create and solve CTF challenges, testing various penetration techniques.
