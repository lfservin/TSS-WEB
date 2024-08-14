---
toc: false
toc_label: "Table of Contents"
toc_icon: "cog"
toc_sticky: true
---

# NIST SSDF Mapping (Draft)

## Prepare the Organization (PO)

### Define Security Requirements for Software Development (PO.1)

This is what should be archived by applying TSS-WEB in general.

### Implement Roles and Responsibilities (PO.2)

See [{{site.TITLE_SSDLC_SECDEV_ROLES}}]({{site.URL_SSDLC_SECDEV_ROLES}}).

### Implement Supporting Toolchains (PO.3)

Covered from a requirement perspective mostly at [{{site.TITLE_SSDLC_SECDEV_BUILD}}]({{site.URL_SSDLC_SECDEV_BUILD}}). However, this SSDF requirements also focussed on the general process of selecting and implementing the right tooling which is not covered by TSS-WEB.

### Define and Use Criteria for Software Security Checks (PO.4)

Covered from a requirement perspective mostly at [{{site.TITLE_SSDLC_SECDEV_BUILD}}]({{site.URL_SSDLC_SECDEV_BUILD}}) as wel as [{{site.TITLE_SSDLC_SECDEV_3RDPARTY}}]({{site.URL_SSDLC_SECDEV_3RDPARTY}}).

### Implement and Maintain Secure Environments for Software Development (PO.5)

See [{{site.TITLE_SSDLC_SECENV}}]({{site.URL_SSDLC_SECENV}}).

## Protect the Software (PS)

### Protect All Forms of Code from Unauthorized Access and Tampering (PS.1)

Covered by various requirements, including:

* [{{site.TITLE_SSDLC_SECENV_ACCESS}}]({{site.URL_SSDLC_SECENV_ACCESS}})
* [{{site.TITLE_SSDLC_SECENV_CODEPROTECT}}]({{site.URL_SSDLC_SECENV_CODEPROTECT}})
* [{{site.TITLE_SSDLC_SECOP_SEPERATION}}]({{site.URL_SSDLC_SECOPP_SEPERATION}})
* [{{site.TITLE_SSDLC_SECOP_SECBACKEND}}]({{site.URL_SSDLC_SECOPP_SECBACKEND}})
* [{{site.TITLE_SSDLC_SECOP_ADMINACCESS}}]({{site.URL_SSDLC_SECOPP_ADMINACCESS}})
* [{{site.TITLE_IMPL_SECRETS}}]({{site.URL_IMPL_SECRETS}})
  
### Provide a Mechanism for Verifying Software Release Integrity (PS.2)

### Archive and Protect Each Software Release (PS.3)

## Produce Well-Secured Software (PW)

### Design Software to Meet Security Requirements and Mitigate Security Risks (PW.1)

### Review the Software Design to Verify Compliance with Security Requirements and Risk Information (PW.2)

### Reuse Existing, Well-Secured Software When Feasible Instead of Duplicating Functionality (PW.4)

### Create Source Code by Adhering to Secure Coding Practices (PW.5)

### Configure the Compilation, Interpreter, and Build Processes to Improve Executable Security (PW.6)

### Review and/or Analyze Human-Readable Code to Identify Vulnerabilities and Verify Compliance with Security Requirements (PW.7)

### Test Executable Code to Identify Vulnerabilities and Verify Compliance with Security Requirements (PW.8)

### Configure Software to Have Secure Settings by Default (PW.9)

## Respond to Vulnerabilities (RV)

### Identify and Confirm Vulnerabilities on an Ongoing Basis (RV.1)

### Assess, Prioritize, and Remediate Vulnerabilities (RV.2)

### Analyze Vulnerabilities to Identify Their Root Causes (RV.3)
