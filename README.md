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

### Second example
---

|**Date**|**Entry**|
|-|-|
|04-07-2024 Thursday @ 1100 AM| Phishing: stolen and deleted credentials|
|Description| A Danish insurance company fell victim of a phishing attack which resulted into leaked credentials and some data deleted|
|Tools utilized| Splunk|
| | 1. Who: unknown |
| The| 2. What: Danish insurance company |
| Five|3. When: 04-07-2024 @ 1100 AM |
| W's|4. Where: Copenhagen, DK |
| |5. Why: possibly to use credentials for fraudulent activities|
|Adnotations| A phishing attack was conducted towards an insurance company located in Copenhagen, Denmark. Several employees have received a phishing email that identically resebled the login prompt to their network of business. Upon every attempt of loging in, employees couldn't access further because the login screen hasn't changed, implying that it was a fake domain created by an unknown third party. Soon to be discovered, the malicious actor managed to gain access to sensitive customer data in which some entries were either manipulated or deleted from the database. To prevent any further damage, the organizations' netowrking systems have been temporarily shutdown, saftey measures were implemented to fortify network defences such as firewall rules being updated, two-factor authentication and the implementation of updating passwords every six months. A back-up of the data has been restored to the damaged database and IT assistance was requested to further inspect this incident from their side. |

### Third example
---

|**Date**|**Entry**|
|-|-|
|05-04-2024 Friday @ 0830 AM| Mis-use: employee downloaded software without correct authorization |
|Description| A private humanitarian organization employee downloaded software on their workstation without prior authorization from administrator|
|Tools utilized| Datadog|
| | 1. Who: employee |
| The| 2. What: A private humanitarian organization |
| Five|3. When: 05-04-2024 @ 0830 AM |
| W's|4. Where: Gdansk, PL |
| |5. Why: eployee wanted to try out something on his workstation because he forgot his private laptop at home |
|Adnotations| Early in the morning I've received a ticket of an employee downloading software without the proper administrator authorization. The employee managed to download a copy of an image manipulation program from a third party source, which resulted the workstation to fall in computing performance, taking up storage and possibly having installed spyware along with the program since it wasn't straight from the official website. The employee was asked to remove the program immediately to prevent any further damage, a software swipe was done to check if everything is intact and erradication was conducted. The workstation was restored to it's previous state with a snapshot that was made from the IT team by their side.|


## 6. Automation with Python

In this example, we'll be going over the automatics of Python and what it can do for us to ease certain tasks that would require a lot of effort and time put in. For this scenario my task was to update a list of IPs that were supposed to be removed with a list that's included in the source file. 

![alt_text](https://github.com/danioklein/cyber-portfolio/blob/e63bc432545eb295ef8cb217d872ef37e380de5a/Opera%20Snapshot_2024-08-13_172622_www.coursera.org.png)

In this snippit, we are preparing the main string which is `import_file` and the list known as `remove_list` to later on filter out the IP addresses that need to be removed from the `allow_list.txt` file. First, I've printed out the following string and list to check if the code is properly functioning. Comments are left over so that other fellow members can understand the code if further editing would be necessary.

---
![alt_text](https://github.com/danioklein/cyber-portfolio/blob/e63bc432545eb295ef8cb217d872ef37e380de5a/Opera%20Snapshot_2024-08-13_172924_www.coursera.org.png)

The next step was to implement the `open()` function in it's initial stage. The compiler returns an error because it expects more detail in order to handle the rest of the function, and that will be presented in the next step.

---
![alt_text](https://github.com/danioklein/cyber-portfolio/blob/e63bc432545eb295ef8cb217d872ef37e380de5a/Opera%20Snapshot_2024-08-13_173124_www.coursera.org.png)

Here we have the fully functional code that was meant to be printed out. The indented line `ip_adresses = file.read()` was missing so that it can read directly from the file. Finishing this step I've left a `print()` statemnt to check if the code runs properly.

---
![alt_text](https://github.com/danioklein/cyber-portfolio/blob/e63bc432545eb295ef8cb217d872ef37e380de5a/Opera%20Snapshot_2024-08-13_173336_www.coursera.org.png)

In this step, I've used `ip_addresses = ip_addresses.split()` statement to convert the string to a list, thus showing that it executed the code successfully. 

---
![alt_text](https://github.com/danioklein/cyber-portfolio/blob/e63bc432545eb295ef8cb217d872ef37e380de5a/Opera%20Snapshot_2024-08-13_173621_www.coursera.org.png)

In this stage I'm setting up a loop statment, otherwise known as an iterative statement to loop through the text file so that later on this code can filter through the IP addresses that are unwanted. The code that represents that is `for element in ip_addresses:` where `element` is the loop variable. 

---
![alt_text](https://github.com/danioklein/cyber-portfolio/blob/e63bc432545eb295ef8cb217d872ef37e380de5a/Opera%20Snapshot_2024-08-13_173855_www.coursera.org.png)

Later on, I'm setting up a conditional statement `if element in remove_list:` which tells the interpreter to look through the `remove_list` followed by a `ip_addresses.remove(element)` to remove the matching IP address specified in the `remove_list` list. 

---
![alt_text](https://github.com/danioklein/cyber-portfolio/blob/e63bc432545eb295ef8cb217d872ef37e380de5a/Opera%20Snapshot_2024-08-13_174118_www.coursera.org.png)

In the next step I'm implememnting a conversion statmenet `ip_addresses = "".join(ip_addresses)` followed by the `with open(import_file, "w") as file:` and `file.write(ip_addresses)` statement so that it converts the filtered data back into a string, followed by an overwriting routine to the `import_file` string with the removed IP addresses. In this case there is no printed results because no such statement is included in the code.

---
![alt_text](https://github.com/danioklein/cyber-portfolio/blob/e63bc432545eb295ef8cb217d872ef37e380de5a/Opera%20Snapshot_2024-08-13_174644_www.coursera.org.png)

Now here is where we'll be displaying the results. As earlier we'll be implementing another read routine: `with open(import_file, "r") as file:` `text = file.read()` followed by a print statement `print(text)` to show the allowed IP addresses.

---
![alt_text](https://github.com/danioklein/cyber-portfolio/blob/e63bc432545eb295ef8cb217d872ef37e380de5a/Opera%20Snapshot_2024-08-13_174904_www.coursera.org.png)

So now this is where it get's a little advanced. On the very beginning of the code, this whole routine will be converted into a customized function using this statement `def update_file(import_file, remove_list):` where the `import_file` is the source document and the `remove_list` will be the specified IP addresses to be removed in future allow lists.

---
![alt_text](https://github.com/danioklein/cyber-portfolio/blob/e63bc432545eb295ef8cb217d872ef37e380de5a/Opera%20Snapshot_2024-08-13_175225_www.coursera.org.png)

With our customized function, I've added another line of code `update_file("allow_list.txt", [..IP ADDRESSES..])` along with the edited line `with open("allow_list.txt", "r") as file:` to match the criteria of the function and `text = file.read()` ended with a print statement `print(text)` to display the final list of allowed IP addresses.


