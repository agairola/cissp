## Malicious Code

Malicious code objects include a broad range of programmed computer security threats that exploit various network, operating system, software, and physical security vulnerabilities to spread malicious payloads to computer systems.

* Computer viruses and Trojan horses depends on irresponsible use of computer by humans.

* Worms, spread rapidly among vulnerable systems under their own power.

### Sources of Malicious Code

* In the early days of computer security, malicious code writers were extremely skilled (albeit misguided) software developers who took pride in carefully crafting innovative malicious code techniques. 

* They use to help in exposing security holes.

* Modern times have given rise to the script kiddie—the malicious individual who doesn’t understand the technology behind security vulnerabilities but downloads ready-to-use software (or scripts) from the internet and uses them to launch attacks against remote systems.

* Indeed international organized crime syndicates are known to play a role in malware proliferation. Located in countries with weak law enforcement mechanisms, use malware to steal the money and identities of people from around the world. **Example**, Zeus Trojan (banking passwords) believed to be product of Eastern European organized crime ring. 

* **Advanced persistent threat (APT)**: APTs are sophisticated adversaries with advanced technical skills and significant financial resources. They have access to zero-day exploits which are unknown to vendors. **Example**, Stuxnet, one example of APT-developed malware.

### Viruses

*  According to Symantec, one of the major antivirus software vendors, there were over 357 million strains of malicious code roaming the global network in 2016 and this trend only continues, with some sources suggesting that 200,000 new malware variants appear on the internet every day!

* As with biological viruses, computer viruses have two main functions—**propagation** and **destruction**.

* The **propagation** function defines how the virus will spread from system to system, infecting each machine it leaves in its wake. A virus’s payload delivers the **destructive power** by implementing whatever malicious activity the virus writer had in mind. This could be anything that negatively impacts the confidentiality, integrity, or availability of systems or data.

### Virus Propagation Techniques

* Four common propagation techniques: master boot record infection, file infection, macro infection, and service injection.

* **Master boot record infection**

  * MBR is extremely small (usually 512 bytes), it can’t contain all the code required to implement the virus’s propagation and destructive functions. To bypass this space limitation, MBR viruses store the majority of their code on another portion of the storage media. When the system reads the infected MBR, the virus instructs it to read and execute the code stored in this alternate location, thereby loading the entire virus into memory and potentially triggering the delivery of the virus’s payload.

  * MBR viruses act by redirecting the system to an infected boot sector, which loads the virus into memory before loading the operating system from the legitimate boot sector.

* **File Infector Viruses**

  * File infector viruses may slightly alter the code of an executable program (.exe and .com), thereby implanting the technology the virus needs to replicate and damage the system.

  * A variation of the file infector virus is the *companion virus*. These viruses are self-contained executable files that escape detection by using a filename similar to, but slightly different from, a legitimate operating system file. They rely on the default filename extensions that Windows-based operating systems append to commands when executing program files (.com, .exe, and .bat, in that order). For example, if you had a program on your hard disk named game.exe, a companion virus might use the name game.com. 

* **Macro Viruses**

  * Its a common practice for software application to create scripts to automate certain tasks. Common programming language used is Visual Basic for Applications (VBA).

  * Macro viruses first appeared on the scene in the mid-1990s, utilizing crude technologies to infect documents created in the popular Microsoft Word environment. 
 
  * Examples, *Melissa Virus* and *I Love You Virus* are few examples that uses Word documents to exploit vulnerability in other application like Microsoft Outlook. 

  * **Safeguard**: Do not allow untrusted macro to execute without explicit user permission.

* **Service Injection Viruses**

  * Its a technique where virus inject themselves into trusted running processes like svchost.exe, winlogin.exe, and explorer.exe. Its effective cause this will bypass detection via any anti-virus.

  * **Safeguard**: Keep application up-to-date with the latest security patches. 

### Platforms Vulnerable to Viruses

  * As per av-test.org, researchers estimated that 77 percent of malware in existence targets the Windows platform in 2017. Which was 95 % in 2016.

  * Above change in the percentage reflects that malware focus has changed from windows to mobile and/or other platforms.

  * Malware targeting Mac tripled in 2016.

  * Malware for Android doubled in 2016.

