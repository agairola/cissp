## Applying Security Operations Concepts

The primary purpose for security operations practices is to safeguard assets including information, systems, devices, and facilities. *Purpose:* `reduce the overall risk` `identify threats and vulnerabilities.`. Security operations are part of *due care* and *due diligence* responsibility of Senior executives.

### Need-to-know And Least Privilege

It is a common mechanism to provide protection for valuable assets by limiting access to these assets.  Need-to-know focuses on permissions and the ability to access information, whereas least privilege focuses on privileges.

#### Need-to-Know Access

The primary purpose is to keep secret information secret. Limit the people who know and you increase the chances of keeping it secret. Need-to-know is commonly associated with security clearances.

#### The Principle of Least Privilege

The principle of least privilege states that subjects are granted only the privileges necessary to perform assigned work tasks and no more. The principle of least privilege relies on the assumption that all users have a well-defined job description that personnel understand. Privileges applies to user, system, data, application etc. 


Additional concepts personnel should consider when implementing need-to-know and least privilege are entitlement, aggregation, and transitive trusts:

**Entitlement** Entitlement refers to the amount of privileges granted to users, typically when first provisioning an account. Proper user provisioning processes follow the principle of least privilege.

**Aggregation** In the context of least privilege, aggregation refers to the amount of privileges that users collect over time. To avoid access aggregation problems such as this, administrators should revoke privileges when users move to a different department and no longer need the previously assigned privileges.

**Transitive Trust** There is a trust relationship between parent security domain (*primary* and *training*), with transitive trust, the trust relationship extends to child domain (eg. *training.cissp*). From least privileges perspective admin should exmain allow or deny these trust relationship in other words make it **non-transitive**.

### Separation of duties and responsibilities

Separation of duties and responsibilities ensures that no single person has total control over a critical function or system. This is necessary to ensure that no single person can compromise the system or its security. Instead, two or more people must conspire or collude against the organization, which increases the risk for these people. Its an `effective deterrent`. 

Organizational *example*, divide the security or administrative capabilities and functions among multiple trusted individuals. When the organization divides administration and security responsibilities among several users, no single person has sufficient access to circumvent or disable security mechanisms.

#### Separation of Privilege

It builds on the principle of least privilege and applies it to applications and processes. A separation-of-privilege policy requires the use of granular rights and permissions. 

#### Segregation of Duties

When duties are properly segregated, no single employee will have the ability to commit fraud or make a mistake and have the ability to cover it up. 

**Standard/Guideline:** Sarbanes–Oxley Act (SOX) of 2002 which is used by all public companies that deals with Securities and Exchange Commission (SEC).

*Example:* Personnel responsible for auditing, monitoring, and reviewing security do not have other operational duties related to what they are auditing, monitoring, and reviewing.

*Another Example:* The programmer can make unauthorized modifications to an application, but auditing or reviews by a security administrator would detect the unauthorized modifications. However, if a single person had the duties (and the privileges) of both jobs, this person could modify the application and then cover up the modifications to prevent detection.

#### Two-Person Control

Two-person control (often called the two-man rule) requires the approval of two individuals for critical tasks. *Example*, safe deposit boxes in banks often require two keys. A bank employee controls one key and the customer holds the second key.

***Split knowledge*** combines the concepts of separation of duties and two-person control into a single solution. The basic idea is that the information or privilege required to perform an operation be divided among two or more users. This ensures that no single person has sufficient privileges to compromise the security of the environment.

### Job Rotation

Job rotation (sometimes called rotation of duties) means simply that employees are rotated through jobs, or at least some of the job responsibilities are rotated to different employees. 

It is both `deterrent` and a `detection mechanism`.

If employees know that someone else will be taking over their job responsibilities at some point in the future, they are less likely to take part in fraudulent activities.

### Mandatory Vacations

Many organizations require employees to take mandatory vacations in one-week or two-week increments. Another employee takes over an individual’s job responsibilities for at least a week. If an employee is involved in fraud, the person taking over the responsibilities is likely to discover it.

