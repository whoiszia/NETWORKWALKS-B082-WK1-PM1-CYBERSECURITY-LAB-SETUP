# NETWORKWALKS-B084-WK1-PM1-CYBERSECURITY-LAB-SETUP
Lab environment setup for Ethical Hacking. Tools: Kali Linux-2026.3 ,  VirtualBox-7.2.22 , Windows 10/11/7/Andriod9x

                                            PROJECT OVERVIEW

This project focuses on setting up a virtual cybersecurity and penetration-testing laboratory using VirtualBox and Kali Linux.

The purpose of the lab is to create a controlled environment where cybersecurity tools, network scanning, reconnaissance, vulnerability assessment, and other security-testing activities can be performed safely and repeatedly.

The lab is configured on a private virtual network so that additional machines can be added later and used as targets for authorized security testing.

Step 1 : Install Virtual Box 
VirtualBox was installed as the hypervisor. You can download VirtualBox for Windows from https://www.virtualbox.org/

Step 2 : Create NAT Network
For "NatNetwork"; the IPV4 Prefix: 10.0.0.0/24 was configured. DHPC: enabled and IPV6: disabled/
<img width="1047" height="926" alt="Screenshot 2026-10-30 180057" src="https://github.com/user-attachments/assets/ce971445-d1e6-473d-89d2-4b6fe38ba43c" />

Why NAT? all machines connected to a NAT network can communicate with one another and also have outbound network connectivity. This setup allows the virtualized attacker and target VMs to communicate.

Step 3: Import Kali Linux
The Kali Linux  VM is available for download from https://www.kali.org/ (the official Kali Linux website)
<img width="1173" height="910" alt="image" src="https://github.com/user-attachments/assets/3b572461-e619-4391-8686-e1473d60ba4f" />

Step 4: Configure Kali linux Network
A consistent IP address makes it easier to document the lab and reference the Kali machine in future exercises.
So we set up and manual IP and have it match the subnet used in the Network Setting for on the hypervisor(VB).

<img width="703" height="547" alt="Screenshot 2026-10-30 235856" src="https://github.com/user-attachments/assets/db1da42f-769f-46cd-a1da-a81dafbc7ce7" />
 Step 5: Create VM Snapshot
<img width="855" height="291" alt="image" src="https://github.com/user-attachments/assets/d0d03484-29bb-449a-9051-f274c94d67ca" />
The snapshot represents the clean baseline of the laboratory.

If a future exercise changes or damages the VM configuration, the machine can be restored to this baseline.



                              Lab Verification
                                            command:
                  Check IP Address           ip a
                  Test Gateway               ping 10.0.0.1
                  Test Internet              ping 8.8.8.8  
                  connectivity
                  Test DNS resolution        nslookup networkwalks.com
                  Verify nmap                nmap ----version

Author: Zia Phaswana
Cybersecurity Student 
LinkedIn: www.linkedin.com/in/zia-phaswana-88117331b
                  Project Information
Program Name: Cybersecurity at Networkwalks | Week: 01 | Project: Cybersecurity & Pentesting Lab Setup | Repository: GitHub