### Antivirus Mechanisms

  * Popular softwares include, Microsoft Security Essentials, McAfee AntiVirus, Avast Antivirus, Trend Micro Antivirus, ESET NOD32 Antivirus, Sophos Antivirus, and Symantec Norton AntiVirus, but a plethora of other products on the market offer protection for anything from a single system to an entire enterprise; other packages are designed to protect against specific common types of virus invasion vectors, such as inbound email.

  * Most of software are *signature-based detection* and maintain (frequently update) large database that contains telltale characteristic of known viruses. Action includes:
    * Eradicate the virus (disinfect the file)
    * Quarantine the file for manual examination
    * Delete the file most when it is deemed dangerous

  * Another technique is heuristic-based mechanisms to detect potential malware infections. Which analyzes behavior of a software to telltale sign of virus activity, example privilege escalation, alter unrelated OS files etc. Mostly file that is deemed harmful is quarantined and send to malware analysis tool where they are executed in an isolated but monitored environment, then blacklist it everywhere.

  * Another example is of Tripwire data integrity assurance package, also provide a secondary antivirus functionality. Alerts admins about unauthorized file modification. It keeps a hash table of all the files and if there is any modification it would be able to alarm about modification unless it was intended. 

### Virus Technologies

This this section we will exmines **four** specific types of viruses that use sneaky techniques in an attempt to escape detection:

**Multipartite Viruses**

  * It uses more than one propagation technique in an attempt to penetrate systems that defend against only one method or the other.

  * **Example:** Marzia virus which infected critical EXE and COM files in Windows, like command.exe but attaching 2048 bytes of malicious message to each file (***First* - file infector virus**) then after 2 hours effected the MBR and loads the virus to the memory (***Second* - Master boot record infection**)

**Stealth Viruses** 

  * It hides themselves by actually tampering with the operating system to fool antivirus packages into thinking that everything is functioning normally.

  * **Example:** A stealth boot sector virus might overwrite the system’s master boot record with malicious code but then also modify the operating system’s file access functionality to cover its tracks. So when an AV requests a copy of MBR it receives a clean copy. 

**Polymorphic Viruses**

  * Actually modify their own code as they travel from system to system. The virus’s propagation and destruction techniques remain the same, but the signature of the virus is somewhat different each time it infects a new system, its is done to evade signature-based detection. 

  * But AVs not have detection based on polymorphism techniques which helps them detect these viruses. But AV takes longer time to create signatures.

**Encrypted Viruses**

  * It is quite similar to polymorphic viruses—each infected system has a virus with a different signature.

  * Encrypted viruses use a very short segment of code, known as the *virus decryption routine*, which contains the cryptographic information necessary to load and decrypt the main virus code stored elsewhere on the disk. Each infection utilizes a different cryptographic key, causing the main code to appear completely different on each system. 

  * However, the virus decryption routines often contain telltale signatures that render them vulnerable to updated antivirus software packages.

### Hoaxes

  * No discussion of viruses is complete without mentioning the nuisance and wasted resources caused by virus hoaxes.

  * EMAIL messages used to spread the infection

  * One famous example of such a hoax is the Good Times virus warning that first surfaced on the internet in 1994 and still circulates today.

### Logic Bombs

  * Logic bombs are malicious code objects that infect a system and lie dormant until they are triggered by the occurrence of one or more conditions such as time, program launch, website logon, and so on.

  * Many viruses and Trojan horses contain a logic bomb component.

### Trojan Horses

  * Its software program that appears benevolent but carries a malicious, behind-the-scenes payload that has the potential to wreak havoc on a system or network.

  * *Example*: A piece of software that claims that PC users can run XBOX games on PC. Once user installed this software nothing happened, but on the trojan made a windows registry change that would open a website whenever someone boot there PC. They were earning Ad renewing from the website and earning lot due to high number of page hits.

  * **Rogue antivirus software** which claims to clean your PC via pop-ups then either steals personal info or prompt user to pay for an "upgrade" with more featured software.

  * **Ransomware** infects a target machine and then uses encryption technology to encrypt documents, spreadsheets, and other files stored on the system with a key known only to the malware creator. Pop-up message warning that the files will be permanently deleted unless a ransom is paid within a short period of time. *example* Cryptolocker, WannaCry, NotPetya etc.

  * **Botnet** is a Trojan horse made all the infected systems members of a botnet, a collection of computers (sometimes thousands or even millions!) across the internet under the control of an attacker known as the *botmaster*. Then infected PC become a part of denial-of-service attack against a website that he/she didn’t like for one reason or another.

### Worms

  * They contain the same destructive potential as other malicious code objects with an added twist—they propagate themselves without requiring any human intervention.

  * *Code Red Worm* unpatched versions of Microsoft’s Internet Information Server (IIS)

  * *Stuxnet* exloted undocumented vulnerabilities and shared infected USB drives.

