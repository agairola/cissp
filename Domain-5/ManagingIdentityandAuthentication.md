## Controlling Access to Assets

An asset includes information, systems, devices, facilities, and personnel.

**Information** `all of organization data` `Data stored in simple files on servers, computers, and smaller devices or huge databases within a server farm`

**Systems** `any information technology (IT) systems` 

**Devices** `computing system, including servers, desktop computers, portable laptop computers, tablets, smartphones, and external devices such as printers` `BYOD devices to`
**Facilities** `any physical location that it owns or rents`

**Personnel** 


### Comparing Subject and Object

Access control addresses more than just controlling which users can access which files or services. It is about the relationships between entities (that is, subjects and objects). Access is the transfer of information from an object to a subject, which makes it important to understand the definition of both subject and object.

**Subject** – (Active) Most often users, but can also be programs – Subjects manipulate object.

**Object** – (Passive) Any passive data (both physical paper and data) – Objects are manipulated by subject.

> You can often simplify the access control topics by substituting the word user for subject and the word file for object. 

Programs, services, and computers, at times listed as subject or object as roles are interchangeable.

As an example, consider a common web application that provides dynamic web pages to users. Users query the web application to retrieve a web page, so the application starts as an *object*. The web application then switches to a *subject* role as it queries the user’s computer to retrieve a cookie and then queries a database to retrieve information about the user based on the cookie. Finally, the application switches back to an *object* as it sends dynamic web pages back to the user.

### The CIA Triad and Access Control

**Confidentiality** Access controls help ensure that only `authorized subjects can access objects`. When unauthorized entities can access systems or data, it results in a loss of confidentiality.

**Integrity** Integrity ensures that data or system configurations are `not modified without authorization`, or if unauthorized changes occur, security controls detect the changes. If unauthorized or unwanted changes to objects occur, it results in a loss of integrity.

**Availability** Authorized requests for objects must be granted to subjects within a `reasonable amount of time`. In other words, systems and data should be available to users and other subjects when they are needed. If the systems are not operational or the data is not accessible, it results in a loss of availability.

### Type of Access Control

Access control includes the following overall steps:

* Identify and authenticate users or other subjects attempting to access resources.
* Determine whether the access is authorized.
* Grant or restrict access based on the subject’s identity.
* Monitor and record access attempts.

Three primary control types are `preventive, detective, and corrective`.

Four other access control types, commonly known as `deterrent, recovery, directive, and compensating` access controls.

![alt text](typesofaccesscontrol.png)


Access controls are also categorized by how they are implemented:

* **Administrative Access Controls**
* **Logical/Technical Controls**
* **Physical Controls**

![alt text](implementationofaccesscontrol-1.png)
![alt text](implementationofaccesscontrol-2.png)

## Comparing Identification and Authentication

*Identification* is the process of a subject claiming, or professing, an identity. A subject must provide an identity to a system to start the authentication, authorization, and accountability processes. Example, username. A core principle with authentication is that all subjects must have unique identities.

*Authentication* verifies the identity of the subject by comparing one or more factors against a database of valid identities, such as user accounts.


### Registration and Proofing of Identity

  * The registration process occurs when a user is first given an identity. Example, a new employee is given userid by HR.

  * Identity proofing normally entails asking the user to provide information that is known to the user and the bank (for example) such as account numbers and personal information about the user such as a national identification number or social security number.

### Authorization and Accountability

  * **Authorization** Subjects are granted access to objects based on proven identities. For example, administrators grant users access to files based on the user’s proven identity.

  * **Accountability** Users and other subjects can be held accountable for their actions when auditing is implemented. Auditing tracks subjects and records when they access objects, creating an audit trail in one or more audit logs. For example, auditing can record when a user reads, modifies, or deletes a file. Auditing provides accountability. Additionally, assuming the user has been properly authenticated, audit logs provide *nonrepudiation*. The user cannot believably deny taking an action recorded in the audit logs.

### Authentication Factor

Three basic methods of authentication are also known as types or factors. They are as follows:

* **Type 1** A Type 1 authentication factor is *something you know*. Examples include a password, personal identification number (PIN), or passphrase.

* **Type 2** A Type 2 authentication factor is *something you have*. Physical devices that a user possesses can help them provide authentication. Examples include a smartcard, hardware token, memory card, or Universal Serial Bus (USB) drive.

* **Type 3** A Type 3 authentication factor is *something you are or something you do*. It is a physical characteristic of a person identified with different types of biometrics. Examples in the something-you-are category include fingerprints, voice prints, retina patterns, iris patterns, face shapes, palm topology, and hand geometry. Examples in the something-you-do category include signature and keystroke dynamics, also known as behavioral biometrics.


In addition to the three primary authentication factors, there are some others.

**Somewhere You Are** subject’s location based on a specific computer, a geographic location identified by an Internet Protocol (IP) address, or a phone number identified by caller ID.

**Context-Aware Authentication** Many mobile device management (MDM) systems use context-aware authentication to identify mobile device users. It can identify multiple elements such as the location of the user, the time of day, and the mobile device. If the user meets all the requirements (location, time, and type of device in this example), it allows the user to log on using the other methods such as with a username and password.

### Passwords

A *static password* stays the same for a length of time such as 30 days, but static passwords are the weakest form of authentication. Passwords are weak security mechanisms for several reasons:

* Users often choose passwords that are easy to remember and therefore easy to guess or crack.
* Randomly generated passwords are hard to remember; thus, many users write them down.
* Users often share their passwords, or forget them.
* Attackers detect passwords through many means, including observation, sniffing networks, and stealing security databases.
* Passwords are sometimes transmitted in clear text or with easily broken encryption protocols. Attackers can capture these passwords with network sniffers.
* Password databases are sometimes stored in publicly accessible online locations.
* Brute-force attacks can quickly discover weak passwords.


> **PASSWORD STORAGE** Most OS use HASH (SHA-3) to store the password instead of storing it in plaintext. Many systems use more sophisticated hashing functions such as Password-Based Key Derivation Function 2 (PBKDF2) or bcrypt to add bits to the password before hashing it. These additional bits are referred to as a salt, and salting helps thwart rainbow table attacks.

#### Creating Strong Passwords

Organizations often include a written password policy in the overall security policy. IT security professionals then enforce the policy with technical controls such as a technical *password policy* that enforces the *password restriction* requirements. The following list includes some common password policy settings:

* **Maximum Age** change their password periodically, such as every 45 days.
* **Password Complexity** An eight-character password using uppercase characters, lowercase characters, symbols, and numbers. National Institute of Standards and Technology (NIST) special publication (SP) **800-63B**, “Digital Identity Guidelines,” states that authentication systems should support the use of any printable American Standard Code for Information Interchange (ASCII) characters and the space character.
* **Password Length** NIST SP **800-63B** states that passwords should be at least eight characters long, and systems should support passwords as long as 64 characters. Many organizations require privileged account passwords to be longer, such as at least 15 characters long.

> NIST SP 800-63B says that passwords should be at least eight characters long and support the use of any printable ASCII characters, and systems should support passwords of at least 64 characters long. It also recommends hashing the password using random salts of at least 32 bits in length and storing the salted hash of the password plus use additional authentication factor, such as a smart card 

* **Password History** A password history remembers a certain number of previous passwords and prevents users from reusing a password in the history. Minimum password age is often set to one day.

The following suggestions can help them create strong passwords:

* *Do not* use any part of your name, logon name, email address, employee number, national identification number or social security number, phone number, extension, or any other identifying name or code.
* *Do not* use information available from social network profiles such as a family member’s name, a pet’s name, or your birth date.
* *Do not* use dictionary words (including words in foreign dictionaries), slang, or industry acronyms.
* *Do use* nonstandard capitalization and spelling, such as stRongsecuRitee instead of strongsecurity.
* *Do replace* letters with special characters and numbers, such as stR0ng$ecuR1tee instead of strongsecurity.
