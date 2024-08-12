# Greetings and welcome to my Cyber Security portfolio!

My name is Daniel Klein. The curiosity and fascination of languages and communication have always been by my side, but with this comes a hint of complex problem solving. Each language is built differently, thus time management plays a key role in organising the learning process, as is to the cyber security space as a whole. In my meantime I loved to tinker around with computers, like disassembling them and reassembling them while learning how these components work together, in the same way I love to tinker around with programming languages, and a fun-fact: my very first programming language I've dealt with was the BASIC interpreter on the VICE emulator. I even loved to experiment around with installing and reinstalling various discontinued Windows operating systems, some old and modern Linux distros (including BSD, CentOS, Ubuntu, Debian, etc.) and even obscure ones like HaikuOS, icaros desktop (AROS-based, Amiga compatible) and SymbOS for the MSX machines, Amstrad CPC/PCW and Enterprise 64/128.

As you traverse further on through my portfolio, you will see some tasks, functions, reports and anything else related with computer interactions and cybersecurity presented right here down below. All examples have been based on scenarios that have been conducted and practiced in the Google Cybersecurity Professional course and as well as a couple of local examples to prove my knowledge in computer related stuff.

## 1. Security incident report

In this section is presented a brief sample of a security incident report conducted alongside a summary of the scenario:


| **Section 1: Identify the network protocol involved in the incident**|
|--|
| Upon investigating the incident, it appears that a former employee had gained access to the admin panel of the yummyrecipiesforme.com website with the brute force method of guessing the login credentials. |
| **Section 2: Document the incident**|
|In turn, this event lead to a disastrous outcome of modifying the website’s source code to redirect to a malicious clone of the website called greatrecipiesforme.com which included a malicious executable that prompts the viewer to download it, causing slow downs of user devices that have viewed the website. Upon examining the tcpdump log, it seems that everything goes normally as it should, but since yummyrecipiesforme.com was modified with a couple lines of javascript, it initiated the download in which it immediately requested the address of the malicious clone of the original website.|
| **Section 3: Recommend one remediation for brute force attacks** |
|The easiest way to prevent such an attack from happening again is to immediately set up different login credentials, with a password containing at least a total of 16 characters of which it can include a minimum of 2 numbers and 2 special characters.|

In this example, the scenario described a rogue attack conducted by a former employee that used to work in a bakery. With this knowledge in place, the malicious actor proceeds to brute force attack the website of the bakery and modifies it by adding a couple of bad lines in javascript, which causes unnecessary damages for both the owner of the website, the customers and it's devices used to browse the website. 

## 2. Controls and compliance checklist
For this scenario, a toy company under the name Botium Toys established in the U.S. is a small toy making company that sells toys, plushies and the alike for customers inside the country and as well as overseas customers, namely from the E.U. countries. With the ever growing recognition from both U.S. and E.U. customers, the management is concerned that network security and compliance should be reviewed for necessary reasons. Given the fact that in the E.U. exists the GDPR policies and processing payment operations online require compliance, the IT team of the company implemented National Institute of Standards and Technology Cybersecurity Framework (NIST CSF), providing an audit scope and goals, reviewing the current assets and conducting a risk assessment. Underneath is the task I've completed alongside a recommendation.

| **Controls assessment checklist** | **No** | **Yes** |
|--|--|--|
|Least Privilege| •|
|Disaster recovery plans| •|
|Password policies|•|
|Separation of duties|•|
|Firewall||•|
|Intrusion detection system (IDS)|•|
|Backups|•|
|Antivirus software||•|
|Manual monitoring, maintenance, and intervention for legacy systems|•|
|Encryption|•|
|Password management system|•|
|Locks (offices, storefront, warehouse)||•|
|Closed-circuit television (CCTV) surveillance||•|
|Fire detection/prevention (fire alarm, sprinkler system, etc.)||•|

### Compliance checklist

| **Payment Card Industry Data Security Standard (PCI DSS)**| **No** | **Yes** |
|--|--|--|
|Only authorized users have access to customers’ credit card information|•|
|Credit card information is stored, accepted, processed, and transmitted internally, in a secure environment||•|
|Implement data encryption procedures to better secure credit card transaction touchpoints and data|•|
|Adopt secure password management policies|•|

| **General Data Protection Regulation (GDPR)** | **No**| **Yes**|
|-|-|-|
|E.U. customers’ data is kept private/secured|•|
|There is a plan in place to notify E.U. customers within 72 hours if their data is compromised/there is a breach||•|
|Ensure data is properly classified and inventoried|•|
|Enforce privacy policies, procedures, and processes to properly document and maintain data|•|

|**System and Organizations Controls (SOC type 1, SOC type 2)** |**No** |**Yes** |
|-|-|-|
|User access policies are established|•|
|Sensitive data (PII/SPII) is confidential/private|•|
|Data integrity ensures the data is consistent, complete, accurate, and has been validated||•|
|Data is available to individuals authorized to access it|•|

*Recommendation: Given the security posture Botium Toys is in, I urgently recommend to focus on data encryption including payment processing and customer data as well as configuring proper employee access privileges to PII/SPII data, least privileges, data recovery plans, password policies, manual monitoring schedule for legacy systems, back-ups, an IDS and a password management system to ensure that the company is at it’s highest digital security standards in order to prevent any type of unwanted leaks, breaches or stolen identities. Not only this would generate a loss of profit, but this would also lose trust in your customers. In regards of clientele purchasing items from outside of the United States, namely from the European Union countries, it is also highly recommended to abide to their security standards, as this may pose a massive fine if none of the standards have been met. Otherwise, physical security measures have been met to its standards.*

## 3. Linux commands and the CLI

In this scenario, we'll be going over my knowledge of the Linux CLI and it's commands that are included in the bash shell. Below is included a screenshot with explanations of every step made, what each command does and how the permissions work.

![alt text](https://github.com/danioklein/cyber-portfolio/blob/469b087a7f26eb85545ef6c6833cd5c7d6cfbcf3/Opera%20Snapshot_2024-08-08_204506.png)


> Written with [StackEdit](https://stackedit.io/).
