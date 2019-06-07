Communications security is designed to detect, prevent, and even correct data transportation errors (that is, it provides integrity protection as well as confidentiality). This is done to sustain the security of networks while supporting the need to exchange and share data.

## Network and Protocol Security Mechanisms

Focus would be on Transmission Control Protocol/Internet Protocol (TCP/IP) protocol suite.

### Secure Communications Protocols

Protocols that provide security services for application-specific communication channels are called secure communication protocols. The following list includes a small sampling of some of the options available:

**IPsec**

Uses public key cryptography to provide encryption, access control, nonrepudiation, and message authentication, all using IP-based protocols. The primary use of IPsec is for virtual private networks (VPNs), so IPsec can operate in either transport or tunnel mode

**Kerberos**

Provide reliable authentication protection

**SSH**

Used to encrypt numerous plaintext utilities (such as rcp, rlogin, rexec), serve as a protocol encrypter (such as with SFTP), and function as a VPN.

**Signal Protocol**

Provides end-to-end encryption for voice communications, videoconferencing, and text message services.

**Secure Remote Procedure Call (S-RPC)**

This is an authentication service and is simply a means to prevent unauthorized execution of code on remote systems.

**Secure Sockets Layer (SSL)**

SSL can be used to secure web, email, File Transfer Protocol (FTP) or even Telnet traffic. Provides confidentiality and integrity.

**Transport Layer Security (TLS)**

TLS functions in the same general manner as SSL, but it uses stronger authentication and encryption protocols.

### Authentication Protocols

After a connection is initially established between a remote system and a server or a network, the first activity that should take place is to verify the identity of the remote user. This activity is known as authentication.

**Challenge Handshake Authentication Protocol (CHAP)**:

  * Used over Point-to-Point Protocol (PPP) links
  * CHAP encrypts usernames and passwords. 
  * It performs authentication using a challenge-response dialogue that cannot be replayed.
  * CHAP also periodically reauthenticates the remote system throughout an established communication session to verify a persistent identity of the remote client.

**Password Authentication Protocol (PAP)**
  
  * PAP transmits usernames and passwords in cleartext. 
  * It offers no form of encryption

**Extensible Authentication Protocol (EAP)**

  * This is a framework for authentication instead of an actual protocol.
  * Example: EAP, PEAP, AND LEAP

    * Protected Extensible Authentication Protocol (PEAP) encapsulates EAP in a TLS tunnel. PEAP is also preferred over Cisco’s proprietary EAP known as Lightweight Extensible Authentication Protocol (LEAP).

## Secure Voice Communications

Normal *private branch exchange (PBX)* or POTS/*public switched telephone network (PSTN)* voice communications are vulnerable to interception, eavesdropping, tapping, and other exploitations. Often, physical security is required to maintain control over voice communications within the confines of your organization’s physical locations. Security of voice communications outside your organization is typically the responsibility of the phone company from which you lease services. If voice communication vulnerabilities are an important issue for sustaining your security policy, you should deploy an encrypted communication mechanism and use it exclusively


### Voice Over Internet Protocol

Hackers can wage a wide range of potential attacks against a VoIP solution:

* *Caller ID* can be falsified easily using any number of VoIP tools, so hackers can perform *vishing (VoIP phishing)* or *Spam over Internet Telephony (SPIT)* attacks.

* Call manager systems and the VoIP phones are vulnerable host OS attacks and DOS.

* Perform *man-in-the-middle* (MitM) attacks by spoofing call managers or endpoint connection negotiations and/or responses.

* There are also risks associated with deploying VoIP phones off the same switches as desktop and server systems. This could allow for 802.1X authentication falsification as well as virtual local area network (VLAN) and VoIP hopping (i.e., jumping across authenticated channels).

* It is often possible to listen in on VoIP communications by decoding the VoIP traffic when it isn’t encrypted.

**SafeGuard** Use *Secure Real-Time Transport Protocol or SecureRTP (SRTP)* which aims to minimize the risk of VoIP DoS through robust encryption and reliable authentication.

### Social Engineering

Social engineering is a means by which an unknown, untrusted, or at least unauthorized person gains the trust of someone inside your organization. Social engineering is the art of using an organization’s own people against it. The only way to protect against social engineering attacks is to teach users how to respond and interact with any form of communications, whether voice-only, face to face, IM, chat, or email.

Here are some guidelines:

* Always err on the side of caution whenever voice communications seem odd, out of place, or unexpected.
* Always request proof of identity.
* Require `callback` authorizations on all voice-only requests for network alterations or activities. A callback authorization occurs when the initial client connection is disconnected, and a person or party would call the client on a predetermined number that would usually be stored in a corporate directory in order to verify the identity of the client.
* Classify information (usernames, passwords, IP addresses, manager names, dial-in numbers, and so on), and clearly indicate which information can be discussed or even confirmed using voice communications.
* If privileged information is requested over the phone by an individual who should know that giving out that particular information over the phone is against the company’s security policy, ask why the information is needed and verify their identity again. This incident should also be reported to the security administrator.
* Never give out or change passwords via voice-only communications.
* When disposing of office documentation (according to policy and regulation compliance) always use a secure disposal or destruction process, especially for any paperwork or media that contains information about the IT infrastructure or its security mechanisms.

### Fraud and Abuse

