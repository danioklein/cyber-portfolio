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

---
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

---
*Recommendation: Given the security posture Botium Toys is in, I urgently recommend to focus on data encryption including payment processing and customer data as well as configuring proper employee access privileges to PII/SPII data, least privileges, data recovery plans, password policies, manual monitoring schedule for legacy systems, back-ups, an IDS and a password management system to ensure that the company is at it’s highest digital security standards in order to prevent any type of unwanted leaks, breaches or stolen identities. Not only this would generate a loss of profit, but this would also lose trust in your customers. In regards of clientele purchasing items from outside of the United States, namely from the European Union countries, it is also highly recommended to abide to their security standards, as this may pose a massive fine if none of the standards have been met. Otherwise, physical security measures have been met to its standards.*

## 3. Linux commands and the CLI

In this scenario, we'll be going over my knowledge of the Linux CLI and it's commands that are included in the bash shell. Below is included a screenshot with explanations of every step made, what each command does and how the permissions work.

For this project, my task was to update certain file permissions due to a security policy revision.

![alt text](https://github.com/danioklein/cyber-portfolio/blob/469b087a7f26eb85545ef6c6833cd5c7d6cfbcf3/Opera%20Snapshot_2024-08-08_204506.png)

---
As you can see, commands like `chmod` and `ls -la` were utilized to make the permission changes possible. For one, the command `ls -la` was used to list the directory in full detail including the hidden files that start with a `.` alongside the current permissions displayed from the left side with these letters:`drwxrwxrwx` and the command `chmod` was used to delete or elevate privileges. In order to add or remove a permission to a user, group or other, the file first has to be inspected with what permissions are in place. If we'd want to add read and write access for the user, then the input command would go like this:`chmod u+rw FILENAME.txt` and if we'd want to remove that same set of access, all we have to do is swap the `+` with a `-`, which gives us this input command:`chmod u-rw FILENAME.txt`. Multiple groups can be changed at once with any of the following letters: `u`, `g` and `o`. To elevate read and write access for multiple groups, all we have to do is specify which ones we want to allow for. For example: `chmod ug+rwx FILENAME.txt` grants read, write and execute access for the user and group respectively. As seen above, you can also add a pipe `|` which tells the command line to execute the next command that's been typed into the prompt, and as you can see I've given and removed access for two files at the same time. The permissions structure goes as such: `drwxrwxrwx` in which the first letter `d` indicates a directory, the first three `rwx` indicate `r`ead, `w`rite and e`x`ecute for the **user**, the second set of those letters indicate the same but for the **group** and the last set of those letters indicate the same thing but for the **other**. 

In MS-DOS and similar disk operating systems, the command `ls -la` would be equivalent to the `dir /w` command, whereas the equivalent of `chmod` would be `attrib`, but since the MS-DOS file structure is different in comparision to Linux/Unix, MS-DOS has different permission values. 

## 4. Applying filters with SQL commands

In this section we'll be going over some simple yet effective filters that can be utilized to find and locate specific information. With the project below, I was tasked to locate failed login attempts that happened out of working hours and workstations for certain departments that required a software update.

![alt_text](https://github.com/danioklein/cyber-portfolio/blob/3a99a2549e70dd6f0ed0d99c9e93246784ae3cbf/Opera%20Snapshot_2024-08-12_191511_www.cloudskillsboost.google.png)

As seen here, my main goal was to find failed login attempts that happened before 6:00 PM, and with the results provided it seems that there are quite some tries over here. The operator `AND` includes two columns in this case: `login_time` anywhere `> 18:00 AND` if the login attempts were `FALSE` or `0`, or simply put unsuccessful.

---
![alt_text](https://github.com/danioklein/cyber-portfolio/blob/3a99a2549e70dd6f0ed0d99c9e93246784ae3cbf/Opera%20Snapshot_2024-08-12_192043_www.cloudskillsboost.google.png)
![alt_text](https://github.com/danioklein/cyber-portfolio/blob/3a99a2549e70dd6f0ed0d99c9e93246784ae3cbf/Opera%20Snapshot_2024-08-12_192124_www.cloudskillsboost.google.png)

Over here with this next step I was supposed to retrieve any login attempts that occured between the 8th and the 9th. The operator `OR` serves as a condition marker to include one `OR` another, and in this case the dates of `2022-05-08` and `2022-05-09` were specified in order to return the necessary information needed. 

---
![alt_text](https://github.com/danioklein/cyber-portfolio/blob/3a99a2549e70dd6f0ed0d99c9e93246784ae3cbf/Opera%20Snapshot_2024-08-12_192420_www.cloudskillsboost.google.png)
![alt_text](https://github.com/danioklein/cyber-portfolio/blob/3a99a2549e70dd6f0ed0d99c9e93246784ae3cbf/Opera%20Snapshot_2024-08-12_192456_www.cloudskillsboost.google.png)

With this step I was tasked to filter out login attempts that happened outside of Mexico, and as you can see there are quite some attempts here. It's no wonder the organization wanted to conduct a security update for their machines. However, in this example the operator `NOT` was utilized in order to weed out any login location that happened outside of Mexico, where `MEX%` was used to filter out both the values `MEX` and `MEXICO`.

---
![alt_text](https://github.com/danioklein/cyber-portfolio/blob/3a99a2549e70dd6f0ed0d99c9e93246784ae3cbf/Opera%20Snapshot_2024-08-12_192813_www.cloudskillsboost.google.png)

Here I was supposed to find out how many machines are there in any of the East offices within the Marketing department. Not that much to be honest. Here the operator `AND` has been used to include both the `East%` to locate more than one East office and the `department = 'Marketing'` to return results found within the table.

---
![alt_text](https://github.com/danioklein/cyber-portfolio/blob/3a99a2549e70dd6f0ed0d99c9e93246784ae3cbf/Opera%20Snapshot_2024-08-12_194557_www.cloudskillsboost.google.png)
![alt_text](https://github.com/danioklein/cyber-portfolio/blob/3a99a2549e70dd6f0ed0d99c9e93246784ae3cbf/Opera%20Snapshot_2024-08-12_194620_www.cloudskillsboost.google.png)

To be honest, at first this one was quite confusing to me but then I realized what I was doing wrong. In this case both conditions were needed to be inlcuded to return proper results, as in `department LIKE 'Finance' OR department LIKE 'Sales'` instead of `department LIKE 'Finance' OR 'Sales'`. 

---
![alt_text](https://github.com/danioklein/cyber-portfolio/blob/3a99a2549e70dd6f0ed0d99c9e93246784ae3cbf/Opera%20Snapshot_2024-08-12_194801_www.cloudskillsboost.google.png)
![alt_text](https://github.com/danioklein/cyber-portfolio/blob/3a99a2549e70dd6f0ed0d99c9e93246784ae3cbf/Opera%20Snapshot_2024-08-12_194820_www.cloudskillsboost.google.png)

And here is a second example of utilizing the `NOT` operator to exclude certain information.

In conclusion, these filters are simple yet effective and does not require that much rocket science. Although in certain scenarios where there are longer queries then it might get a little more confusing. 

## 5. Incident handler journal

Here in this part of my portfolio will be included five incident journal entries as per requisite by the Google Cyber Security Certification course. In this section there will be various life-like scenarios covered to demonstrate my reporting an adnotation skills.

In this example, we'll be going over an incident journal that covers a scenario where a malicious attack was counducted by unethical hackers onto a U.S. health care clinic encrypting lots and lots of patient and company info in exchange for a large amount of money to decrypt it. As you may have noticed, in certain reports I tend to keep stuff short, clean, and precise as possible. My adnotation style for notes is somewhat of a hybrid between a programming language and a natural language. For example, the term uhackers is short for unethical hackers, where ehackers would be short for ethical hackers. To some this might seem confusing, but as long as it works for me and I know what's going on then Bob's your uncle. :)

### First example
---

|**Date**|**Entry**|
|-|-|
|13-08-2024 Tuesday @ 0900 AM| Malicious attack: Phishing; Ransomeware |
|Description| A U.S. health care clinic became victim under a malicious:ransomeware attack conducted by uhackers|
|Tools utilized| Splunk, Datadog|
| | 1. Who: uhackers |
| The| 2. What: target: U.S. health care clinic |
| Five|3. When: 13-08-2024 @ 0900 AM |
| W's|4. Where: Madison, WI |
| |5. Why: money exchange for ransome |
|Adnotations| This attack was deployed through phishing. Several employees received a suspicious email by the same style with the same malicious attatchment included. Upon opening the email it was noticed that the malicious download was initiated once the email received the <email read> flag, causing it to disable some computers and eventually restricting access to vital data. Once the ransomeware got ahold of every machine, the network and other services linked to the health care clinic had to be shutdown and backup technical assistance was requested by the clinic to avoid paying the uhackers a large amount of cash to decrypt the files. |

### First example
---

|**Date**|**Entry**|
|-|-|
|13-08-2024 Tuesday @ 0900 AM| Malicious attack: Phishing; Ransomeware |
|Description| A U.S. health care clinic became victim under a malicious:ransomeware attack conducted by uhackers|
|Tools utilized| Splunk, Datadog|
| | 1. Who: uhackers |
| The| 2. What: target: U.S. health care clinic |
| Five|3. When: 13-08-2024 @ 0900 AM |
| W's|4. Where: Madison, WI |
| |5. Why: money exchange for ransome |
|Adnotations|

### Second example
---

|**Date**|**Entry**|
|-|-|
|13-08-2024 Tuesday @ 0900 AM| Malicious attack: Phishing; Ransomeware |
|Description| A U.S. health care clinic became victim under a malicious:ransomeware attack conducted by uhackers|
|Tools utilized| Splunk, Datadog|
| | 1. Who: uhackers |
| The| 2. What: target: U.S. health care clinic |
| Five|3. When: 13-08-2024 @ 0900 AM |
| W's|4. Where: Madison, WI |
| |5. Why: money exchange for ransome |
|Adnotations|

### Third example
---

|**Date**|**Entry**|
|-|-|
|13-08-2024 Tuesday @ 0900 AM| Malicious attack: Phishing; Ransomeware |
|Description| A U.S. health care clinic became victim under a malicious:ransomeware attack conducted by uhackers|
|Tools utilized| Splunk, Datadog|
| | 1. Who: uhackers |
| The| 2. What: target: U.S. health care clinic |
| Five|3. When: 13-08-2024 @ 0900 AM |
| W's|4. Where: Madison, WI |
| |5. Why: money exchange for ransome |
|Adnotations|

### Fourth example
---

|**Date**|**Entry**|
|-|-|
|13-08-2024 Tuesday @ 0900 AM| Malicious attack: Phishing; Ransomeware |
|Description| A U.S. health care clinic became victim under a malicious:ransomeware attack conducted by uhackers|
|Tools utilized| Splunk, Datadog|
| | 1. Who: uhackers |
| The| 2. What: target: U.S. health care clinic |
| Five|3. When: 13-08-2024 @ 0900 AM |
| W's|4. Where: Madison, WI |
| |5. Why: money exchange for ransome |
|Adnotations|

### Fifth example
---

|**Date**|**Entry**|
|-|-|
|13-08-2024 Tuesday @ 0900 AM| Malicious attack: Phishing; Ransomeware |
|Description| A U.S. health care clinic became victim under a malicious:ransomeware attack conducted by uhackers|
|Tools utilized| Splunk, Datadog|
| | 1. Who: uhackers |
| The| 2. What: target: U.S. health care clinic |
| Five|3. When: 13-08-2024 @ 0900 AM |
| W's|4. Where: Madison, WI |
| |5. Why: money exchange for ransome |
|Adnotations|