### Spyware and Adware

  * *Spyware* monitors your actions and transmits important details to a remote system that spies on your activity. For example, spyware might wait for you to log into a banking website and then transmit your username and password to the creator of the spyware. Alternatively, it might wait for you to enter your credit card number on an e-commerce site and transmit it to a fraudster to resell on the black market.

  * *Adware*, while quite similar to spyware in form, has a different purpose. It uses a variety of techniques to display advertisements on infected computers. The simplest forms of adware display pop-up ads on your screen while you surf the web. More nefarious versions may monitor your shopping behavior and redirect you to competitor websites.

### Zero-Day Attacks

  * Many forms of malicious code take advantage of zero-day vulnerabilities, security flaws discovered by hackers that have not been thoroughly addressed by the security community. There are two main reasons systems are affected by these vulnerabilities:

    * The necessary delay between the discovery of a new type of malicious code and the issuance of patches and antivirus updates. This is known as the *window of vulnerability*.

    * Slowness in applying updates on the part of system administrators
  
  * *Safeguard* - defense-in-depth approach to cybersecurity that incorporates a varied set of overlapping security controls.

### Password Attacks

Three methods attackers use to learn the passwords of legitimate users and access a system: password-guessing attacks, dictionary attacks, and social-engineering attacks:

**Password Guessing**

Use of `Most Common Passwords`, SplashData produces list of most common password every year. 

**Dictionary Attacks**

`John the Ripper` is a common tool used by attackers, where a list of common password called dictionary which is then passed through a hash/encryption options which matching the destination  (/etc/shadow file) alog. Then attacker match the output with the shadow files to guess the password.

Hashing `Rainbow table` is another variant of dictionary attacks.

**Social Engineering Attacks**

`Fraud Calls` to extract personal information which can be useful to guess user passwords. `Phishing emails`are another popular mechanisms. Common variant include:

  * **Spear phishing** attacks are specifically targeted at an individual based upon research conducted by the attacker. They may include personal information designed to make the message appear more authentic.
  * **Whaling** attacks are a subset of spear phishing attacks sent to high-value targets, such as senior executives.
  * **Vishing** attacks use phishing techniques over voice communications, such as the telephone.

Another mechanism is `Dumpster diving`

**Countermeasure**

The cornerstone of any security program is education, `periodic training`, use of password storage service like LastPass.

### Application Security

Below are some of the specific techniques attackers use to exploit vulnerabilities left behind by sloppy coding practices:

#### Buffer Overflows

Buffer overflow vulnerabilities exist when a developer does not properly validate user input to ensure that it is of an appropriate size. Input that is too large can “overflow” a data structure to affect other data stored in the computer’s memory.

Programmer should take steps to ensure that each of the following conditions is met:

  * The user can’t enter a value longer than the size of any buffer that will hold it (for example, a 10-letter word into a 5-letter string variable).
  * The user can’t enter an invalid value for the variable types that will hold it (for example, a letter into a numeric variable).
  * The user can’t enter a value that will cause the program to operate outside its specified parameters (for example, answer a “yes” or “no” question with “maybe”).

#### Time of check to time to use (TOCTTOU or TOC/TOU)

It is timing vulnerability that occurs when a program checks access permissions too far in advance of a resource request. *Example* If the system administrator revokes a particular permission, that restriction would not be applied to the user until the next time they log on. 

#### Back Doors

Back doors are undocumented command sequences that allow individuals with knowledge of the back door to bypass normal access restrictions. They are often used during the development and debugging process to speed up the workflow and avoid forcing developers to continuously authenticate to the system.

#### Escalation of privilege and Rootkits

Once attackers gain a foothold on a system, they often quickly move on to a second objective—expanding their access from the normal user account they may have compromised to more comprehensive, administrative access. They do this by engaging in escalation-of-privilege attacks. One of the most common ways that attackers wage escalation-of-privilege attacks is through the use of *rootkits*. Rootkits are freely available on the internet and exploit known vulnerabilities in various operating systems.  

**Safeguard:** Administrators must keep themselves informed about new 
security patches released for operating systems used in their environment and apply these corrective measures consistently. 

### Web Application Security

We will cover common web application attacks

#### Cross-Site Scripting

Cross-site scripting (XSS) attacks occur when web applications contain some type of reflected input. For example, consider a simple web application that contains a single text box asking a user to enter their name. When the user clicks Submit, the web application loads a new page that says, *“Hello, name.”*

Under normal circumstances, this web application functions as designed. However, a malicious individual could take advantage of this web application to trick an unsuspecting third party. As you may know, you can embed scripts in web pages by using the Hypertext Markup Language (HTML) tags `<SCRIPT> and </SCRIPT>`. Suppose that, instead of entering Mike in the Name field, you enter the following text:

