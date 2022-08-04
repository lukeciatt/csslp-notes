[Buy CSSLP CBK](https://www.amazon.com/Official-ISC-Guide-CSSLP-Press-ebook-dp-B00EYLMBHQ/dp/B00EYLMBHQ/ref=mt_other?_encoding=UTF8&me=&qid=)

# Acronyms & General Concepts
## Core Security:
CIA Triad
- Confidentiality: how the system prevents the disclosure of information. Mainly focused on software encryption and data storage. Cryptography and Masking. TLS, etc.
- Integrity: how the system protects data from unauthorized access. Checksums, CRCs, Message Digests, MACs, etc. Code Injection or Input Validation affect the integrity of the backend data.
- Availability: The system must always remain accessible for authorized personnel.
	- MTD (Maximum Tolerable Downtime)
	- RTO (Recovery Time Objective)
	- RPO (Recovery Point Objective)
	- SLAs
	- MTBF (Mean Time Between Failure)
	- MTTR (Mean Time To Repair)
  
---

IAAA 
- Identification: is the “who are you?” stage and could be any of the following: Name, username, ID, employee number etc.
- Authentication: process of determining the identity of a user. Four methods can be used to authenticate a user:
	- Knowledge Based Authentication: Something you know (ex: password, pin code).
	- Ownership Based Authentication: Something you have (ex: token, card).
	- Characteristic Based Authentication: Something you are (ex: biometrics mechanisms).
	- Something you do, such as a mandatory action to complete authentication.
- Authorisation: is the process of specifying user access rights and privileges using access control models such as DAC (Discretionary Access Control) , MAC (Mandatory Access Control) and RBAC (Role-based Access Control).
- Accountability (also known as Auditability):  Prove what someone did, and when they did it. Known as non-repudiation. (Log everything. "Tracing an action to a subject"). Must include the following: 
	- Identity of subject 
	- The Action 
	- Object on which the action was performed 
	- Timestamp 
  
PNE (Protection Needs Elicitation): Gathering information from the client in order to build the software requirements.

IMM (Information Management Model)

IPP (Information Protection Profile)

Polyinstatiation: Lies. For example, if someone without access read a classified document then this document will show false information instead of the real one. The sensitive information it will be displayed just to authorized users.

MSB (Minimum Security Baseline)

CMDB (Change Management Database)

PII (Personally Identifiable Information)
PHI (Personal Health Information)
PFI (Personal Financial Information)

DRM (Digital Rights Management): gives copyright owners control over access and use of the copyright protected material.

CDI (Constrained Data Item): Restricted element in Clark-Wilson, what we hide behind the controlled environment we give to the user.

IVP (Integrity Verification Procedure): To ensure that the CDIs remain unaltered by users in a bad way.

Implicit Deny: Is when a user or group are not granted a specific permission in the security settings of an object, but they are not explicitly denied either.

ERM (Enterprise Risk Management)

V&V (Verification and Validation): The Capability Maturity Model (CMM) for Software defines (V&V) as the following:
- Verification: ensures that the software performs as required and expected to (Review phase).
- Validation: ensures that the software meets required specifications (Testing Phase).

Clipping level: e pre-determined number of acceptable user errors before recording the error as a potential security incident. (Ex: Login attempts)

SLA (Service Level Agreements): defines the level of service you expect from a vendor, laying out the metrics by which service is measured, as well as remedies or penalties should agreed-on service levels not be achieved.

BCP (Business Continuity Planning): It has  7 phases:
- Initiate project
- Perform BIA
- Create strategy
- Create plan
- Implement plan
- Test plan
- Maintain plan

DRP (Disaster Recovery Plan)

In short, a DRP is the strategy and actions to follow to restore IT services in the event of any eventuality in a very short time and without loss of information.
4 Types of Disaster Recovery Plans:
- Data Center Disaster Recovery (When using own servers)
- Cloud-Based Disaster Recovery (When using cloud servers like AWS, Google Cloud, etc.)
- Virtualization Disaster Recovery (When using VMs)
- Disaster Recovery as a Service (Cloud oriented)

BIA (Business Impact Analysis): Process of analyzing the impact over time of a disruption on the organization

ISSE (Information Systems Security Engineer/Engineering)

# Basics
### System Principles
- Session management – design and implementation of controls to ensure that the communications channels are secured from unauthorized access and disruption of communications.
- Exception management – the process of handling any errors that could appear during the system execution.
- Configuration management – identification and management of the configuration items (initialization parameters, connection strings, paths, keys).

### Secure Design Principles
How Much Security is enough? 
Always perform a Risk Analysis, because it does not make sense to spend 10 million dollars in security in an asset that is not important. So the security depends on the risk and importance of the asset, the phrase "there is never enough security" in this case is totally false, there is enough security, depending on the value of the asset.

- **Good enough security** – there is a trade-off between security and other aspects associated with a system. The level of required security must be determined at design time.
- **Least privilege** – a subject should have only the necessary rights and privileges to perform a specific task.
- **Separation of duties (or) Compartmentalization Principle** – for any given task, more than one individual needs to be involved.
- **Defense in depth (layered security)** – single points of complete compromise are eliminated or mitigated by the incorporation of a series or multiple layers of security safeguards and risk-mitigation countermeasures.
- **Fail Secure** – when a system experiences a failure, it should fail to a safe state; all the attributes associated with the system security (confidentiality, integrity, availability) should be appropriately maintained.
- **Economy of mechanism** – keep the design of the system simple and less complex; reduce the number of dependencies and/or services that the system needs in order to operate. K.I.S.S (Keep It Simple, Silly)
- **Complete mediation** – checking permission each time a subject requests access to objects. A measure that can't be bypassed or circumvented.
- **Open design** – design is not a secret, the implementation of the safeguard is (ex: cryptography algorithms are open but the keys used are secret). "Producing a security mechanism in which its strength is independent of its design".
- **Least common mechanism** – disallows the sharing of mechanisms that are common to more than one user or process if the users and processes are at different levels of privilege. For example, the use of the same function to retrieve the bonus amount of an exempt employee and a non-exempt employee will not be allowed. In this case the calculation of the bonus is the common mechanism.
- **Psychological acceptability** – accessibility to resources should not be inhibited by security mechanisms. If security mechanisms hinder the usability or accessibility of resources, then users may opt to turn off those mechanisms.
- **Weakest link** – attackers are more likely to attack a weak spot in a software system than to penetrate a heavily fortified component.
- **Leverage existing components** – focuses on ensuring that the attack surface is not increased and no new vulnerabilities are introduced by promoting the reuse of existing software components, code and functionality.
- **Single point of failure** – a system design should not be susceptible to a single point of failure.
- **Dual Control** - process that uses two or more separate entities (usually persons) operating in concert to protect sensitive functions or information.

# Risk Management

Vocabulary

- **Risk** – possibility of suffering harm or loss.
- **Residual risk** – risk that remains after a control was added to mitigate the initial risk.
- **Total risk** – the sum of all risks associated with an asset.
- **Asset** – resource an organization needs to conduct business.
- **Threat** – circumstance or event with the potential to cause harm to an asset.
- **Threat Source / Agent** - anyone or anything that has the potential to make a threat materialize.
- **Probability / Likehood** - is the chance that a particular threat can happen.
- **Vulnerability** – any characteristic of an asset that can be exploited by a threat to cause harm.
- **Attack** – attempting to use a vulnerability.
- **Impact** – loss resulting when a threat exploits a vulnerability.
- **Mitigate** – action taken to reduce the likelihood of a threat.
- **Control** – a measure taken to detect, prevent, or mitigate the risk associated with a threat.
- **Risk assessment** – process of identifying risks and mitigating actions.
- **Qualitative risk assessment** – subjectively determining the impact of an event that affects assets.

### Quantitative risk assessment

Objectively determining the impact of an event that affects assets.

**Single Loss Expectancy (SLE)** - Single Loss Expectancy (SLE) is used to estimate potential loss. It is calculated as the product of the value of the asset (usually expressed monetarily) and the exposure factor, which is expressed as a percentage of asset loss when a threat is materialized.

SLE = Asset Value ($) x Exposure Factor (%)

- **Asset Value (AV):** Dollar figure that represents what the asset is worth to the organization.
- **Exposure Factor (EF):** The opportunity (in %) for a threat to cause loss.

**Annual Rate of Occurrence (ARO)** - is an expression of the number of incidents from a particular threat that can be expected in a year.
ARO = number of events/number of years

**Annual Loss Expectancy (ALE)** - Annual Loss Expectancy (ALE) is an indicator of the magnitude of risk in a year.
ALE = Single Loss Expectancy (SLE) x Annualized Rate of Occurrence (ARO)

![Simple Quantitative Risk Calculation](https://github.com/lukeciatt/csslp-notes/blob/main/Images/risk.jpg)

**ROI (Return on investment)**
ROI (%) = (Avoided Loss – Control Cost) / (Control Cost) * 100
ROI (Time) = (Avoided Annual Loss) / (Annual Control Cost)

## Risk Management Models
General Risk Management Model

The steps contained in a general risk management model:

1. **Asset identification** – identify and clarify all the assets, systems, and processes that need to be protected.
2. **Threat assessment** – identify the threats and vulnerabilities associated with each asset.
3. **Impact determination and qualification.**
4. **Control design and evaluation** – determine which controls to put in place to mitigate the risks.
5. **Residual risk management** – evaluate residual risks to identify where additional controls are needed.

### Risk Management Model Proposed by Software Engineering Institute

[SEI](http://www.sei.cmu.edu/) model steps :

1. **Identity** – enumerate potential risks.
2. **Analyze** – convert the risk data gathered into information that can be used to make decisions.
3. **Plan** – decide the actions to take to mitigate them.
4. **Track** – monitor the risks and mitigations plans.
5. **Control** – make corrections for deviations from the risk mitigation plan.

### Risk Mitigation

- **Reduce / Mitigate:** Mitigation does not always mean lowering a risk to 0, but rather lowering the risk to a level that is acceptable to the company's management level.
- **Accept:** Accept the risk without solving it but this is documented and recorded, even with the excuse of why the risk was accepted (almost always because the cost of mitigating it was higher than the cost of the asset itself).
- **Transfer:** Sharing the risk. Common ways to transfer the risk are by buying insurance and using disclaimers.
- **Avoidance:** This can be done by, for example, discontinuing the feature that contains the risk.
- **Ignore / Rejection:** Ignore the risk totally. The risk is left unhandled.

# Security Standards
![Security Standards](https://github.com/lukeciatt/csslp-notes/blob/main/Images/security_standards.PNG)

## COBIT (Control Objectives for Information and Related Technology) - From ISACA
The COBIT framework was created by ISACA to bridge the crucial gap between technical issues, business risks and control requirements.
Is a framework that aims to help organizations that are looking to develop, implement, monitor, and **improve IT governance and information management**.

COBIT 5 principles

- Principle 1: Meeting stakeholder needs.
- Principle 2: Covering the enterprise end to end.
- Principle 3: Applying a single integrated framework.
- Principle 4: Enabling a holistic approach.
- Principle 5: Separating governance from management.

## COSO (Committee of Sponsoring Organizations of the Treadway Commission)
**A 360° view to manage risk.**
It was designed to identify, assess and manage risks; to give an overview of the threats to which a company is exposed; to broaden the concept of internal control; and to provide a clear direction for the business.
The first version of COSO was published in 1992 and, since then, the document has become a reference for risk managers, boards of directors and managers of organizations around the world. By providing a 360° view of the risks that could affect the company, this framework provides a guideline for action plans for proper risk management.

There is also the COSO ERM or also known as COSO II which provides even more risk coverage.

![Frameworks Order](https://github.com/lukeciatt/csslp-notes/blob/main/Images/frameworks_order.jpg)

## ITIL (Information Technology Infrastructure Library) 
Is a set of practices for IT activities such as IT service management (ITSM) and IT asset management (ITAM) that focus on aligning IT services with the needs of business.

![ITIL Framework](https://github.com/lukeciatt/csslp-notes/blob/main/Images/itil.jpeg)

## SABSA (Sherwood Applied Business Security Architecture) 
Framework and methodology for developing risk-driven enterprise information security architecture.

### SABSA LifeCycle

![SABSA LifeCycle](https://github.com/lukeciatt/csslp-notes/blob/main/Images/sabsa.png)

## SEI CMMI (Capability Maturity Model Integration)
Process metric model that rates the **process maturity** of an organization on a 1 to 5 scale.
1. Initial (Level 1)
2. Repeatable (Level 2)
3. Defined (Level 3)
4. Managed Quantitatively (Level 4)
5. Optimizing (Level 5)

## NIST CSF

![NIST CSF](https://github.com/lukeciatt/csslp-notes/blob/main/Images/nist.jpg)

# Security Assessment Methodology

## OCTAVE (Operationally Critical Threat, Asset, and Vulnerability Evaluation) 

Suite of tools, techniques, and methods for risk-based information security assessment.

The 3 phases of OCTAVE are:
-     Phase 1: Develop initial security strategies / Build Asset-Based Threat Profile:
	- In this phase, the analysis team determines what information-related assets are important to the organization and how they are currently being protected.

-     Phase 2: Identify infrastructure vulnerabilities
	- The goal of this phase is to identify important infrastructure vulnerabilities as well as develop policies and practices that will address these vulnerabilities.

-     Phase 3: Risk analysis — Develop security strategy and plans
	- In this phase, you will create a prioritized list of risks which will then be translated to an overarching security risk management strategy, to be used on a continual basis.
	
## FRAP (Facilitated Risk Analysis Process) Framework

Aims to get **conclusions** about risks **quicker**. Is a **qualitative approach**, using **brainstorming techniques**.
Basically a subjective (qualitative) analysis is done on something to determine whether or not it is worthwhile to move forward with a more quantitative analysis.

## CRAMM (CCTA Risk Analysis and Management Method)

A Qualitative Risk Analysis and Management Tool (Similar to FRAP).

CRAMM has 3 stages:
- **Asset identification and valuation.**  The goal here is to identify and value assets.
- **Threat and vulnerability assessment.**  The goal here is to assess the CIA risks to assets. 
- **Countermeasure selection and recommendation.**  The goal here is to identify the changes required to manage the CIA risks identified.

Is like a Threat Model but instead of focusing on STRIDE it focuses on the CIA Triad.

## NIST Standards

- SP 800-12: An Introduction to Computer Security: The NIST Handbook
- SP 800-14: Generally Accepted Principles and Practices for Security IT Systems
- SP 800-18: Guide for developing Security Plans for Federal Systems
- SP 800-27: Engineering Principles for Information Technology Security
- SP 800-61 – Computer Security Incident Handling Guide
- SP 800-64: Security Considerations in the Information Systems Development Life Cycle
- SP 800-100: Information Security Handbook: A Guide for Managers

### NIST SP 800-30: Risk Management Guide for IT
The NIST SP 800 30 provides guidance for conducting risk assessments of information systems and organizations. It further amplifies the guidance in SP 800-39.

![NIST SP 800-30](https://github.com/lukeciatt/csslp-notes/blob/main/Images/NIST-SP-800-30.png)

## FIPS (Federal Information Processing Standards)

Developed by NIST
FIPS publications are developed to address Federal requirements for:
- Interoperability of disparate systems
- Portability of data and software
- Computer security

Some of the well-known FIPS publications that are closely related to software security are:
- FIPS 140: Security Requirement for Cryptographic Modules
- FIPS 186: Digital Signature Standard
- FIPS 197: Advanced Encryption Standard
- FIPS 201: Personal Identity Verification (PIV) of Federal Employees and Contractors

Common ISO standards

ISO/IEC

| ISO | Description |
| ----------- | ----------- |
| 9126  | Software Engineering Product Quality. Multipart series standard. |
| 10746  | Information Technology – Open distributed processing. Multipart series standard. |
| 12207 | Systems and Software Engineering – Software lifecycle processes. |
| 14143  | Information Technology – Software measurement – Functional size measurement. Multipart series standard. |
| 15026 | Systems and Software Assurance. Multipart series standard. |
| 15288 | Systems and Software Engineering – System lifecycle processes. |
| 15408 | Evaluating Criteria for IS Security (Common Criteria). |
| 21827 | Information Technology – Security techniques – Systems security engineering – Capability Maturity Model (SSE-CMM). |
| 27001 | Information Security Management System (ISMS) Overview and Vocabulary. |
| 27002 | Code of Practice for Information Security Management. |
| 27003 | Information Security Management System Implementation Guidance. |
| 27004 | Information Security Management – Measurement. |
| 27005 | Information Security Risk Management. |

## Intellectual Property

Intellectual property is protected by the U.S. law under one of four classifications:

- **Patents** – Right to use, make, or sell an invention (idea) for a period of time in exchange for the patent holder’s making the invention public.
- **Trademarks** – Trademarks are associated with marketing: the purpose is to allow for the creation of a brand that distinguishes the source of products or services.
- **Copyrights** – represents a type of intellectual property that protects the form of expression in artistic, musical, or literary works, and is typically denoted by the [circle c symbol](http://en.wikipedia.org/wiki/Copyright_symbol). Software is typically covered by copyright law as if it were a literary work. Two important limitations on the exclusivity of the copyright holder’s monopoly exist: the doctrines of first sale and fair use.
- **Trade secrets** – business-proprietary information that is important to an organization’s ability to compete. Software source code or firmware code are examples of computer-related objects that an organization may protect as trade secrets.

## Privacy and Data Protection Laws

Privacy and data protection laws are enacted to protect information collected and maintained on individuals from unauthorized disclosure or misuse.

Several important pieces of privacy and data protection legislation include:

- **U.S. Federal Privacy Act of 1974** – protects records and information maintained by U.S. government agencies about U.S. citizens and lawful permanent residents.
- **U.S. Health Insurance Portability and Accountability Act (HIPAA) of 1996** – seeks to guard protected health information against unauthorized use or disclosure.
- **Payment Card Industry Data Security Standard (PCI-DSS)** – the goal is to ensure better protection of cardholder data through mandating security policy, security devices, control techniques, and monitoring of systems and networks.
- **U.S. Gramm-Lech-Bliley Financial Services Modernization Act (GLBA)** – requires financial institutions to protect the confidentiality and integrity of consumer financial information.
- **U.S. Sarbanes-Oxley Act of 2002 (SOX)** – the primary goal of SOX is to ensure adequate financial disclosure and financial auditor independence.