It is both`deterrent` and a `detection mechanism`.

### Privileged Account Management

Privileged account management ensures that personnel do not have more privileges than they need and that they do not misuse these privileges. *Special privilege operations* includes creating new user accounts, adding new routes to a router table, altering the configuration of a firewall, and accessing system log and audit files.

Using principle of least privilege, ensures that only a limited number of people have these special privileges. ***Monitoring*** ensures that users granted these privileges do not abuse them.

*Principles such as least privilege and separation of duties help prevent security policy violations, and monitoring helps to deter and detect any violations that occur despite the use of preventive controls*

### Managing the Information Cycle

Security controls protect information throughout its lifecycle. The following list includes some terms used to identify different phases of data within its lifecycle:

**Creation or Capture** User or system creates a file or data. Network or monitoring system can capture the dats.

**Classification** Personnel should mark the data as soon as possible after creating it.

**Storage** Protected by adequate security controls based on its classification. This includes applying appropriate permissions to prevent unauthorized disclosure. Sensitive data should also be encrypted to protect it.

**Usage** Usage refers to anytime data is in use or in transit over a network.

**Archive** Data is sometimes archived to comply with laws or regulations requiring the retention of data.

**Destruction or Purging** When data is no longer needed, it should be destroyed in such a way that it is not readable. When deleting sensitive data, many organizations require personnel to destroy the disk to ensure that data is not accessible. **Standard/Guideline:** The National Institute of Standards and Technology (NIST) special publication (SP) *SP 800-88r1*, “Guidelines for Media Sanitization,” provides details on how to sanitize media. 

### Service-Level Agreements

A service-level agreement (SLA) is an agreement between an organization and an outside entity, such as a vendor. The SLA stipulates performance expectations and often includes penalties if the vendor doesn’t meet these expectations.

*Example:* Cloud-based services to rent servers.

In addition to an SLA, organizations sometimes use a ***memorandum of understanding (MOU)*** and/or an ***interconnection security agreement (ISA)***. 

MOUs document the intention of two entities to work together toward a common goal. They can use an ISA to specify the technical requirements of the connection, like minimum encryption methods .

**Standard/Guideline:** NIST Special Publication *800-47*, “Security Guide for Interconnecting Information Technology Systems,” includes detailed information on MOUs and ISAs.

### Addressing Personnel Safety and Security

Organizations should implement security controls that enhance personnel safety as they are impossible to replace.

As an *example*, consider the exit door in a datacenter that is controlled by a pushbutton electronic cipher lock. If a fire results in a power outage, does the exit door automatically unlock or remain locked? An organization that values personnel safety over the assets in the datacenter will ensure that the locks unlock the exit door when power is lost.

#### Duress

Duress systems are useful when personnel are working alone. Security systems often include code words or phrases that personnel use to verify that everything truly is okay, or to verify that there is a problem.

#### Travel

Another safety concern is when employees travel because criminals might target an organization’s employees while they are traveling. Employees should also be warned about the many risks associated with electronic devices (such as smartphones, tablets, and laptops) when traveling. These risks include the following:

**Sensitive Data** Ideally the device should not contain sensitive data but for any reason employee needs the data it should be encrypted using strong encryption.

**Malware and Monitoring Devices** Malware or monitoring software can be installed when employee travel to a foreign country. Its suggested to bring temporary devices what would be wiped clean and reimaged.

**Free Wi-Fi** Avoid to mitigate `man-in-the-middle attack`.

**VPNs** Employers should have access to virtual private networks (VPNs) that they can use to create secure connections. These can be used to access resources in the internal network, including their work-related email.

### Emergency Management

Emergency management plans and practices help an organization address personnel safety and security after a disaster.

### Security Training and Awareness

It’s also important to implement security training and awareness programs. These programs help ensure that personnel are aware of duress systems, travel best practices, emergency management plans, and general safety and security best practices.

