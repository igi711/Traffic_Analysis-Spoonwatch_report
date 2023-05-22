# Traffic_Analysis-Spoonwatch_report
Malware Traffic Analysis -- 2022-01-07 - TRAFFIC ANALYSIS EXERCISE - SPOONWATCH -- report

# Contents of this file
***
- Introduction
- Executive Summary
- Details
- Indicators of Compromise (IOCs)
- Maintainers

# Introduction
***
This task located on the [malware-traffic.analysis.net](https://www.malware-traffic-analysis.net/2022/01/07/index.html). 
 In this report, I describe how I analyzed and detected the problem. I used [Wireshark](https://www.wireshark.org/) , [IDA](https://hex-rays.com/ida-pro/) and [Virustotal](https://www.virustotal.com/gui/home/upload). 

# Executive Summary
***

On 2022-01-07 at 16:07 UTC, I detected an attack known as "Oski Stealer", which is a credential stealing malware. The compromised host name is DESKTOP-GXMYNO2. During the attack, files visible as .jpg hid the malicious programs with the .pdb extension. The following documentation describes the examination of these files.


# Details
***

- MAC address: 9c:5c:8e:32:58:f9
- IP address: 192.168.1.216
- Hostname: DESKTOP-GXMYNO2 
- Windows user account: steve.smith 

# Indicators of Compromise (IOCs)
***
## Malicious traffic:

![Malicious traffic](https://github.com/igi711/Traffic_Analysis-Spoonwatch_report/blob/main/3.png)
 
***
 
 - Format: Portable executable for 80386 (PE)

 
![Malicious traffic](https://github.com/igi711/Traffic_Analysis-Spoonwatch_report/blob/main/18.png)

***

- Format: Portable executable for 80386 (PE)
- PDB file name: freebl3.pdb

![Malicious traffic](https://github.com/igi711/Traffic_Analysis-Spoonwatch_report/blob/main/17.png)

***

- Format: Portable executable for 80386 (PE)
- PDB file name: mozglue.pdb

![Malicious traffic](https://github.com/igi711/Traffic_Analysis-Spoonwatch_report/blob/main/16.png)

***

- Format: Portable executable for 80386 (PE)
- PDB File Name : msvcp140.i386.pdb

![Malicious traffic](https://github.com/igi711/Traffic_Analysis-Spoonwatch_report/blob/main/15.png)

***

- Format: Portable executable for 80386 (PE)
- PDB file name: nss3.pdb

![Malicious traffic](https://github.com/igi711/Traffic_Analysis-Spoonwatch_report/blob/main/14.png)
 
 ***
 
 - Format: Portable executable for 80386 (PE)
 - PDB file name: softokn3.pdb
 
 ![Malicious traffic](https://github.com/igi711/Traffic_Analysis-Spoonwatch_report/blob/main/13.png)
  
  ***
  
 - Format: Portable executable for 80386 (PE)
 - PDB File Name : vcruntime140.i386.pdb
   
 ![Malicious traffic](https://github.com/igi711/Traffic_Analysis-Spoonwatch_report/blob/main/12.png)

    
# Maintainers
***
Brigitta Bujdosone Kovacs 
- (ISC)² Candidate
- [kovacsbrigi.hu](https://kovacsbrigi.hu/) 
- [LinkedIn](https://www.linkedin.com/in/bujdos%C3%B3n%C3%A9-brigi-3698a5242/)
