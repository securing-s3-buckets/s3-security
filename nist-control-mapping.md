# NIST Control Mappings
If you are curious about which NIST 800-53 controls are satisfied by the instructions in the [main guide](README.md), see each control family below. 

# CA Assessment Authorization and Monitoring
The CA family of controls deals with assessing the environment and access, authorizing access, and monitoring. The applicable control for S3 buckets is below: 
- CA-9

NIST 800-53 control CA-9 reads: 
> Authorize internal connections of [organization-defined system components or classes of components] to the system;

The "Protecting S3 Buckets by Limiting Public Access" section of the guide satisfies control CA-9. 

# CM Configuration Management
The CM family of controls deals with managing the configuration of information systems. For S3 buckets, the below control is applicable: 
- CM-5

NIST 800-53 control CM-5 reads: 
> Define, document, approve, and enforce physical and logical access restrictions associated with changes to the system.

The "Removing Overly Permissive Admin Accounts" section of the guide satisfies control CM-5. 

# IA Identification and Authentication
## IA-2 Identification and Authentication (organizational Users)
Identifying individual users and authenticating those users so that you can restrict access and assign permissions appropriately is crucial. For S3 buckets, the below controls are applicable: 
- IA-2
- IA-2(1)
- IA-2(2)

NIST 800-53 control IA-2 reads: 
> Uniquely identify and authenticate organizational users and associate that unique identification with processes acting on behalf of those users.

The "Implementing Authentication for S3 Users" section of the guide satisfies control IA-2. 

NIST 800-53 IA-2(1) reads: 
> Implement multi-factor authentication for access to privileged accounts.

And IA-2(2) reads: 
> Implement multi-factor authentication for access to privileged accounts.

The "Implementing Multi-factor Authentication on AWS Accounts" section of the guide satisfies controls IA-2(1) and IA-2(2). 

## AC Access Control
The AC Control Family consists of security requirements detailing system logging. The applicable control for S3 buckets is below: 
- AC-2(12)
- AC-22

AC-(12) Reads as:
> Monitor system accounts for [Assignment: organization-defined atypical usage]; and Report atypical usage of system accounts to [Assignment: organization-defined personnel or roles].

This control is covered later by CloudFlare and System Access logging. This information can be found in the next section of Audit and Accountability

AC-22 Reads as:
> Designate individuals authorized to make information publicly accessible; Train authorized individuals to ensure that publicly accessible information does not contain nonpublic information; Review the proposed content of information prior to posting onto the publicly accessible system to ensure that nonpublic information is not included; and Review the content on the publicly accessible system for nonpublic information [Assignment: organization-defined frequency] and remove such information, if discovered.

This can be acheived by simply allowing public access to specifc buckets.

<p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><a property="dct:title" rel="cc:attributionURL" href="https://securing-s3-buckets.github.io/s3-security/">Securing S3 Buckets</a> by <span property="cc:attributionName">Matt Estabrook, Mark Magno, and Grace Evah</span> is licensed under <a href="https://creativecommons.org/licenses/by-sa/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">Creative Commons Attribution-ShareAlike 4.0 International<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/sa.svg?ref=chooser-v1" alt=""></a></p>
