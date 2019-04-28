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