All follow-on actions vary depending on the classification. For example, highly classified data requires stringent security controls. In contrast, unclassified data uses fewer security controls.

## Identify and Classify Assets

Organizations often include classification definitions within a security policy. Personnel then label assets appropriately based on the security policy requirements.

Assets - sensitive data, the hardware used to process it, and the media used to hold it.

### DEFINING SENSITIVE DATA

Sensitive data is any information that `isn’t public or unclassified`. It can include confidential, proprietary, protected, or any other type of data that an organization needs to protect due to its value to the organization, or to comply with existing laws and regulations.

#### Personally Identifiable Information

Personally identifiable information (PII) is any information that can identify an individual. `National Institute of Standards and Technology (NIST) Special Publication (SP) 800-122` provides a more formal definition:

```
Any information about an individual maintained by an agency, including

(1) any information that can be used to distinguish or trace 
an individual’s identity, such as name, social security 
number, date and place of birth, mother’s maiden name,
 or biometric records; and

(2) any other information that is linked or linkable 
to an individual, such as medical, educational, 
financial, and employment information.
```

The key is that organizations have a responsibility to protect PII.

#### Protected Health Information

Protected health information (PHI) is any health-related information that can be related to a specific person. In the United States, the `Health Insurance Portability and Accountability Act (HIPAA)` mandates the protection of PHI.

```
Health information means any information, whether oral
or recorded in any form or medium, that—

(A) is created or received by a health care provider,
 health plan, public health authority, employer, 
 life insurer, school or university, or 
 health care clearinghouse; and

(B) relates to the past, present, or future physical 
or mental health or condition of any individual, 
the provision of health care to an individual, 
or the past, present, or future payment for the 
provision of health care to an individual.
```

Any employer that provides, or supplements, healthcare policies collects and handles PHI.

#### Proprietary Data

Proprietary data refers to any data that helps an organization maintain a competitive edge. It could be software code it developed, technical plans for products, internal processes, intellectual property, or trade secrets. If competitors are able to access the proprietary data, it can seriously affect the primary mission of an organization.

### DEFINING DATA CLASSIFICATIONS

A data classification identifies the value of the data to the organization and is critical to protect data confidentiality and integrity. The policy identifies classification labels used within the organization. It also identifies how data owners can determine the proper classification and how personnel should protect data based on its classification.

Example: government data classifications include top secret, secret, confidential, and unclassified. 

**Top Secret** The top secret label is “applied to information, the unauthorized disclosure of which reasonably could be expected to cause `exceptionally grave damage` to the national security that the original classification authority is able to identify or describe.”

**Secret** The secret label is “applied to information, the unauthorized disclosure of which reasonably could be expected to cause `serious damage` to the national security that the original classification authority is able to identify or describe.”

**Confidential** The confidential label is “applied to information, the unauthorized disclosure of which reasonably could be expected to cause `damage` to the national security that the original classification authority is able to identify or describe.”

**Unclassified** Unclassified refers to any data that doesn’t meet one of the descriptions for top secret, secret, or confidential data. Within the United States, unclassified data is available to anyone, though it often requires individuals to request the information using procedures identified in the Freedom of Information Act (FOIA).

There are additional subclassifications of `unclassified` such as `for official use only (FOUO)` and `sensitive but unclassified (SBU)`. Documents with these designations have strict controls limiting their distribution. As an example, the U.S. Internal Revenue Service (IRS) uses `SBU` for individual tax records, limiting access to these records.

An organization doesn’t just consider the sensitivity of the data but also the criticality of the data.

Data classifications - Government vs Non-Government

![alt text](dataclassifications.jpg)

> Remember that “sensitive information” typically refers to any information that isn’t public or unclassified.

### DEFINING ASSET CLASSIFICATIONS

Asset classifications should match the data classifications. In other words, if a computer is processing top secret data, the computer should also be classified as a top secret asset.

### DETERMINING DATA SECURITY CONTROLS

After defining data and asset classifications, it’s important to define the security requirements and identify security controls to implement those security requirements. For this example, we’re limiting the type of data to only email. The organization has defined how it wants to protect email in each of the data categories

Securing email data:

Classification | Security requirements for email
--- | ---
Confidential/Proprietary (highest level of protection for any data) | Email and attachments must be encrypted with AES 256. Email and attachments remain encrypted except when viewed. Email can only be sent to recipients within the organization. Email can only be opened and viewed by recipients (forwarded emails cannot be opened). Attachments can be opened and viewed, but not saved. Email content cannot be copied and pasted into other documents.Email cannot be printed.
Private (examples include PII and PHI) | Email and attachments must be encrypted with AES 256. Email and attachments remain encrypted except when viewed. Can only be sent to recipients within the organization.
Sensitive (lowest level of protection for classified data) | Email and attachments must be encrypted with AES 256. 
Public | Email and attachments can be sent in cleartext.

Although it’s possible to meet all of the requirements in above table they require implementing other solutions. For example, these emails pass through a data loss prevention (DLP) server that detects the labels, and applies the required protection.

Additionally, identity and access management (IAM) security controls help ensure that only authorized personnel can access resources.

### UNDERSTANDING DATA STATES

It’s important to protect data in all data states, including while it is at rest, in motion, and in use.

**Data at Rest** Data at rest is any data `stored` on media such as system hard drives, external USB drives, storage area networks (SANs), and backup tapes.

**Data in Transit** Data in transit (sometimes called data in motion) is any data `transmitted over a network`. This includes data transmitted over an internal network using wired or wireless methods and data transmitted over public networks such as the internet.

**Data in Use** Data in use refers to data in memory or temporary storage buffers, while an application is using it. Because an application can’t process encrypted data, it must decrypt it in memory.

The best way to protect the confidentiality of data is to use strong encryption protocols + strong authentication and authorization controls help prevent unauthorized access.

> The Identity Theft Resource Center (ITRC) routinely tracks data breaches. They post reports through their website (www.idtheftcenter.org/) that are free to anyone

### HANDLING INFORMATION AND ASSETS

A key goal of managing sensitive data is to prevent data breaches. A data breach is any event in which an unauthorized entity can view or access sensitive data. 

#### Marking Sensitive Data and Assets

Marking (often called labeling) sensitive information ensures that users can easily identify the classification level of any data. The most important information that a mark or a label provides is the classification of the data. Marking includes both physical and electronic marking and labels.

`Physical labels` indicate the security classification for the data stored on assets such as media or processed on a system. For example, if a backup tape includes secret data, a physical label attached to the tape makes it clear to users that it holds secret data. A computer used to process confidential, secret, and top secret data should be marked with a label indicating that it processes top secret data. Physical labels remain on the system or media throughout its lifetime.

Marking also includes using `digital marks or labels`. A simple method is to include the classification as a header and/or footer in a document, or embed it as a watermark. Headers aren’t limited to files. Backup tapes often include header information, and the classification can be included in this header.

Another benefit of headers, footers, and watermarks is that DLP systems can identify documents that include sensitive information, and apply the appropriate security controls. Some DLP systems will also add metadata tags to the document when they detect that the document is classified. These tags provide insight into the document’s contents and help the DLP system handle it appropriately.

Organizations often identify procedures to `downgrade media`. For example, if a backup tape includes confidential information, an administrator might want to `downgrade` the tape to unclassified. The organization would identify trusted procedures that will purge the tape of all usable data. After administrators purge the tape, they can then downgrade it and replace the labels. However, many organizations prohibit downgrading media at all. The policy might mandate destroying this tape when it reaches the end of its lifecycle.

#### Handling Sensitive Information and Assets
