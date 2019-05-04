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