---
toc: true
toc_label: "Table of Contents"
toc_icon: "cog"
toc_sticky: true
---

# Mapping of SAFECode Practices for Secure Software Development (Draft)

[Fundamental Practices for Secure Software Development](https://safecode.org/wp-content/uploads/2018/03/SAFECode_Fundamental_Practices_for_Secure_Software_Development_March_2018.pdf)

## Application Security Control Definition

TBD

### Actively Manage Application Security Controls

TBD

## Design

### Secure Design Principles

See [{{site.TITLE_IMPL_PRINCIPLES}}]({{site.URL_IMPL_PRINCIPLES}}).

### Threat Modeling

See [{{site.TITLE_SSDLC_SECDEV_SECDESIGN}}]({{site.URL_SSDLC_SECDEV_SECDESIGN}}).

### Develop an Encryption Strategy

See [{{site.TITLE_IMPL_DATASEC}}]({{site.URL_IMPL_DATASEC}}).

### Standardize Identity and Access Management

Implicitly covered:

* As implementation requirements: [{{site.TITLE_IMPL_AUTHZ}}]({{site.URL_IMPL_AUTHZ}})
* As to use standardized technologies in general: [{{site.TITLE_SSDLC_SECDEV_SECDESIGN}}]({{site.URL_SSDLC_SECDEV_SECDESIGN}}).

### Establish Log Requirements and Audit Practices

* Log Requirements: [{{site.TITLE_IMPL_ERRORLOG}}]({{site.URL_IMPL_ERRORLOG}})
* Audit Practices: [{{site.TITLE_SSDLC_SECOP_MONITORING}}]({{site.URL_SSDLC_SECOP_MONITORING}})

## Secure Coding Practices 

Not explicitly covered.

### Establish Coding Standards and Conventions

Not explicitly covered.

### Use Safe Functions Only

Covered in [{{site.TITLE_SSDLC_SECDEV_SECDESIGN}}]({{site.URL_SSDLC_SECDEV_SECDESIGN}}).

### Use Code Analysis Tools to Find Security Issues Early

Covered in [{{site.TITLE_IMPL_SECRETS}}]({{site.URL_IMPL_SECRETS}}).

### Handle Data Safely

Covered in [{{site.TITLE_IMPL_DATASEC}}]({{site.URL_IMPL_DATASEC}}).

### Handle Errors

Covered in [{{site.TITLE_IMPL_ERRORLOG}}]({{site.URL_IMPL_ERRORLOG}}).

## Manage Security Risk Inherent in the Use of Third-party Components 

## Testing and Validation

Covered in [{{site.TITLE_IMPL_ERRORLOG}}]({{site.URL_IMPL_ERRORLOG}}).

### Automated Testing

Covered in [{{site.TITLE_SSDLC_SECTESTS_SECSCANS}}]({{site.URL_SSDLC_SECTESTS_SECSCANS}}).

### Manual Testing

Abuse case testing is covered in [{{site.TITLE_SSDLC_SECTESTS_CUSTOMTESTS}}]({{site.URL_SSDLC_SECTESTS_CUSTOMTESTS}}).

## Manage Security Findings

Covered in [{{site.TITLE_SSDLC_SECTESTS_DEFECTH}}]({{site.URL_SSDLC_SECTESTS_DEFECTH}}).

### Define Severity

TBD

### Risk Acceptance Process

TBD

## Vulnerability Response and Disclosure

TBD

### Define Internal and External Policies

TBD

### Define Roles and Responsibilities

Covered in [{{site.TITLE_GENERAL_ROLES}}]({{site.URL_GENERAL_ROLES}}).

### Ensure that Vulnerability Reporters Know Whom to Contact

Not covered.

### Manage Vulnerability Reporters

Not covered.

### Monitor and Manage Third-party Component Vulnerabilities

Covered in [{{site.TITLE_SSDLC_SECDEV_3RDPARTY}}]({{site.URL_SSDLC_SECDEV_3RDPARTY}}).

### Fix the Vulnerability

Covered in [{{site.TITLE_SSDLC_SECOP_VULNREMED}}]({{site.URL_SSDLC_SECOP_VULNREMED}}) and [{{site.TITLE_SSDLC_SECTESTS_DEFECTH}}]({{site.URL_SSDLC_SECTESTS_DEFECTH}}).

### Vulnerability Disclosure

TBD

### Secure Development Lifecycle Feedback

## Planning the Implementation and Deployment of Secure Development Practices

Covered in [{{site.TITLE_SSDLC_SECDEV_SECIMP}}]({{site.URL_SSDLC_SECDEV_SECIMP}}).

### Culture of the Organization

Not in scope.

### Expertise and Skill Level of the Organization

Not in scope.

### Product Development Model and Lifecycle

Covered in [{{site.TITLE_SSDLC_SECDEV}}]({{site.URL_SSDLC_SECDEV}}).

### Scope of Initial Deployment

Not in scope.

### Stakeholder Management and Communications

Not in scope.

### Compliance Measurement

Not in scope.

### SDL Process Health

Not in scope.

### Value Proposition

Not in scope.