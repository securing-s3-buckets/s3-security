# NIST Control Mappings
If you are curious about which NIST 800-53 controls are satisfied by the instructions in the [main guide](README.md), see each control family below. 

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