```
Mike<SCRIPT>alert('hello')</SCRIPT>

```
**SafeGuard:** When you create web applications that allow any type of user input, you must be sure to perform *input validation*. The best solution is to determine the type of input that you will allow and then validate the input to ensure that it matches that pattern.

[Ways evade cross-site scripting filters (OWASP)](https://www.owasp.org/index.php/XSS_Filter_Evasion_Cheat_Sheet)

#### Cross-Site Request Forgery

Cross-site request forgery attacks, abbreviated as XSRF or CSRF attacks, are similar to cross-site scripting attacks but exploit a different trust relationship. XSS attacks exploit the trust that a user has in a website to execute code on the user’s computer. XSRF attacks exploit the trust that remote sites have in a user’s system to execute commands on the user’s behalf.

XSRF attacks work by making the reasonable assumption that users are often logged into many different websites at the same time. Attackers then embed code in one website that sends a command to a second website. When the user clicks the link on the first site, he or she is unknowingly sending a command to the second site. If the user happens to be logged into that second site, the command may succeed.

**SafeGuard:** One way to do this is to create web applications that use secure tokens that the attacker would not know to embed in the links. Another safeguard is for sites to check the referring URL in requests received from end users and only accept requests that originated from their own site.

#### SQL Injection

SQL (Structured Query Language) injection attacks use unexpected input to a web application. However, instead of using this input to attempt to fool a user, SQL injection attacks use it to gain unauthorized access to an underlying database. 

SQL injection attacks allow a malicious individual to directly perform SQL transactions against the underlying database.

**SafeGuard:**

  * **Use Prepared Statements** Developers of web applications should leverage prepared statements to limit the application’s ability to execute arbitrary code. Prepared statements, including parameterized queries and stored procedures, store the SQL statement on the database server, where it may be modified only by database administrators and developers with appropriate access.

  * **Perform Input Validation**

  * **Limit Account Privileges** The database account used by the web server should have the smallest set of privileges possible. If the web application needs only to retrieve data, it should have that ability only. In the example, the DELETE command would fail if the account had SELECT privileges only.

### Reconnaissance Attacks

Performing reconnaissance can allow an attacker to find weak points to target directly with their attack code. We will look into three of those automated techniques — IP probes, port scans, and vulnerability scans

#### IP Probes

IP probes (also called IP sweeps or ping sweeps) are often the first type of network reconnaissance carried out against a targeted network. With this technique, automated tools simply attempt to ping each address in a range. Systems that respond to the ping request are logged for further analysis. Addresses that do not produce a response are assumed to be unused and are ignored. *Example* NMAP

**SafeGuard:** Disable ping functionality, if that not possible at least for users external to a network.

#### Port Scans

Attackers use port scan software to probe all the active systems on a network and determine what public services are running on each machine. For example, if the attacker wants to target a web server, they might run a port scan to locate any systems with a service running on port 80, the default port for Hypertext Transfer Protocol (HTTP) services

**SafeGuard:** Administrators should use this information to disable unnecessary services on systems under their control. 

#### Vulnerability Scan

Once the attacker determines a specific system to target, they need to discover a specific vulnerability in that system that can be exploited to gain the desired access permissions. Some of the more popular tools for this purpose include Nessus, OpenVAS, Qualys, Core Impact, and Nexpose

### Masquerading Attacks

One of the easiest ways to gain access to resources you’re not otherwise entitled to use is to impersonate someone who does have the appropriate access permissions. Two common masquerading attacks—IP spoofing and session hijacking

#### IP spoofing

In an IP spoofing attack, the malicious individual simply reconfigures their system so that it has the IP address of a trusted system and then attempts to gain access to other external resources.

**SafeGuard:** Rules on the perimeter:

  * Packets with internal source IP addresses don’t enter the network from the outside.
  * Packets with external source IP addresses don’t exit the network from the inside.
  * Packets with private IP addresses don’t pass through the router in either direction (unless specifically allowed as part of an intranet configuration).

#### Session hijacking 

Session hijacking attacks occur when a malicious individual intercepts part of the communication between an authorized user and a resource and then uses a hijacking technique to take over the session and assume the identity of the authorized user. 

The following list includes some common techniques:

  * Capturing details of the authentication between a client and server and using those details to assume the client’s identity
  * Tricking the client into thinking the attacker’s system is the server, acting as the middleman as the client sets up a legitimate connection with the server, and then disconnecting the client
  * Accessing a web application using the cookie data of a user who did not properly close the connection