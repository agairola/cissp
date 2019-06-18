## Comparing Access Control Models

The method of authorizing subjects to access objects varies depending on the access control method used by the IT system.

### Comparing Permissions, Rights and Privileges  

**Permissions** In general, permissions refer to the access granted for an object and determine what you can do with it. If you have read permission for a file, you’ll be able to open it and read it. You can grant user permissions to create, read, edit, or delete a file on a file server.

**Rights** A right primarily refers to the ability to take an action on an object. For example, a user might have the right to modify the system time on a computer or the right to restore backed-up data.

**Privileges** Privileges are the combination of rights and permissions. For example, an administrator for a computer will have full privileges, granting the administrator full rights and permissions on the computer. The administrator will be able to perform any actions and access any data on the computer.

### Understanding Authorization Mechanisms

Access control models use many different types of authorization mechanisms, or methods, to control who can access specific objects.

**Implicit Deny** `access to an object is denied unless access has been explicitly granted to a subject`

**Access Control Matrix** `table that includes subjects, objects, and assigned privileges` `subject has the appropriate privileges to perform the action`

**Capability Tables** `identify privileges assigned to subjects` 

> ACLs are object focused and identify access granted to subjects for any specific object. Capability tables are subject focused and identify the objects that subjects can access.

**Constrained Interface** `Applications use constrained interfaces or restricted interfaces to restrict what users can do or see based on their privileges`

**Content-Dependent Control** `restrict access to data based on the content within an object` `A database view is a content-dependent control (A view retrieves specific columns from one or more tables, creating a virtual table)`

**Context-Dependent Control** `require specific activity before granting users access`

*Example:* of downloading a digital produce. Users add products to a shopping cart and begin the checkout process. The first page in the checkout flow shows the products in the shopping cart, the next page collects credit card data, and the last page confirms the purchase and provides instructions for downloading the digital products.

`It’s also possible to use date and time controls as context-dependent controls`

**Need to Know** `subjects are granted access only to what they need to know for their work tasks and job functions` *Example*, even subject with required clearance may be denied access if access is not required to do a job function.

**Least Privilege** `subjects are granted only the privileges they need to perform their work tasks and job functions`

**Separation of Duties and Responsibilities** `sensitive functions are split into tasks performed by two or more employees` `prevent fraud and errors by creating a system of checks and balances`

### Defining Requirements with Security Policy

Security policies help personnel within the organization understand what security requirements are important. Senior leadership approves the security policy. Security policy usually does not go into details about how to fulfill the security needs or how to implement the policy.

### Implementing Defense in Depth

![alt text](defenceindepth.jpg)

The concept of defense in depth highlights several important points:

* An organization’s *security policy*, which is one of the administrative access controls, provides a layer of defense for assets by *defining security requirements*.

* *Personnel* are a key component of defense. However, they *need proper training and education* to implement, comply with, and support security elements defined in an organization’s security policy.

* A combination of administrative, technical, and physical access controls provides a much stronger defense. Using only administrative, only technical, or only physical controls results in weaknesses that attackers can discover and exploit.

### Summarizing Access Control Models

Below section describe five access control models:

**Discretionary Access Control (DAC)**

  * Every object has an owner and the owner can grant or deny access to any other subjects. 
  * New Technology File System (NTFS), used on Microsoft Windows operating systems, uses the DAC model.

**Role Based Access Control (RBAC)** 

  * Privileges are assigned to roles or groups, more like job functions.
  * And user accounts are placed in roles.

**Rule-based access control (sometime called - restrictions or filters)** 

  * It applies global rules that apply to all subjects
  * Example: a firewall uses rules that allow or block traffic to all users equally

**Attribute Based Access Control (ABAC)**

  * Use of rules that can include multiple attributes
  * Many software-defined networks use the ABAC model
  * Can be in plaintext - “Allow Managers to access the WAN using a mobile device.”

**Mandatory Access Control (MAC) (sometime referred as lattice-based model)**

  * Use of labels applied to both subjects and objects
  * Example: User has a label of top secret, the user can be granted access to a top-secret document. In this example, both the subject and the object have matching labels

### Discretionary Access Controls

Every object has an owner (or data custodian), and owners have full control over their objects. Permissions (such as read and modify for files) are maintained in an ACL, and owners can easily change permissions. This makes the model very flexible.

### Non-discretionary Access Controls

The major difference between discretionary and nondiscretionary access controls is in how they are controlled and managed. Administrators centrally administer nondiscretionary access controls and can make changes that affect the entire environment. A static set of rules governing the whole environment manages access. Any model that isn’t a discretionary model is a nondiscretionary model.

