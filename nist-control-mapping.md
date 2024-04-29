# NIST Control Mappings
If you are curious about which NIST 800-53 controls are satisfied by the instructions in the [main guide](README.md), see each control family below. 

# Table of Contents
- [AC Access Control](#ac-access-control)
- [AU Audit and Accountability](#au-audit-and-accountability)
- [CA Assessment Authorization and Monitoring](#ca-assessment-authorization-and-monitoring)
- [CM Configuration Management](#cm-configuration-management)
- [IA Identification and Authentication](#ia-identification-and-authentication)
- [SC Systems and Communications Protection](#sc-systems-and-communications-protection)
- [SI System and Information Integrity](#si-system-and-information-integrity)

# AC Access Control
The AC Control Family consists of security requirements detailing system logging. The applicable control for S3 buckets is below: 
- AC-2(12)
- AC-22

AC-2(12) Reads as:
> Monitor system accounts for [Assignment: organization-defined atypical usage]; and Report atypical usage of system accounts to [Assignment: organization-defined personnel or roles].

AC-22 Reads as:
> Designate individuals authorized to make information publicly accessible; Train authorized individuals to ensure that publicly accessible information does not contain nonpublic information; Review the proposed content of information prior to posting onto the publicly accessible system to ensure that nonpublic information is not included; and Review the content on the publicly accessible system for nonpublic information [Assignment: organization-defined frequency] and remove such information, if discovered.

The ["Safely Sharing Files Publicly via S3"](README.md#safely-sharing-files-publicly-via-s3) section of the main guide satisfies controls AC-2(12) and AC-22. 

# AU Audit and Accountability
The AU control family comprises security controls related to an organization’s audit capabilities. The applicable control for S3 buckets is below: 
- AU-2
- AU-3
- AU-8
- AU-9
- AU-9(3)
- AU-9(4)
- AU-10
- AU-12
- AU-12(1)
- AU-12(3)

The ["Turn On Server Access Logging"](README.md#turn-on-server-access-logging) section of the main guide will cover controls: AU-2, AU-3, AU-8, AU-10, AU-12.
These controls read as:

AU-2:
> Determines that the information system is capable of auditing the following events: [Assignment: organization-defined auditable events];

AU-3:
> The information system generates audit records containing information that establishes what type of event occurred, when the event occurred, where the event occurred, the source of the event, the outcome of the event, and the identity of any individuals or subjects associated with the event.

AU-8:
> Use internal system clocks to generate time stamps for audit records; and
Record time stamps for audit records that meet [Assignment: organization-defined granularity of time measurement] and that use Coordinated Universal Time, have a fixed local time offset from Coordinated Universal Time, or that include the local time offset as part of the time stamp.

AU-10:
> The information system protects against an individual (or process acting on behalf of an individual) falsely denying having performed [Assignment: organization-defined actions to be covered by non-repudiation].

AU-12:
> Provides audit record generation capability for the auditable events defined in AU-2 at [Assignment: organization-defined information system components];
Allows [Assignment: organization-defined personnel or roles] to select which auditable events are to be audited by specific components of the information system; and
Generates audit records for the events defined in AU-2 d. with the content defined in AU-3.

The ["Implementing CloudTrail Logging"](README.md#implementing-cloudtrail-logging) section of the main guide will cover controls: AU-2, AU-10, AU-11, AU-12, AU-12(1), AU-12(3).
These controls read as:

AU-2:
> Determines that the information system is capable of auditing the following events: [Assignment: organization-defined auditable events];

AU-10:
> The information system protects against an individual (or process acting on behalf of an individual) falsely denying having performed [Assignment: organization-defined actions to be covered by non-repudiation].

AU-12:
> Provides audit record generation capability for the auditable events defined in AU-2 at [Assignment: organization-defined information system components];
Allows [Assignment: organization-defined personnel or roles] to select which auditable events are to be audited by specific components of the information system; and
Generates audit records for the events defined in AU-2 d. with the content defined in AU-3.

AU-12(1):
> Compile audit records from [Assignment: organization-defined system components] into a system-wide (logical or physical) audit trail that is time-correlated to within [Assignment: organization-defined level of tolerance for the relationship between time stamps of individual records in the audit trail].

AU-12(3):
> The information system provides the capability for [Assignment: organization-defined individuals or roles] to change the auditing to be performed on [Assignment: organization-defined information system components] based on [Assignment: organization-defined selectable event criteria] within [Assignment: organization-defined time thresholds].

# CA Assessment Authorization and Monitoring
The CA family of controls deals with assessing the environment and access, authorizing access, and monitoring. The applicable control for S3 buckets is below: 
- CA-9

NIST 800-53 control CA-9 reads: 
> Authorize internal connections of [organization-defined system components or classes of components] to the system;

The ["Protecting S3 Buckets by Limiting Public Access"](README.md#protecting-s3-buckets-by-limiting-public-access) section of the guide satisfies control CA-9. 

# CM Configuration Management
The CM family of controls deals with managing the configuration of information systems. For S3 buckets, the below control is applicable: 
- CM-5

NIST 800-53 control CM-5 reads: 
> Define, document, approve, and enforce physical and logical access restrictions associated with changes to the system.

The ["Removing Overly Permissive Admin Accounts"](README.md#removing-overly-permissive-admin-accounts) section of the guide satisfies control CM-5. 

# IA Identification and Authentication
## IA-2 Identification and Authentication (organizational Users)
Identifying individual users and authenticating those users so that you can restrict access and assign permissions appropriately is crucial. For S3 buckets, the below controls are applicable: 
- IA-2
- IA-2(1)
- IA-2(2)

NIST 800-53 control IA-2 reads: 
> Uniquely identify and authenticate organizational users and associate that unique identification with processes acting on behalf of those users.

The ["Implementing Authentication for S3 Users"](README.md#implementing-authentication-for-s3-users) section of the guide satisfies control IA-2. 

NIST 800-53 IA-2(1) reads: 
> Implement multi-factor authentication for access to privileged accounts.

And IA-2(2) reads: 
> Implement multi-factor authentication for access to privileged accounts.

The ["Implementing Multi-factor Authentication on AWS Accounts"](README.md#implementing-multi-factor-authentication-on-aws-accounts) section of the guide satisfies controls IA-2(1) and IA-2(2). 

# SC Systems and Communications Protection
The System and Communications Protection control focuses on safeguarding the integrity, confidentiality, and availability of information systems and communications. For S3 Buckets here are the controls that apply:
- SC-5
- SC-8(1)
- SC-12
- SC-12(1)
- SC-13
- SC-28
- SC-28(1)

NIST 800-53 control SC-5 reads:
> Restrict the ability of individuals to launch the following denial-of-service attacks against other systems

The ["Implementing AWS Shield for DDoS Protections"](README.md#implementing-aws-shield-for-ddos-protections) section fo the main guide satisfies control SC-5. 

NIST 800-53 control SC-8,12,12(1),13,28 and 28(1) read respectfully:
> - Protecting the confidentiality and integrity of transmitted information
> - Establish and manage cryptographic keys when cryptography is employed within the system in accordance with key management requirements
> - Maintain availability of information in the event of the loss of cryptographic keys by users.
> - Cryptographic Protection
> - Protect the information at rest
> - Implement cryptographic mechanisms to prevent unauthorized disclosure and modification of information at rest

The ["Enabling Server-Side Encryption and Key Management Service for AWS S3 Buckets"](READMe.md#enabling-server-side-encryption-and-key-management-service-for-aws-s3-buckets) section of the main guide satisfies controls SC-8, 12, 12(1), 13, 28, and 28(1). 

# SI System and Information Integrity
The System and Information Integrity (SI) control provides guidelines for ensuring the integrity of system information. Essentially, it aims to protect against unauthorized changes to information within a system and ensures that systems operate correctly and securely. For S3 Buckets here are the controls that apply:
- SI-4(2),(5),(12),(20)
- SI-7
- SI-7(1),(2),(5),(7)
- SI-11
- SI-12
 NIST 800-53 SI-4(2),(5),(12),(20), read respectfully:
> - Employ automated tools and mechanisms to support near real-time analysis of events.
> - Alert when the system-generated indications of compromise or potential compromise occur
> - Alert using automated mechanisms when the indications of inappropriate or unusual activities with security or privacy implications occur
> - Implement the following additional monitoring of privileged users.

These controls focus on continuous monitoring of security controls and operational status in information systems including both real-time and periodic monitoring activities to detect and respond to security incidents. Activities like security status monitoring, monitoring security controls, system events, and security-related information to maintain situational awareness and promptly address emerging threats or vulnerabilities.

NIST 800-53 SI-7,(1),(2),(5),(7) read respectfully:
> - Employ integrity verification tools to detect unauthorized changes to the following software, firmware, and information
> - Perform an integrity check
> - Employ automated tools that provide notification to defined personnel upon discovering discrepancies during integrity verification.
> - Automatically shut the system down; restart the system
> - Incorporate the detection of unauthorized changes into the organizational incident response capability

These controls focus on ensuring the effectiveness of security controls within an information system making sure that security controls are implemented correctly, operate as intended, and provide the necessary protection against security threats

The ["Turn On Server Access Logging"](README.md#turn-on-server-access-logging) and ["Implementing CloudTrail Logging"](README.md#implementing-cloudtrail-logging) sections of the main guide satisfy these controls above. 

<p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><a property="dct:title" rel="cc:attributionURL" href="https://securing-s3-buckets.github.io/s3-security/">Securing S3 Buckets</a> by <span property="cc:attributionName">Matt Estabrook, Mark Magno, and Grace Evah</span> is licensed under <a href="https://creativecommons.org/licenses/by-sa/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">Creative Commons Attribution-ShareAlike 4.0 International<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/sa.svg?ref=chooser-v1" alt=""></a></p>
