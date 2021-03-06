# Table of Content

   * [Managing Incident Response](#managing-incident-response)
        * [Defining an Incident](#defining-an-incident)
        * [Incident response steps](#incident-response-steps)
           * [Detection](#detection)
           * [Response](#response)
           * [Mitigation](#mitigation)
           * [Reporting](#reporting)
           * [Recovery](#recovery)
           * [Remediation](#remediation)
           * [Lesson Learned](#lesson-learned)
   * [Implementing Detective and Preventive Measures](#implementing-detective-and-preventive-measures)
        * [Basic Preventive Measures](#basic-preventive-measures)         
        * [Understanding Attacks](#understanding-attacks)
           * [Botnets](#botnets)
           * [Denial-of-Service Attacks](#denial-of-service-attacks)
           * [SYN Flood Attack](#syn-flood-attack)
           * [TCP RESET Attack](#tcp-reset-attack)
           * [Smurf and Fraggle Attacks](#smurf-and-fraggle-attacks)
           * [Ping Flood](#ping-flood)
           * [Ping of Death](#ping-of-death)
           * [Teardrop](#teardrop)
           * [Land Attacks](#land-attacks)
           * [Zero-Day Exploit](#zero-day-exploit)
           * [Malicious Code](#malicious-code)
           * [Man-in-the-Middle Attacks](#man-in-the-middle-attacks)
           * [Sabotage](#sabotage)
           * [Espionage](#espionage)
        * [Intrusion Detection and Prevention Systems](#intrusion-detection-and-prevention-systems)
           * [Knowledge- and Behavior-Based Detection](#knowledge--and-behavior-based-detection)
           * [SIEM Systems](#siem-systems)
           * [IDS Response](#ids-response)
           * [Host- and Network-Based IDSs](#host--and-network-based-idss)
           * [Intrusion Prevention Systems](#intrusion-prevention-systems)
        * [Specific Preventive Measures](#specific-preventive-measures)
           * [Honeypots/Honeynets](#honeypotshoneynets)
           * [Understanding Pseudo Flaws](#understanding-pseudo-flaws)
           * [Understanding Padded Cells](#understanding-padded-cells)
           * [Warning Banners](#warning-banners)
           * [Anti-malware](#anti-malware)
           * [Whitelisting and Blacklisting](#whitelisting-and-blacklisting)
           * [Firewalls](#firewalls)
           * [Sandboxing](#sandboxing)
           * [Third-Party Security Services](#third-party-security-services)
           * [Penetration Testing](#penetration-testing)
   * [Logging, Monitoring, and Auditing](#logging-monitoring-and-auditing)
        * [Logging and Monitoring](#logging-and-monitoring)
           * [Logging Techniques](#logging-techniques)
           * [Common Log Types](#common-log-types)
           * [Protecting Log Data](#protecting-log-data)
           * [The Role of Monitoring](#the-role-of-monitoring)
        * [Egress monitoring](#egress-monitoring)
           * [Data Loss Prevention](#data-loss-prevention)
           * [Steganography](#steganography)
           * [Watermarking](#watermarking)
        * [Auditing to Assess Effectiveness](#auditing-to-assess-effectiveness)
           * [Inspection Audits](#inspection-audits)
           * [Access Review Audits](#access-review-audits)
           * [User Entitlement Audits](#user-entitlement-audits)
           * [Audits of Privileged Groups](#audits-of-privileged-groups)
           * [Dual Administrator Accounts](#dual-administrator-accounts)
        * [Security Audits and Reviews](#security-audits-and-reviews)
        * [Reporting Audit Results](#reporting-audit-results)
           * [Protecting Audit Results](#protecting-audit-results)
           * [Distributing Audit Reports](#distributing-audit-reports)
           * [Using External Auditors](#using-external-auditors)

## Managing Incident Response

Regardless of best efforts incident do occur. The primary goal of incident response is to minimize the impact on the organization.

### Defining an Incident

A computer security incident (sometimes called just security incident) commonly refers to an incident that is the result of an attack, or the result of malicious or intentional actions on the part of users. For example, request for comments (RFC) 2350, “Expectations for Computer Security Incident Response,” defines both a security incident and a computer security incident as “**any adverse event which compromises some aspect of computer or network security.**” National Institute of Standards and Technology (NIST) special publication (SP) 800-61 “Computer Security Incident Handling Guide” defines a computer security incident as “**a violation or imminent threat of violation of computer security policies, acceptable use policies, or standard security practices.**” [NIST documents, including SP 800-61, can be accessed from the NIST publications page](https://csrc.nist.gov/Publications).

Within the CISSP Security Operations domain, the “Conduct incident management” objective is clearly referring to computer security incidents.

An organization normally classify security incidents as:
* Any attempted network intrusion
* Any attempted denial-of-service attack
* Any detection of malicious software
* Any unauthorized access of data
* Any violation of security policies

### Incident response steps

As per CISSP objective below are steps involved:

![alt text](incidentresponsesteps.jpg)

Note: Incident response does not include a counterattack against the attacker, as most of the time its illegal and plus attacker would be spoofing identity behind a innocent user.

#### Detection

Common technique to detect potential threats are:

* Intrusion detection and prevention systems - Alert admins
* Anti-malware software
* Many automated tools regularly scan audit logs looking for predefined events, such as the use of special privileges
* End user report an event

First responder of the threat is like first responder for medical emergency. They need to have skills to understand difference between major and minor event and should know what should be the action plan for each type of incidents.

#### Response

  * After detecting and verifying an incident, the next step is response. The response varies depending on the severity of the incident. Many organizations have a designated incident response team—sometimes called a computer incident response team (CIRT), or computer security incident response team (CSIRT)

  *  The quicker an organization can respond to an incident, the better chance they have at limiting the damage.

#### Mitigation

  * Mitigation steps attempt to contain an incident. One of the primary goals of an effective incident response is to limit the effect or scope of an incident. **For example**, if an infected computer is sending data out its network interface card (NIC), a technician can disable the NIC or disconnect the cable to the NIC.

  * Sometimes isolating the problematic device is better and solve the problem later. 

#### Reporting
  
  * Reporting refers to reporting an incident within the organization and to organizations and individuals outside the organization. Although there’s no need to report a minor malware infection to a company’s chief executive officer (CEO), upper-level management does need to know about serious security breaches.

  * Sometimes organization have legal requirement to report the incident. 

  * In response to serious security incidents, the organization should consider reporting the incident to official agencies. In US that means notify FBI etc, in Europe its International Criminal Police Organization (INTERPOL)
  
  * Training should teach individuals how to recognize incidents, what to do in the initial response, and how to report an incident.

#### Recovery 

  * After investigators collect all appropriate evidence from a system, the next step is to recover the system, or return it to a fully functioning state. This can be very simple for minor incidents and may only require a reboot. However, a major incident may require completely rebuilding a system. Rebuilding the system includes restoring all data from the most recent backup.

  * Make sure that the secure state of the system is as it was before the incident. If proper change management system is allowed then it would be documented.

#### Remediation

  * In the remediation stage, personnel look at the incident and attempt to identify what allowed it to occur, and then implement methods to prevent it from happening again. This includes performing a root cause analysis.

  * Suggestion could be vulnerability patches and/or infrastructure changes.

#### Lesson Learned

  * During the lessons learned stage, personnel examine the incident and the response to see if there are any lessons to be learned. The incident response team will be involved in this stage, but other employees who are knowledgeable about the incident will also participate.

  * The output of this stage can be fed back to the detection stage of incident management. 

## Implementing Detective and Preventive Measures

This section covers several preventive security controls that can prevent many attacks and describes many common well-known attacks.

### Basic Preventive Measures 

There is no one single step you can take to avoid all attacks but here is few key measures:

  * Keep systems and applications up-to-date.
  * Remove or disable unneeded services and protocols
  * Use intrusion detection and prevention systems.
  * Use up-to-date anti-malware software
  * Use firewalls
  * Implement configuration and system management processes

### Understanding Attacks

#### Botnets

  * Computer in the botnet are called **bot** and sometime **zombies**.
  * Many bot in a network create a **botnet**
  * Botnet **herder** is a criminal that manage botnet via command and control server (C&C) server.
  * Bots can contact C&C server for instruction periodically or upon certain events. 
  * Computers are typically joined to a botnet after being infected with some type of malicious code or malicious software.
  * **SafeGuard:** `Defense-in-depth` `anti-malware` `Keep system up-to-date` `Educating users` `For Browser: do not disable there build-in security`
  * traditionally computer and laptops were inflect to join them to botnet, but with recently IoT devices have become a common target of these attacks.
  * *Example* Mirai malware in 2016 to launch a distributed denial-of-service (DDoS) attack on Domain Name System (DNS) servers hosted by Dyn. 

#### Denial-of-Service Attacks

  * Denial-of-service (DoS) attacks are attacks that prevent a system from processing or responding to legitimate traffic or requests for resources and objects.
  * Another form of DoS attack is a ***distributed denial-of-service (DDoS)*** attack. A DDoS attack occurs when multiple systems attack a single system at the same time.
  * Attackers commonly use botnets to launch DDoS attacks.
  * ***Distributed reflective denial-of-service (DRDoS)*** attack is a variant of a DoS. It uses a reflected approach to an attack. In other words, it doesn’t attack the victim directly, but instead manipulates traffic or a network service so that the attacks are reflected back to the victim from other sources. Domain Name System (DNS) poisoning attacks and smurf attacks.

#### SYN Flood Attack

  * The SYN flood attack is a common DoS attack. It disrupts the standard three-way handshake used by Transmission Control Protocol (TCP) to initiate communication sessions. In a SYN flood attack, the attackers send multiple SYN packets but never complete the connection with an ACK.

  *  It’s common for the attacker to spoof the source address, with each SYN packet having a different source address.

  * **SafeGuard:** Using *SYN cookies* is one method of blocking this attack. These small records consume very few system resources. When the system receives an ACK, it checks the SYN cookies and establishes a session. *Firewalls* often include mechanisms to check for SYN attacks, as do *intrusion detection and intrusion prevention systems*.Another method of blocking this attack is to *reduce the amount of time a server will wait for an ACK*. It is typically three minutes by default, but in normal operation it rarely takes a legitimate system three minutes to send the ACK packet. By reducing the time, half-open sessions are flushed from the system’s memory quicker. 

#### TCP RESET Attack
  
  * Sessions are normally terminated with either the FIN (finish) or the RST (reset) packet. Attackers can spoof the source IP address in a RST packet and disconnect active sessions. The two systems then need to reestablish the session. 

#### Smurf and Fraggle Attacks
  
  * In a *smurf attack* the attacker sends the echo request out as a broadcast to all systems on the network and spoofs the source IP address. All these systems respond with echo replies to the spoofed IP address, flooding the victim with traffic.

  * Smurf attacks take advantage of an *amplifying network* (also called a smurf amplifier) by sending a directed broadcast through a router. **SafeGuard** for that was introduce via RFC 2644, released in 1999, that change the standard that router should not forward directed broadcast through routers. Additionally, it is common to disable ICMP on firewalls, routers, and even many servers to prevent any type of attacks using ICMP. When standard security practices are used, smurf attacks are rarely a problem today.

  * *Fraggle attacks* are similar to smurf attacks. However, instead of using ICMP, a fraggle attack uses UDP packets over *UDP ports 7 and 19*. The fraggle attack will broadcast a UDP packet using the spoofed IP address of the victim. All systems on the network will then send traffic to the victim, just as with a smurf attack.

#### Ping Flood

  * A ping flood attack floods a victim with ping requests. This can be very effective when launched by zombies within a botnet as a DDoS attack. The victim will not have time to respond to legitimate requests. **SafeGuard** blocking ICMP traffic and/or use an IDS to detect the attack and implement controls to block ICMP.

#### Ping of Death

  * A *ping-of-death* attack employs an oversized ping packet. Ping packets are normally 32 or 64 bytes, though different operating systems can use other sizes. The ping-of-death attack changed the size of ping packets to *over 64 KB*, which was bigger than many systems could handle. When a system received a ping packet larger than 64 KB, it resulted in a problem. In some cases the system crashed. In other cases, it resulted in a buffer overflow error. A ping-of-death attack is rarely successful today because patches and updates remove the vulnerability.

#### Teardrop

  * In a *teardrop attack*, an attacker fragments traffic in such a way that a system is unable to put data packets back together. A teardrop attack mangles these packets in such a way that the system cannot put them back together. Older systems couldn’t handle this situation and crashed, but patches resolved the problem.

  * Not an active threat these days as its already been patched. But IDS can still be used to inspect malformed packets. 

#### Land Attacks

  * A land attack occurs when the attacker sends spoofed SYN packets to a victim using the victim’s IP address as both the source and destination IP address. This tricks the system into constantly replying to itself and can cause it to freeze, crash, or reboot.

#### Zero-Day Exploit

  * A zero-day exploit refers to an attack on a system exploiting a vulnerability that is unknown to others. Security professionals use the term in different contexts and it has some minor differences based on the context. Here are some examples:

    * Attacker First Discovers a Vulnerability
    * Vendor Learns of Vulnerability
    * Vendor Releases Patch (time difference between vendor releasing the path and admin applying the patch)

#### Malicious Code

  * Malicious code is any script or program that performs an unwanted, unauthorized, or unknown activity on a computer system. Malicious code can take many forms, including viruses, worms, Trojan horses, documents with destructive macros, and logic bombs. It is often called malware, short for malicious software, and less commonly malcode, short for malicious code. 

  * A *drive-by download* (one of the most popular method to distribute malware) is code downloaded and installed on a user’s system without the user’s knowledge. Attackers modify the code on a web page and when the user visits, the code downloads and installs malware on the user’s system without the user’s knowledge or consent.

  * Another popular method of installing malware uses a pay-per-install approach. Criminals pay website operators to host their malware, which is often a fake anti-malware program (also called *rogueware*). 

  * Although the majority of malware arrives from the internet, some is transmitted to systems via Universal Serial Bus (USB) flash drives.

#### Man-in-the-Middle Attacks

  * A man-in-the-middle (MITM) attack occurs when a malicious user can gain a position logically between the two endpoints of an ongoing communication. There are two types of man-in-the-middle attacks:

    * Copying or sniffing the traffic between two parties
    * Attackers positioning themselves in the line of communication where they act as a store-and-forward or proxy mechanism.

  * **SafeGuard:** `keeping systems up-to-date`  `virtual private networks (VPNs) to avoid these attacks`

#### Sabotage

  * Employee sabotage is a criminal act of destruction or disruption committed against an organization by an employee. Employee sabotage occurs most often when employees suspect they will be terminated without just cause or if employees retain access after being terminated.

  * **SafeGuard:** This is another important reason employee terminations should be handled swiftly and account access should be disabled as soon as possible after the termination. Other safeguards against employee sabotage are intensive auditing, monitoring for abnormal or unauthorized activity, keeping lines of communication open between employees and managers, and properly compensating and recognizing employees for their contributions.

#### Espionage

  * Espionage is the malicious act of gathering proprietary, secret, private, sensitive, or confidential information about an organization.

  * Attackers often commit espionage with the intent of disclosing or selling the information to a competitor or other interested organization (such as a foreign government). 

  * Many reported cases of espionage are traced back to advanced persistent threats (APTs) sponsored by nation-states. 

### Intrusion Detection and Prevention Systems

  * Intrusion detection systems (IDSs) and intrusion prevention systems (IPSs) are two methods organizations typically implement to detect and prevent attacks.

  * *Intrusion detection* is a specific form of monitoring that monitors recorded information and real-time events to detect abnormal activity indicating a potential incident or intrusion. An intrusion detection system (IDS) automates the inspection of logs and real-time system events to detect intrusion attempts and system failures. Because an IPS includes detection capabilities, you’ll often see them referred to as intrusion detection and prevention systems (IDPSs).

  * An *intrusion prevention system (IPS)* includes all the capabilities of an IDS but can also take additional steps to stop or prevent intrusions. If desired, administrators can disable these extra features of an IPS, essentially causing it to function as an IDS.

  * **Standard/Guideline** NIST SP 800-94, “Guide to Intrusion Detection and Prevention Systems”

#### Knowledge- and Behavior-Based Detection


  * *Knowledge-based detection* uses signatures similar to the signature definitions used by anti-malware software. *Behavior-based detection* doesn’t use signatures but instead compares activity against a baseline of normal performance to detect abnormal behavior. Many IDSs use a combination of both methods.

  * The primary ***drawback*** for a *knowledge-based* IDS is that it is effective only against known attack methods. New attacks, or slightly modified versions of known attacks, often go unrecognized by the IDS.

  * Anomaly analysis adds to an IDS’s capabilities by allowing it to recognize and react to sudden increases in traffic volume or activity, multiple failed login attempts, logons or program activity outside normal working hours, or sudden increases in error or failure messages. All of these could indicate an attack that a knowledge-based detection system may not recognize.

  * A behavior-based IDS can be labeled an expert system or a pseudo–artificial intelligence system because it can learn and make assumptions about events.

  * The primary ***drawback*** for a *behavior-based* IDS is that it often raises a high number of false alarms, also called false alerts or false positives.

#### SIEM Systems

  * Many IDSs and IPSs send collected data to a security information and event management (SIEM) system. A SIEM system also collects data from many other sources within the network. It provides real-time monitoring of traffic and analysis and notification of potential attacks. Additionally, it provides long-term storage of data, allowing security professionals to analyze the data.

#### IDS Response

  * When the IDS detects an event, it triggers an alarm or alert. It can then respond using a passive or active method. A *passive response* logs the event and sends a notification. An *active response* changes the environment to block the activity in addition to logging and sending a notification.

#### Host- and Network-Based IDSs

  * IDS types are commonly classified as host based and network based. A *host-based IDS (HIDS)* monitors a single computer or host. A *network-based IDS (NIDS)* monitors a network by observing network traffic patterns.

  * Another type of IDS which is uncommon is the use of Application-based IDS, which is specific type of network based IDS to monitor traffic between two servers. *Example:* traffic between a web server and database.

  * ***Host-Based IDS*** 

    * An HIDS monitors activity on a single computer, including process calls and information recorded in system, application, security, and host-based firewall logs. Its like an anti-malware and some HIDS solution have anti-malware anti-malware capabilities. 

    * *Some Disadvantages* `Admin overhead to manage` `resource intensive` `easier to intrudure to detect and disable`

  * ***Network-Based IDS***

     * A NIDS monitors and evaluates network activity to detect attacks or event anomalies. A single NIDS can monitor a large network by using remote sensors to collect data at key network locations that send data to a central management console and/or a SIEM. These sensors can monitor traffic at routers, firewalls, network switches that support port mirroring, and other types of network taps.

     * TLS traffic (which is almost 75% of Internet traffic) can be a an issue for NIDS, as they cannot inspect the encrypted communication. To tackle this problem some admin deploy *SSL Decryptors*, its like a SSL proxy in the path. But APTs at times encrypt the traffic on the client before sending it to the server which NIDS cannot decrypt.

#### Intrusion Prevention Systems

  * An intrusion prevention system (IPS) is a special type of active IDS that attempts to detect and block attacks before they reach target systems. It’s sometimes referred to as an intrusion detection and prevention system (IDPS).
  
  * IPS is placed in-line with the traffic as compared to IDS which is not in-line and receives copy of traffic for analysis.

### Specific Preventive Measures

Additional security controls to protect networks

#### Honeypots/Honeynets

  * *Honeypots* are individual computers created as a trap for intruders. A *honeynet* is two or more networked honeypots used together to simulate a network. They look and act like legitimate systems, but they do not host data of any real value for an attacker.

  * Longer intruder is busy attacking honeypot, better information would be available to administrator and/or IDS system to detect the unique pattern in attackers traffic. Many security researches thinks that honeypots are effective countermeasure against zero-day attacks.

  * Mostly hosted on virtual machines (VMs)

  * The use of honeypots raises the issue of *enticement versus entrapment*, enticement is legal and enticed attackers make their own decisions to perform illegal or unauthorized actions. Whereas entrapment is when you trick or encourage someone into performing an illegal or unauthorized action. Laws vary in different countries so it’s important to understand local laws related to enticement and entrapment.

#### Understanding Pseudo Flaws

  * Pseudo flaws are false vulnerabilities or apparent loopholes intentionally implanted in a system in an attempt to tempt attackers. They are often used on honeypot systems to emulate well-known operating system vulnerabilities
  
  * Sophisticated pseudo flaw mechanisms actually simulate the penetration and convince the attacker that they have gained additional access privileges to a system. 

#### Understanding Padded Cells

  * A padded cell system is similar to a honeypot, but it performs intrusion isolation using a different approach. When an IDPS detects an intruder, that intruder is automatically transferred to a padded cell. The padded cell has the look and feel of an actual network, but the attacker is unable to perform any malicious activities or access any confidential data from within the padded cell.

#### Warning Banners
  
  * Warning banners inform users and intruders about basic security policy guidelines. They typically mention that online activities are audited and monitored, and often provide reminders of restricted activities. In most situations, wording in banners is important from a legal standpoint because these banners can legally bind users to a permissible set of actions, behaviors, and processes.

  * Warning banners inform both authorized and unauthorized users. These banners typically remind authorized users of the content in acceptable-use agreements.

#### Anti-malware

  * The most important protection against malicious code is the use of anti-malware software with up-to-date signature files and heuristic capabilities. Attackers regularly release new malware and often modify existing malware to prevent detection by anti-malware software. 

  * Vendors used to provider signature updates weekly, now-a-days the updates are done almost daily or even multiple times a day is need be.

  * Many organizations use a multipronged approach to block malware and detect any malware that gets in. Firewalls with content-filtering capabilities (or specialized content-filter appliances) are commonly used at the boundary between the internet and the internal network to filter out any type of malicious code. Specialized anti-malware software is installed on email servers to detect and filter any type of malware passed via email. Additionally, anti-malware software is installed on each system to detect and block malware. Organizations often use a central server to deploy anti-malware software, download updated definitions, and push these definitions out to the clients.
  
  * Following the principle of least privilege also helps, cause even if malware compromise the system, it rights would be restricted to user's permission.

  * Educating users about the dangers of malicious code, how attackers try to trick users into installing it, and what they can do to limit their risks is another protection method. 

#### Whitelisting and Blacklisting

  * Whitelisting identifies a list of applications authorized to run on a system, and blacklisting identifies a list of applications that are not authorized to run on a system. They can also help prevent malware infections. 

  * Some whitelists identify applications using a hashing algorithm to create a hash. However, if an application is infected with a virus, the virus effectively changes the hash, so this type of whitelist blocks infected applications from running too.

#### Firewalls

  * Firewalls provide protection to a network by filtering traffic.

  * *Basic firewalls* filter traffic based on IP addresses, ports, and some protocols using protocol numbers. 

  * *Second-generation firewalls* add additional filtering capabilities like application-level gateway filtering.

  * *Third-generation firewalls*  also called stateful inspection firewalls and dynamic packet filtering firewalls filter traffic based on its state within a stream of traffic.

  * A *next-generation firewall* functions as a unified threat management (UTM) device and combines several filtering capabilities. It includes traditional functions of a firewall such as packet filtering and stateful inspection. However, it is able to perform packet inspection techniques, allowing it to identify and block malicious traffic. It can filter malware using definition files and/or whitelists and blacklists. It also includes intrusion detection and/or intrusion prevention capabilities.

#### Sandboxing

  * Sandboxing provides a security boundary for applications and prevents the application from interacting with other applications. Anti-malware applications use sandboxing techniques to test unknown applications. If the application displays suspicious characteristics, the sandboxing technique prevents the application from infecting other applications or the operating system.

#### Third-Party Security Services

  * Some organizations outsource security services to a third party, which is an individual or organization outside the organization. This can include many different types of services such as auditing and penetration testing. *Example*  Payment Card Industry Data Security Standard (PCI DSS) for organizations processing transactions with major credit cards. And PCI DSS requires organizations to ensure that service providers also comply with PCI DSS requirements.

#### Penetration Testing

  * Penetration testing is another preventive measure an organization can use to counter attacks. A penetration test (often shortened to pentest) mimics an actual attack in an attempt to identify what techniques attackers can use to circumvent security in an application, system, network, or organization. It may include vulnerability scans, port scans, packet sniffing, DoS attacks, and social-engineering techniques.

  * **Standard/Guideline** *NIST SP 800-115, “Technical Guide to Information Security Testing and Assessment,”* includes a significant amount of information about testing, including penetration testing.

  * Here are some of the goals of a penetration test:

    * Determine how well a system can tolerate an attack
    * Identify employees’ ability to detect and respond to attacks in real time
    * Identify additional controls that can be implemented to reduce risk

**Risks of Penetration Testing**

  * A significant danger with penetration tests is that some methods can cause outages.

  * Whenever possible, testers perform penetration tests on a test system instead of a live production system.

**Obtaining Permission for Penetration Testing**
 
  * Penetration testing should only be performed after careful consideration and approval of senior management. Many security professionals insist on getting this approval in writing with the risks spelled out. Performing unapproved security testing could cause productivity losses and trigger emergency response teams.

**Penetration-Testing Techniques** 
 
  * ***Black-Box Testing by Zero-Knowledge Team*** `publicly available info`
  
  * ***White-Box Testing by Full-Knowledge Team*** `patches and upgrade installed` `config of relevant devices` `if application, they may have access to the code` Also called **crystal-box or clear-box testing**

  * ***Gray-Box Testing by Partial-Knowledge Team*** `given information on the network design and configuration details so that they can focus on attacks and vulnerabilities for specific targets`

  * Security professional in-charge of safeguarding the infra should not ideally be doing pentest, as they would have some bias or blind spots or gaps in their understanding, estimation, or capabilities with certain security subjects.

**Protect Reports** 

  * Penetration testers will provide a report documenting their results, and this report should be protected as sensitive information. The report will outline specific vulnerabilities and how these vulnerabilities can be exploited. It will often include recommendations on how to mitigate the vulnerabilities. If these results fall into the hands of attackers before the organization implements the recommendations, attackers can use details in the report to launch an attack.

**Ethical Hacking**

  * Ethical hacking is often used as another name for penetration testing. An ethical hacker is someone who understands network security and methods to breach security but does not use this knowledge for personal gain. Instead, an ethical hacker uses this knowledge to help organizations understand their vulnerabilities and take action to prevent malicious attacks. An ethical hacker will always stay within legal limits.

  * Ethical hackers will learn about and often use the same tools and techniques used by attackers. However, they do not use them to attack systems. Instead, they use them to test systems for vulnerabilities and only after an organization has granted them explicit permission to do so.

## Logging, Monitoring, and Auditing

### Logging and Monitoring

Logging and Monitoring helps an organization detect undesirable events that can negatively affect confidentiality, integrity, or availability of systems. It is also useful in reconstructing activity after an event has occurred to identify what happened and sometimes to prosecute those responsible for the activity.

#### Logging Techniques

  * Logging captures events, changes, messages, and other data that describe activities that occurred on a system. 

  * Logs will commonly record details such as:
    * what happened
    * when it happened 
    * where it happened
    * who did it
    * sometimes how it happened

#### Common Log Types
  
  * *Security Logs*: `record access to resources` `admins might enable this logging for proprietary data`
  
  * *System Logs*:  `record system start or stop` `records service start or stop`

  * *Application Logs*: `application dev can choose what to record`

  * *Firewall Logs*: `traffic permitted or denied by the firewall` `mostly its 5 tuple (IP addr etc) not the content of the packet`

  * *Proxy Logs*: `record user website access info` `how much time user spend`

  * *Change Logs*: `Change logs record change requests, approvals, and actual changes to a system as a part of an overall change management process` `Change logs are useful to track approved changes` 

#### Protecting Log Data

  * Personnel within the organization can use logs to re-create events leading up to and during an incident, but only if the logs haven’t been modified. If attackers can modify the logs, they can erase their activity, effectively nullifying the value of the data. The files may no longer include accurate information and may not be admissible as evidence to prosecute attackers. With this in mind, it’s important to protect log files against unauthorized access and unauthorized modification.

  * **Protection**

    * Store them in a SIEM
    * Limit access via permissions
    * Organizations often have strict policies mandating backups of log files. Additionally, these policies define retention times.

  * **Standard/Guidelines:** As per National Institute of Standards and Technology (NIST) publishes a significant amount of information on IT security, including Federal Information Processing Standards (FIPS) publications. The Minimum Security Requirements for Federal Information and Information Systems ([FIPS 200](https://csrc.nist.gov/csrc/media/publications/fips/200/final/documents/fips-200-final-march.pdf)) specifies the following as the minimum security requirements for audit data:

      *Create, protect, and retain information system audit records to the extent needed to enable the monitoring, analysis, investigation, and reporting of unlawful, unauthorized, or inappropriate information system activity.*

      *Ensure that the actions of individual information system users can be uniquely traced to those users so they can be held accountable for their actions.* 

#### The Role of Monitoring

Monitoring provides several benefits for an organization, including increasing accountability, helping with investigations, and basic troubleshooting.

**Audit Trails**

Audit trails are records created when information about events and occurrences is stored in one or more databases or log files. They provide a record of system activity and can reconstruct activity leading up to and during security events. Security professionals extract information about an incident from an audit trail to prove or disprove culpability, and much more. 

**Monitoring and Accountability**

Monitoring is a necessary function to ensure that subjects (such as users and employees) can be held accountable for their actions and activities. Users claim an identity (such as with a username) and prove their identity (by authenticating), and audit trails record their activity while they are logged in. Monitoring and reviewing the audit trail logs provides accountability for these users.

It promotes positive user behavior and compliance.

Legislation often requires specific monitoring and accountability practices. This includes laws such as the **Sarbanes–Oxley Act** of 2002, the Health Insurance Portability and Accountability Act (**HIPAA**), and European Union (**EU**) **privacy laws** that many organizations must abide by.

**Monitoring and Investigations**

Audit trails give investigators the ability to reconstruct events long after they have occurred. They can record access abuses, privilege violations, attempted intrusions, and many different types of attacks. After detecting a security violation, security professionals can reconstruct the conditions and system state leading up to the event, during the event, and after the event through a close examination of the audit trail.

Setup Network Time Protocol (NTP) for accurate timestamp in the logs. 

NIST NTP Authentication and service, [link](https://www.nist.gov/pml/time-and-frequency-division/time-services/nist-authenticated-ntp-service)

**Monitoring and Problem Identification**

Audit trails can record system failures, OS bugs, and software errors in addition to malicious attacks. Records contents of memory when an application or system crashes. 

**Monitoring Techniques**

*Monitoring* is the process of reviewing information logs looking for something specific. 

*Log analysis* is a detailed and systematic form of monitoring in which the logged information is analyzed for trends and patterns as well as abnormal, unauthorized, illegal, and policy-violating activities. Log analysis isn’t necessarily in response to an incident but instead a periodic task, which can detect potential issues. Due to massive log size, admin prefer this to be automated. 

**Security Information and Event Management**

`Security information and event management (SIEM)`
`Security event management (SEM)`
`Security information management (SIM)`

These tools provide real-time analysis of events occurring on systems throughout an organization. They include agents installed on remote systems that monitor for specific events known as alarm triggers. When the trigger occurs, the agents report the event back to the central monitoring software.

SIEMs uses advanced analytic tools to detect abnormalities and sends alerts to security administrators.

Some monitoring tools are also used for inventory and status purposes

Software monitoring watches for attempted or successful installations of unapproved software, use of unauthorized software, or unauthorized use of approved software

**Sampling**

Sampling is a form of data reduction that allows someone to glean valuable information by looking at only a small sample of data in an audit trail. There is always a risk that sampled data is not an accurate representation of the whole body of data, and statistical sampling can identify the margin of error.

**Clipping Levels**

Clipping is a form of nonstatistical sampling. It selects only events that exceed a clipping level, which is a predefined threshold for the event. The system ignores events until they reach this threshold.

As an example, failed logon attempts are common in any system as users can easily enter the wrong password once or twice. Instead of raising an alarm for every single failed logon attempt, a clipping level can be set to raise an alarm only if it detects five failed logon attempts within a 30-minute period. Many account lockout controls use a similar clipping level. They don’t lock the account after a single failed logon. Instead, they count the failed logons and lock the account only when the predefined threshold is reached.

In other words, the clipping level causes the system to ignore routine events and only raise an alert when it detects serious intrusion patterns.

**Other Monitoring Tools**

Other technique includes, closed-circuit television (CCTV), keystroke monitoring, traffic analysis monitoring, trend analysis monitoring, and monitoring to prevent data loss.

### Egress monitoring

Egress monitoring refers to monitoring outgoing traffic to prevent data exfiltration, which is the unauthorized transfer of data outside the organization. Some common methods used to prevent data exfiltration are using data loss prevention techniques, looking for steganography attempts, and using watermarking to detect unauthorized data going out.

Advanced attackers can encrypt data which bypasses these attempts. However, it’s also possible to include tools that monitor the amount of encrypted data sent out of the network.

#### Data Loss Prevention

  * These systems have the capability of scanning unencrypted data looking for keywords and data patterns. For example, imagine that an organization uses data classifications of Confidential, Proprietary, Private, and Sensitive. A DLP system can scan files for these words and detect them.

  * There are two primary types of DLP systems: network-based and endpoint-based.

    * Network-Based DLP - `Edge of the network`
    * Endpoint-Based DLP - `files stored on a system as well as files sent to external devices, such as printers`

  * **Drawback** A DLP system doesn’t have the ability to decrypt data. Major advance persistent threat (ATP) include Fancy Bear ([APT 28](https://en.wikipedia.org/wiki/Fancy_Bear)) and Cozy Bear ([APT 29](https://en.wikipedia.org/wiki/Cozy_Bear)).

#### Steganography

  * Steganography is the practice of embedding a message within a file. For example, individuals can modify bits within a picture file to embed a message. The change is imperceptible to someone looking at the picture, but if other people know to look for the message, they can extract it.

  * It is possible to detect steganography attempts if you have the original file and a file you suspect has a hidden message. If you use a hashing algorithm such as Secure Hash Algorithm 3 (SHA-3), you can create a hash of both files. If the hashes are the same, the file does not have a hidden message. However, if the hashes are different, it indicates the second file has been modified. Forensic analysis techniques might be able to retrieve the message.

#### Watermarking

  * Watermarking is the practice of embedding an image or pattern in paper that isn’t readily perceivable. It is often used with currency to thwart counterfeiting attempts. Similarly, organizations often use watermarking in documents.

  * From the perspective of egress monitoring, DLP systems can detect the watermark in unencrypted files. 

  * A digital watermark is a secretly embedded marker in a digital file. For example, some movie studios digitally mark copies of movies sent to different distributors.

### Auditing to Assess Effectiveness

*Auditing* is a methodical examination or review of an environment to ensure compliance with regulations and to detect abnormalities, unauthorized occurrences, or crimes. It verifies that the security mechanisms deployed in an environment are providing adequate security for the environment. The test process ensures that personnel are following the requirements dictated by the security policy or other regulations, and that no significant holes or weaknesses exist in deployed security solutions.

*Auditors* perform the auditing.

#### Inspection Audits

Two important audits within the context of access control are access review audits and user entitlement audits.

It’s important to clearly define and adhere to the frequency of audit reviews. Frequency is related to level of risk. Auditing is key element of *due care*. 

#### Access Review Audits

Many organizations perform periodic access reviews and audits to ensure that object access and account management practices support the security policy. These audits verify that users do not have excessive privileges and that accounts are managed appropriately. They ensure that secure processes and procedures are in place, that personnel are following them, and that these processes and procedures are working as expected.

The access review verifies that a policy exists and that personnel are following it. When terminated employees have continued access to the network after an exit interview, they can easily cause damage. For example, an administrator can create a separate administrator account and use it to access the network even if the administrator’s original account is disabled.

#### User Entitlement Audits

User entitlement refers to the privileges granted to users. Users need rights and permissions (privileges) to perform their job, but they only need a limited number of privileges. In the context of user entitlement, the principle of least privilege ensures that users have only the privileges they need to perform their job and no more.

#### Audits of Privileged Groups

Many organizations use groups as part of a Role Based Access Control model. It’s important to limit the membership of groups that have a high-level of privileges, such as administrator groups

#### Dual Administrator Accounts

Many organizations require administrators to maintain two accounts. They use one account for regular day-to-day use. A second account has additional privileges and they use it for administrative work. This reduces the risk associated with this privileged account.

### Security Audits and Reviews 

Security audits and reviews help ensure that an organization has implemented security controls properly. Access review audits (presented earlier in this chapter) assess the effectiveness of access controls. These reviews ensure that accounts are managed appropriately, don’t have excessive privileges, and are disabled or deleted when required. In the context of the Security Operations domain, security audits help ensure that management controls are in place. The following list includes some common items to check:


  * Patch Management
  * Vulnerability Management
  * Configuration Management
  * Change Management

### Reporting Audit Results 

The actual formats used by an organization to produce reports from audits vary. However, reports should address a few basic or central concepts:

  * The purpose of the audit
  * The scope of the audit
  * The results discovered or revealed by the audit

In addition to these basic concepts, audit reports often include many details specific to the environment, such as time, date, and a list of the audited systems. They can also include a wide range of content that focuses on

  * Problems, events, and conditions
  * Standards, criteria, and baselines
  * Causes, reasons, impact, and effect
  * Recommended solutions and safeguards

#### Protecting Audit Results

  * They should be assigned a classification label and only those people with sufficient privilege should have access to audit reports. This includes high-level executives and security personnel involved in the creation of the reports or responsible for the correction of items mentioned in the reports.

  * Auditors sometimes create a separate audit report (overview or summary of findings) with limited data for other personnel. This modified report provides only the details relevant to the target audience. 

#### Distributing Audit Reports

  * It’s common to file a signed confirmation of receipt. When an audit report contains information about serious security violations or performance issues, personnel escalate it to higher levels of management for review, notification, and assignment of a response to resolve the issues.

#### Using External Auditors

  * Many organizations choose to conduct independent audits by hiring external security auditors. Additionally, some laws and regulations require external audits. External audits provide a level of objectivity that an internal audit cannot provide, and they bring a fresh, outside perspective to internal policies, practices, and procedures.

  * An *interim report* is a written or verbal report given to the organization about any observed security weaknesses or policy/procedure mismatches that demand immediate attention. Auditors issue interim reports whenever a problem or issue is too important to wait until the final audit report.

  * `exit conference` findings and discuss resolution issues 

  * After the organization receives the final audit report, internal auditors review it and make recommendations to senior management based on the report. Senior management is responsible for selecting which recommendations to implement and for delegating implementation requirements to internal personnel.