#### Role Based Access Control

Systems that employ role based or task-based access controls define a subject’s ability to access an object based on the subject’s role or assigned tasks. Role Based Access Control (RBAC) is often implemented using groups.

![alt text](rbac.jpg)

This helps enforce the principle of least privilege by preventing privilege creep. *Privilege creep* is the tendency for users to accrue privileges over time as their roles and access needs change. Ideally, administrators revoke user privileges when users change jobs within an organization. In many cases, this follows the organization’s hierarchy documented in an organizational chart. Users who occupy management positions will have greater access to resources than users in a temporary job.

Microsoft operating systems implement RBAC with the use of groups.

Another method related to RBAC is task-based access control (TBAC). 

#### Rule-Based Access Controls

Uses a set of rules, restrictions, or filters to determine what can and cannot occur on a system. It includes granting a subject access to an object, or granting the subject the ability to perform an action. 

For example, the last rule might be deny all all to indicate the firewall should block all traffic in or out of the network that wasn’t previously allowed by another rule. 

#### Attribute Based Access Controls

Traditional rule-based access control models include global rules that apply to all subjects (such as users) equally. However, an advanced implementation of a rule-based access control is an Attribute Based Access Control (ABAC) model. ABAC models use policies that include multiple attributes for rules. Many software-defined networking applications use ABAC models.

#### Mandatory Access Controls

Use of classification labels. Each classification label represents a security domain, or a realm of security. A security domain is a collection of subjects and objects that share a common security policy. For example, a security domain could have the label Secret, and the MAC model would protect all objects with the Secret label in the same manner. Subjects are only able to access objects with the Secret label when they have a matching Secret label. Additionally, the requirement for subjects to gain the Secret label is the same for all subjects.

The MAC model is often referred to as a lattice-based model. 

![alt text](mac_lattice.jpg)

The horizontal lines labeled Confidential, Private, Sensitive, and Public mark the upper bounds of the classification levels

Classifications within a MAC model use one of the following three types of environments:

  * A ***hierarchical environment*** relates various classification labels in an ordered structure from low security to medium security to high security, such as Confidential, Secret, and Top Secret, respectively.  Clearance in one level grants the subject access to objects in that level as well as to all objects in lower levels but prohibits access to all objects in higher levels. For example, someone with a Top Secret clearance can access Top Secret data and Secret data.

  * In a ***compartmentalized environment***, there is no relationship between one security domain and another. Each domain represents a separate isolated compartment. To gain access to an object, the subject must have specific clearance for its security domain.

  * A ***hybrid environment*** combines both hierarchical and compartmentalized concepts so that each hierarchical level may contain numerous subdivisions that are isolated from the rest of the security domain. A subject must have the correct clearance and the need to know data within a specific compartment to gain access to the compartmentalized object.

## Understanding Access Control Attacks

IT security methods attempt to prevent loss of confidentiality, loss of integrity, and loss of availability. Focuses will be on access control attacks. 

### Risk Elements

A *risk* is the possibility or likelihood that a threat will exploit a vulnerability resulting in a loss such as harm to an asset. A *threat* is a potential occurrence that can result in an undesirable outcome. This includes potential attacks by criminals or other attackers. A *vulnerability* is any type of weakness.

*Risk management* attempts to reduce or eliminate vulnerabilities, or reduce the impact of potential threats by implementing controls or countermeasures. The key tasks that security professionals complete early in a risk management process are as follows:

* Identifying assets
* Identifying threats
* Identifying vulnerabilities

### Identifying assets

Asset valuation refers to identifying the actual value of assets with the goal of prioritizing them. Risk management focuses on assets with the highest value and identifies controls to mitigate risks to these assets.

> Customer goodwill is one of many intangible aspects that represent the actual value of an asset.

### Identifying threats

After identifying and prioritizing assets, an organization attempts to identify any possible threats to the valuable systems. *Threat modeling* refers to the process of identifying, understanding, and categorizing potential threats. A goal is to identify a potential list of threats to these systems and to analyze the threats.

It’s common for an organization to begin threat modeling early in the design process of a system and continue throughout its lifecycle. For example, Microsoft motto “Secure by Design, Secure by Default, Secure in Deployment and Communication” (also known as SD3+C). 

#### Advanced Persistent Threats

An Advanced Persistent Threats(APT) is a group of attackers who are working together and are highly motivated, skilled, and patient. They have advanced knowledge and a wide variety of skills to detect and exploit vulnerabilities. They are persistent and focus on exploiting one or more specific targets rather than just any target of opportunity. State nations (or governments) typically fund APTs. However, some groups of organized criminals also fund and run APTs.

