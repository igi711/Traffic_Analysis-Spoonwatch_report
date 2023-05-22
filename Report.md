# Traffic_Analysis-Spoonwatch_report
Malware Traffic Analysis -- 2022-01-07 - TRAFFIC ANALYSIS EXERCISE - SPOONWATCH -- report

# Contents of this file
***
- Introduction
- Executive Summary
- Details
- Indicators of Compromise (IOCs)
- Maintainer

# Introduction
***
This task located on the [malware-traffic.analysis.net](https://www.malware-traffic-analysis.net/2022/01/07/index.html). 
 In this report, I describe how I analyzed and detected the problem. I used [Wireshark](https://www.wireshark.org/) , [IDA](https://hex-rays.com/ida-pro/) and [Virustotal](https://www.virustotal.com/gui/home/upload). 

# Executive Summary
***

On 2022-01-07 at 16:07 UTC, detected an attack known as "Oski Stealer", which is a credential stealing malware. The compromised host name is DESKTOP-GXMYNO2.The following documentation describes the examination of these files.


# Details
***
The compromised host details:

- MAC address: 9c:5c:8e:32:58:f9
- IP address: 192.168.1.216
- Hostname: DESKTOP-GXMYNO2 
- Windows user account: steve.smith 

# Indicators of Compromise (IOCs)
***
## Malicious traffic:


This malware uses two obfuscation techniques, string encryption and
dynamic loading of DLLs and functions.

Before stealing data from various applications, Oski sets up its "working environment" by downloading serval DLLs.


![Malicious traffic](https://github.com/igi711/Traffic_Analysis-Spoonwatch_report/blob/main/3.png)

The compromised host sent HTTP POST requests. After sending the POST requests, the compromised host started downloading the files.

***
 
 - Format: Portable executable for 80386 (PE)
- File name: sqlite3.dll
 
![Malicious traffic](https://github.com/igi711/Traffic_Analysis-Spoonwatch_report/blob/main/18.png)

***

- Format: Portable executable for 80386 (PE)
- File name: freebl3.dll

![Malicious traffic](https://github.com/igi711/Traffic_Analysis-Spoonwatch_report/blob/main/17.png)

***

- Format: Portable executable for 80386 (PE)
- File name: mozglue.dll

![Malicious traffic](https://github.com/igi711/Traffic_Analysis-Spoonwatch_report/blob/main/16.png)

***

- Format: Portable executable for 80386 (PE)
- File Name : msvcp140.dll

![Malicious traffic](https://github.com/igi711/Traffic_Analysis-Spoonwatch_report/blob/main/15.png)

***

- Format: Portable executable for 80386 (PE)
- File name: nss3.dll

![Malicious traffic](https://github.com/igi711/Traffic_Analysis-Spoonwatch_report/blob/main/14.png)
 
 ***
 
 - Format: Portable executable for 80386 (PE)
 - File name: softokn3.dll
 
 ![Malicious traffic](https://github.com/igi711/Traffic_Analysis-Spoonwatch_report/blob/main/13.png)
  
  ***
  
 - Format: Portable executable for 80386 (PE)
 - File Name : vcruntime140.dll
   
 ![Malicious traffic](https://github.com/igi711/Traffic_Analysis-Spoonwatch_report/blob/main/12.png)

    
 ***
 
 
 The compromised host sent an HTTP POST request over the HTTP port containing a .zip file containing credentials, several autocomplete text files, and cookies. 
 The .zip file contains all the stolen files
 
 ![Malicious traffic](https://github.com/igi711/Traffic_Analysis-Spoonwatch_report/blob/main/00.png)
 

***

Details of the compromised host.
  
 ![Malicious traffic](https://github.com/igi711/Traffic_Analysis-Spoonwatch_report/blob/main/01.png)
   
 ***
   
 A compromised host sends an HTTP POST request to a malicious IP address.
   
 ![Malicious traffic](https://github.com/igi711/Traffic_Analysis-Spoonwatch_report/blob/main/02.png)



    
# Maintainer
***
Brigitta Bujdosone Kovacs 
- (ISC)² Candidate
- [kovacsbrigi.hu](https://kovacsbrigi.hu/) 
- [LinkedIn](https://www.linkedin.com/in/bujdos%C3%B3n%C3%A9-brigi-3698a5242/)
