# 5. Security within the SDLC

## 5.1 Roles & Training
1. Every development team MUST be responsible for security of the code it develops
2. Every development team CAN have to appoint a security champion (see 1.4 Roles) and a deputy. One person can fill this role for multiple teams.
3. Every team member MUST receive general awareness and role-specific security training (e.g. secure coding training and training of secure design principles for developers).

## 5.2 Secure By Design
1. Security MUST be taken into account strongly during design phase. Wherever possible, security requireme nts SHOULD be addressed on architecture instead of code layer.
2. For applications with assurance class >= [HIGH], a security architecture MUST be documented that describes relevant security aspects, security controls a threat model of the application. 
3. High-level application security objectives MUST also be mapped to functional requirements. 
4. Decisions with severe security implications MUST be regularly questioned and discussed within the team.

## 5.3 Security within Change Management & Agile Development
1. All changes of source code MUST be committed to a source code repository (e.g. Git).
2. For applications with assurance class >= [HIGH], all commits on protected branches MUST be reviewed by a second developer (e.g. via pull or merge requests).
3. Assessment of all functional requirements and changes (e.g. User Stories) in respect of potential security risks / impact (= “security-relevance”)[^1] MUST be conducted by the team before their implementation.
   - This assessment MAY be conducted informally by a team if it gained sufficient experience.
   - Teams MAY define own criteria for security-relevance.
   - Agile development teams SHOULD integrate corresponding criteria in their Definition of Ready (DoR) and discuss security-relevance in refinement meetings and take security efforts (e.g. for verification) into account for estimation of story.
   - For assurance class >= [HIGH]: If such an assessment is not conducted, a deployed application increment MUST be considered to have a potential high-security risk.
   - Threat models and assurance class MUST be reviewed and updated if affected (e.g. in case of changes of security controls or architectural change in general).
   - A suitable acceptance criteria (e.g. review by security champion, update of security documentation) MUST be defined for all security-relevant requirements and changes. Agile development teams SHOULD integrate corresponding criteria in their Definition of Done (DoD).

## 5.4 Secure Build & Deployment
1. A formal definition of the build & deployment process MUST be created so that it becomes consistent, repeatable and automated.
2. Access to build and deployment systems MUST be secured according to requirements in in 4. Secure Development Environment.
3. Automated security checks MUST be integrated into build & deployment processes in accordance to requirements in 6. Security Tests.
4. Secrets SHOULD be injected during deployment process in accordance to requirements in 8.11 Protection of Secrets.
5. Deployment pipelines SHOULD implement a pull-based model[^3].
6. For assurance class >= [HIGH], integrity of deployed artifacts MUST be automatically verified (e.g. using digital signatures).
7. For assurance class >= [HIGH], executed scripts in build systems SHOULD be authorized and whitelisted.

## 5.5 Security of 3rd Party Dependencies in Target Production Environment
1. 3rd party dependencies SHOULD only be obtained via internal and approved repositories.
2. Before a new 3rd party dependency is allowed to be used in productive applications (or within the release build environment), it MUST be approved by the architecture board. This does not affect new releases of a dependency that has already been approved.
3. 3rd party dependencies SHOULD be updated regularly.
4. 3rd party dependencies MUST be updated in case of relevant critical security vulnerabilities or end of life.
5. A Software Bill of Materials (SBOM) that keeps a record of all 3rd party dependencies MUST be created for all released artifacts
6. The SBOM SHOULD be signed
7. Testing requirements for custom and 3rd party code are defined at 6. Security Tests.

## 5.6 Security Approvals (Security Gates)
1. Initial Project approval (mandatory): All new projects that are either implementing new applications or that plan to change existing ones MUST be approved by the relevant IT security function before they are allowed to be started. As part of this approval, the relevant IT security function will specify the assurance class with the project and may define security controls that have to be implemented or security activities that have to be conducted by the project.
2. Architecture approval (conditional): For all new applications with assurance class >= [HIGH], or if explicitly requested by the IT security function during the project approval, the solution architecture (including security architecture that describes security controls & aspects and a threat model describing relevant threats and mitigations for them) MUST be approved by the relevant IT security function before initial implementation is allowed to begin. The IT security function MAY request this approval to be renewed for architectural changes when certain criteria are met.
3. Go-Live approval (conditional): Initial application releases for applications with assurance class >= [HIGH] MUST pass a security sign-off by the relevant IT security function before they are allowed to be used in the target production environment. The relevant IT security function MAY decide within the project approval as well that this approval is required for subsequent releases (e.g. based on certain criteria) or for projects with a lower assurance class.
4. All security approvals and risks management decisions must be documented.

## 5.7 Remediation of Security Findings
Remediation of security findings with a criticality >= [HIGH] (or CVSS[^2] v3 Score >= 7.0) MUST be sufficiently mitigates before a new application release is allowed to go-live:

1. In case this is not possible, the relevant risk MUST be accepted by the respective management function (e.g. project lead). For applications with assurance class >= [HIGH], this risk acceptance MUST be formally documented (e.g. as Jira ticket).
2. In addition, security findings with criticality >= [MEDIUM] (or CVSS v3 Score >= 5.0) SHOULD NOT go-live without proper verification.
3. Teams MAY reassess tool findings. For instance, they may refine a CVSS Base Score by evaluating its CVSS Environmental Score and thereby taken aspects like its classification or accessibility into account. When a rating/score is refined the respected reason (e.g. CVSS vector) MUST be documented.
4. Identified vulnerabilities MUST be retested after remediation to verify that countermeasures has been implemented correctly.
5. For assurance class >= [HIGH]: Exceptions (such as temporary workarounds) MUST be approved by the IT security function.

## 5.8 Security Documentation

1. A comprehensive security documentation MUST exist and formally be approved by the relevant IT security function for every application with assurance class >= [HIGH] before its implementation starts (relevant aspects) and it’s allowed to initially go-live (complete documentation).
2. In case the relevant IT security function has not requested it differently, this document SHOULD cover the following aspects:
   - Data and application classification (assurance class),
   - application security architecture (relevant application components, interfaces and relevant data flows and architectural security controls in the form of a diagram),
   - network/cloud security architecture,
   - list of relevant security requirements (e.g. security standards or business  security requirements),
   - known threats and respective countermeasures to mitigate them,
   - role and authorization concept (required for go-live),
   - data handling that describes what data handles where and how (required for go-live),
   - operational security controls (required for go-live).

[^1]: SAFECode defines a good security indicator here, by describing security-relevant changes as “Any additions or changes in security controls and functionality”: (1) Authentication (Adding or changing an authentication method, or mechanism), (2) Authorization (Shifting the trust relationships between any components or actors in the system (change of user levels, change of data access permissions, etc or adding or changing an authorization method, or mechanism), (3) Logging, monitoring and alerting (Adding or changing application monitoring, business analytics and insight, auditing and compliance requirements or forensics) or (3) Cryptography (Adding or changing cryptographic functionality: hashing algorithms, salt, encryption/decryption algorithms, SSL/TLS configuration, key management, etc). See SAFECode paper “Tactical Threat Modeling”: https://safecode.org/wp-content/uploads/2017/05/SAFECode_TM_Whitepaper.pdf

[^2]: CVSS = Common Vulnerability Scoring System (CVSS) v3, https://www.first.org/cvss

[^3]: See https://www.weave.works/blog/why-is-a-pull-vs-a-push-pipeline-important