Once an organization identifies these threats, it categorizes them based on the priority of the underlying assets.

Examples: “cozy bear attacks” - [wiki](https://en.wikipedia.org/wiki/Cozy_Bear) and “fancy bear attacks” - [wiki](https://en.wikipedia.org/wiki/Fancy_Bear)

#### Threat Modeling Approaches

Many organizations use one or more of the following three approaches to identify threats:

**Focused on Assets** `identify threats to the valuable assets`

**Focused on Attackers** `identify potential attackers and identify the threats they represent based on the attacker’s goals.` example, in government and APT knowledge they may have.

**Focused on Software** `consider potential threats against the software while developing`

### Identifying vulnerabilities

Organization attempts to discover weaknesses in these systems against potential threat.  *Vulnerability analysis* attempts to identify the strengths and weaknesses of the different access control mechanisms and the potential of a threat to exploit a weakness. A risk analysis will often include a vulnerability analysis by evaluating systems and the environment against known threats and vulnerabilities, followed by a penetration test to exploit vulnerabilities.

### Common Access Control Attacks

Access control starts with identification and authorization, and access control attacks often try to steal user credentials.

#### Access Aggregation Attacks

A person or group may be able to collect multiple facts about a system and then use these facts to launch an attack. Reconnaissance attacks are access aggregation attacks.

**Safeguard** Combining defense-in-depth, need-to-know, and least privilege principles helps prevent access aggregation attacks.

#### Password Attacks


**Safeguard** A strong password helps prevent password attacks. It is sufficiently long with a combination of character types. The phrase “sufficiently long” is a moving target and dependent on the usage and the environment. Passwords should not be stored in cleartext. Instead, they are typically hashed (SHA3). Change default passwords. 

The following sections describe common password attacks using dictionary, brute-force, rainbow tables, and sniffing methods.

* **Dictionary Attacks**  

A dictionary attack is an attempt to discover passwords by using every possible password in a predefined database or list of common or expected passwords. 

* **Brute-Force Attacks** 

A brute-force attack is an attempt to discover passwords for user accounts by systematically attempting all possible combinations of letters, numbers, and symbols. Attackers don’t typically type these in manually but instead have programs that can programmatically try all the combinations. A *hybrid attack* attempts a dictionary attack and then performs a type of brute-force attack with one-upped-constructed passwords. 

**Safeguard**  the longer the password and the more character types it includes, the more secure it is against brute-force attacks. Hash passwords.

As processors get better and cheaper, it will be easier for attackers to cluster more processors into a single system. This allows the systems to try more passwords per second, reducing the amount of time to takes to crack longer passwords.

* **Birthday Attack** 

A birthday attack focuses on finding collisions. Its name comes from a statistical phenomenon known as the birthday paradox. The birthday paradox states that if there are 23 people in a room, there is a 50 percent chance that any two of them will have the same birthday. This is not the same year, but instead the same month and day, such as March 30.

This is similar to finding any two passwords with the same hash. If a hashing function could only create 366 different hashes, then an attacker with a sample of only 23 hashes has a 50 percent chance of discovering two passwords that create the same hash. Hashing algorithms can create many more than 366 different hashes, but the point is that the birthday attack method doesn’t need all possible hashes to see a match.

**Safeguard** You can reduce the success of birthday attacks by using hashing algorithms with enough bits to make collisions computationally infeasible, and by using salts

* **Rainbow Table Attacks**

A rainbow table reduces this time by using large databases of precomputed hashes. Attackers guess a password (with either a dictionary or a brute-force method), hash it, and then put both the guessed password and the hash of the guessed password into the rainbow table.

**Safeguard** Many systems commonly *salt* passwords to reduce the effectiveness of rainbow table attacks. A salt is a group of random bits added to a password before hashing it. Cryptographic methods add the additional bits before hashing it, making it significantly more difficult for an attacker to use rainbow tables against the passwords. Bcrypt and Password-Based Key Derivation Function 2 (PBKDF2) are two commonly used algorithms to salt passwords. Adding a pepper to a salted password increases the security, making it more difficult to crack. A *pepper* is a large constant number stored elsewhere, such as a configuration value on a server or a constant stored within application code.

* **Sniffer Attacks** 

*Sniffing* captures packets sent over a network with the intent of analyzing the packets. A sniffer (also called a packet analyzer or protocol analyzer) is a software application that captures traffic traveling over the network. Administrators use sniffers to analyze network traffic and troubleshoot problems. A *sniffer attack* (also called a snooping attack or eavesdropping attack) occurs when an attacker uses a sniffer to capture information transmitted over a network. They can capture and read any data sent over a network in clear text, including passwords. Example tool, wireshark. 

**Safeguard** 

  * Encrypt all sensitive data (including passwords) sent over a network. Example: Kerberos encrypts tickets to prevent attacks
  * Use onetime passwords when encryption is not possible or feasible.
  * Protect network devices with physical security. 
  * Intrusion detection systems can monitor the network for sniffers and will raise an alert when they detect a sniffer on the network.

* **Spoofing Attacks**

Spoofing (also known as masquerading) is pretending to be something, or someone, else. Examples: an attacker can use someone else’s credentials to enter a building or access an IT system, IP spoofing attack, Email Spoofing (From field) and Phone Number Spoofing 

* **Social Engineering Attacks** 

*Social engineering* occurs when an attacker attempts to gain the trust of someone by using deceit, such as false flattery or impersonation, or by using conniving behavior. The attacker attempts to trick people into revealing information they wouldn’t normally reveal or perform an action they wouldn’t normally perform. Often the goal of the social engineer is to gain access to the IT infrastructure or the physical facility.

Example: skilled social engineers can convince an uneducated help desk employee that they are associated with upper management and working remotely but have forgotten their password. 

**Safeguard** Educating employees on common social engineering tactics reduces the effectiveness of these types of attacks. For physical security - Verifying visitor identities before providing access can mitigate these types of impersonation attacks. For *shoulder surfing* - screen filters, password marking.

* **Phishing** 

Phishing is a form of social engineering that attempts to trick users into giving up sensitive information, opening an attachment, or clicking a link. It often tries to obtain user credentials or personally identifiable information (PII) such as usernames, passwords, or credit card details by masquerading as a legitimate company.

Sophisticated attacks include a link to a bogus website that looks legitimate. For example, if the phishing email describes a problem with a PayPal account, the bogus website looks like the PayPal website.

The email could include a link to a website that installs a malicious *drive-by download* without the user’s knowledge. Installation of *Ransomware* is another example.

**Safeguard** Follow simple rule:

  * Be suspicious of unexpected email messages, or email messages from unknown senders.
  * Never open unexpected email attachments.
  * Never share sensitive information via email.
  * Be suspicious of any links in email.

Several variations of phishing attacks:

  * **Spear Phishing**

    Spear phishing is a form of phishing targeted to a specific group of users, such as employees within a specific organization. It may appear to originate from a colleague or co-worker within the organization or from an external source.

  * **Whaling**

    Whaling is a variant of phishing that targets senior or high-level executives such as chief executive officers (CEOs) and presidents within a company. A well-known whaling attack targeted about 20,000 senior corporate executives with an email identifying each recipient by name and stating they were subpoenaed to appear before a grand jury.  It included a link to get more information on the subpoena. If the executive clicked the link, a message on the website indicated that the executive needed to install a browser add-on to read the file.

  * **Vishing**

    Vishing is a variant of phishing that uses the phone system or VoIP. A common attack uses an automated call to the user explaining a problem with a credit card account.

* **Smartcard Attacks**

A *side-channel attack* is a passive, noninvasive attack intended to observe the operation of a device. When the attack is successful, the attacker can learn valuable information contained within the card, such as an encryption key.

A smartcard includes a microprocessor, but it doesn’t have internal power. Instead, when a user inserts the card into the reader, the reader provides power to the card. The reader has an electromagnetic coil that excites electronics on the card. This provides enough power for the smartcard to transmit data to the reader.

Side-channel attacks analyze the information sent to the reader. Sometimes they can measure the power consumption of a chip, using a power monitoring attack or differential power analysis attack, to extract information. In a timing attack, they can monitor the processing timings to gain information based on how much time different computations require. Fault analysis attacks attempt to cause faults, such as by providing too little power to the card, to glean valuable information.

### Summary of Protection Methods

* **Control physical access to systems** 
* **Control electronic access to files** `example, password file`
* **Create a strong password policy** `strong passwords``regularly change``password policies`
* **Hash and salt passwords** `bcrypt and PBKDF2 to salt passwords` `external pepper`
* **Use password masking** `use asterisk (*)`
* **Deploy multifactor authentication** `biometrics or token devices`
* **Use account lockout controls** `lock an account after the incorrect password is entered a predefined number of times`
* **Use last logon notification** `message including the time, date, and location`
* **Educate users about security** 
