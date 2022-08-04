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

- **U.S. Federal [Privacy Act of 1974](http://en.wikipedia.org/wiki/Privacy_Act_of_1974)** – protects records and information maintained by U.S. government agencies about U.S. citizens and lawful permanent residents.
- **U.S. [Health Insurance Portability and Accountability Act](http://en.wikipedia.org/wiki/Health_Insurance_Portability_and_Accountability_Act) (HIPAA) of 1996** – seeks to guard protected health information against unauthorized use or disclosure.
- **Payment Card Industry Data Security Standard (PCI-DSS)** – the goal is to ensure better protection of cardholder data through mandating security policy, security devices, control techniques, and monitoring of systems and networks.
- **U.S. Gramm-Lech-Bliley [Financial Services Modernization Act](http://en.wikipedia.org/wiki/Gramm%E2%80%93Leach%E2%80%93Bliley_Act) (GLBA)** – requires financial institutions to protect the confidentiality and integrity of consumer financial information.
- **U.S. [Sarbanes-Oxley Act of 2002](http://en.wikipedia.org/wiki/Sarbanes%E2%80%93Oxley_Act) (SOX)** – the primary goal of SOX is to ensure adequate financial disclosure and financial auditor independence.

### International Safe Harbor Privacy Principles

Safe Harbour Privacy Principles prevent private organizations within the European Union or United States which store customer data from accidentally disclosing or losing personal information.
The seven principles are:
- Notice – Individuals must be informed that their data is being collected and how it will be used. The organization must provide information about how individuals can contact the organization with any inquiries or complaints.
- Choice – Individuals must have the option to opt out of the collection and forward transfer of the data to third parties.
- Onward Transfer – Transfers of data to third parties may only occur to other organizations that follow adequate data protection principles.
- Security – Reasonable efforts must be made to prevent loss of collected information.
- Data Integrity – Data must be relevant and reliable for the purpose it was collected.
- Access – Individuals must be able to access information held about them, and correct or delete it, if it is inaccurate.
- Enforcement – There must be effective means of enforcing these rules.

## Security Policies: The ‘What’ and ‘Why’ for Security

The security policy provides the framework and point of reference that can be used to measure an organization’s security posture. The gaps that are identified when being measured against a security policy, a consistent point of reference, can be used to determine effective executive strategy and decisions.

Additionally security policies ensure non-repudiation, because those who do not follow the security policy can be personally held accountable for their behavior or actions.

## Trusted Computing

Trusted computing is the set of technologies to improve computer security.

Trusted Platform Module (TPM). The TPM can hold an encryption key that is not accessible to the system
except through the TPM chip. Principles:
- Security
- Privacy
- Interoperability
- Portability of data
- Controllability
- Ease of use
The Trusted Platform Module (TPM) is an implementation of specifications detailing secure crypto storage on a chip.

When a host system is started, the sequences of events and processes that self-start the system to a preset state is referred to as **booting or bootstrapping**. 
(TPM) chip that provides heightened tamperproof data protection during startup. 

## Computer security models

### Ring Model

Current day Operating Systems (OSs) employ a security mechanism known as ring protection. Hackers use the terms ‘root’, ‘owned’, or ‘pwned’ when they successfully exploit vulnerabilities and gain the highest level privilege (such as privileges at Ring 0) in the system.
Rootkits operate by gaining Ring 0 level privileges as well.

![Ring Model](https://github.com/lukeciatt/csslp-notes/blob/main/Images/ring_model.PNG) 

Trust boundary is the abstract concept that determines the point at which trust levels change. It is also referred to as the security perimeter. There is a very clear cut trust boundary at each ring level starting with the outer most user-land ring level with low trust to the inner most kernel-land ring level that is highly privileged.

### Reference Monitor

A reference monitor is an access control methodology, an abstract machine that is used to implement security. The reference monitor's job is to validate access to objects by authorized subjects.

For a reference validation mechanism to be a reference monitor, it must possess three qualities:
- It must always be invoked and there is no path around it. This is called complete mediation.
- It must be tamper-proof.
- It must be small enough to be verifiable

### Protected Object

A protected object is one whose existence may be known but cannot be directly interacted with. Specifically, any interaction must be done through a protected subsystem.

## Trusted Computing Base

The term trusted computing base (TCB) is used to describe the combination of hardware and software components that are employed to ensure security. 

Trusted Computing Base is the abstract concept that ensures that the security policy is enforced at all times. It is an abstract concept in the sense that software architects and designers must
take into account all the hardware, software and firmware components and their mechanisms to design secure software.

The trusted computing base should not be confused with trustworthy computing or trusted computing.

# Security Models

## Access Control Models

Access controls define what actions a subject can perform on specific objects.

- **Bell-LaPadula confidentiality model** – It is focused on maintaining the confidentiality of objects. Bell-LaPadula operates by observing two rules: the Simple Security Property and the * Security Property.
	- The **Simple security property** states that there is “no read up:”  - a subject at a specific classification level cannot read an object at a higher classification level.
	- The * Security Property** is **“no write down:” - a subject at a higher classification level cannot write to a lower classification level.
- **Take-Grant**  – systems specify the rights that a subject can transfer to or from another subject or object. The model is based on the representation of the controls in forms of directed graphs with the vertices being the subjects and the objects. The edges between them represent the right between the subject and objects. The representation of rights takes the form of {t (take), g (grant), r (read), w (write)}. (Protects Confidentiality)
  
- **RBAC (Role-based Access Control)** – users are assigned a set of roles they may perform. The roles are associated with the access permissions necessary to perform the tasks.
- **RBAC (Rule-Based Access Control)** - In this form of RBAC, you’re focusing on the rules associated with the data’s access or restrictions. These rules may be parameters, such as allowing access only from certain IP addresses, denying access from certain IP addresses, or something more specific.
- **MAC (Mandatory Access Control) Model** – in MAC systems the owner or subject cannot determine whether access is to be granted to another subject; it is the job of the operating system to decide.
- **DAC (Discretionary Access Control) Model** – in DAC systems the owner of an object can decide which other subjects may have access to the object, and what specific kind of access they may have. (Windows usage, I can decide who access every file). 

![RBAC_MAC_DAC](https://github.com/lukeciatt/csslp-notes/blob/main/Images/mac_dac_rbac.jpg) 

- NDAC (Non-Discretionary Access Control) 

**Access Control List (ACLs)** is a list of permissions associated with a system resource. An ACL specifies which users or system processes are granted access to objects, as well as what operations are allowed on given objects

### Integrity Models

- **Biba Integrity Model**  – sometimes referred as Bell-LaPadula upside down, this was the first formal integrity model. Biba is the model of choice when integrity protection is vital. The Biba model has two primary rules: the Simple Integrity Axiom and the * Integrity Axiom.  (Protects Integrity)
	- The **Simple Integrity Axiom** is **“no read down:”** - a subject at a specific classification level cannot read data at a lower classification. This protects integrity by preventing bad information from moving up from lower integrity levels.
	- The * Integrity Axiom is “no write up:” - a subject at a specific classification level cannot write to data at a higher classification. This protects integrity by preventing bad information from moving up to higher integrity levels.

![Biba Integrity Model](https://github.com/lukeciatt/csslp-notes/blob/main/Images/biba.PNG) 

- **Clark-Wilson**  –  this is an informal model that protects integrity by requiring subjects to access resources via interfaces. Clark-Wilson effectively limits the capabilities of the subject. It uses two primary concepts to ensure that security policy is enforced: **well-formed transactions and Separation of Duties**.

### Information Flow Models

Information in a system must be protected when at rest, in transit, and in use.
- **The Chinese Wall model** – designed to avoid conflicts of interest by prohibiting one person, such as a consultant, from accessing multiple **Conflict of Interest Categories (CoIs)**. The Chinese Wall model requires that CoIs be identified so that once a consultant gains access to one CoI, they cannot read or write to an opposing CoI.

![Chinese_Walll](https://github.com/lukeciatt/csslp-notes/blob/main/Images/chinese_wall.png) 

## Access Control

### Types of Risks

- Business Risks:
	- Fraud
	- Regulatory
	- Treasury management
	- Revenue management
	- Contract management
- Technology Risks:
	- Security
	- Privacy
	- Change management

### Types of Controls

Controls can be classified into the types of actions they perform. Three classes of controls exist:
- Administrative
- Technical
- Physical

### Access Control Types (Important)

- **Preventative** (before-the-fact): Controls used to prevent vulnerabilities.
- **Detective** (after-the-fact): Controls used to identify undesirable events that have occurred.
- **Corrective** (after-the-fact): Controls used to correct the effects of undesirable events. (Once the attacker is inside, we try to correct the infection moving a file with malware to quarentine with the antivirus fox example.)
- **Deterrent** (before-the-fact): Controls used to discourage security violations. (Ex: Warnings signs, they don't stop you phisically, but they make you think twice before violate them)
- **Recovery** (after-the-fact): Controls used to restore resources and capabilities. (Have always backups of everything important)
- **Compensation** (after-the-fact): Controls used to provide alternative solutions.
- **Directive** (before-the-fact): An employee handbook for instance will provide directions on how to maintain compliance with security policy. (Ex: sign on a door "No entry, authorized personnel only".)

### Failure Mode Effects Analysis
Failure mode effects analysis (FMEA) is a structured methodology for the assessment of failure modes and
their effects on the system. FMEAs allow engineers to rank risks in a system.

Data Classification and Categorization


# Data states

- At rest, or being stored
- Being created
- Being transmitted from one location to another
- Being changed or deleted

![Data States](https://github.com/lukeciatt/csslp-notes/blob/main/Images/data_states.png) 

## Data usage

- Internal data - Data initialized in the application, used in an internal representation, or computed within the application itself.
- Input data - Data read into a system and possibly stored in an internal representation or used in a computation and stored.
- Output data - Data written to an output destination following processing.

**Data owners** are responsible for defining data classification, **defining** (keyword) authorized users and access criteria, defining the appropriate security controls and making sure they are implemented and operational.

**Data custodians** are responsible for maintaining defined security controls, **managing** (keyword) authorized users and access controls, and performing operational tasks such as backups and data retention and disposal.

## Data Anonymization Techniques:

1. **Replacement:** also known as substitution, is the anonymization technique in which identifiable information is substituted with non-identifiable information.
2. **Suppression:** also known as omission, identifiable information is omitted from the information being released.
3. **Generalization:** specific identifiable information is replaced using a more generalized form.
4. **Pertubation:** also known as randomization, is the anonymization technique that involves making random changes to the data.

# Software Development

## Secure Development Lifecycle Components

- **Software team awareness and education** – all team members should have appropriate training. The key element of team awareness and education is to ensure that all the members are properly equipped with the correct knowledge.
- **Gates and security requirements** – the term gates signifies a condition that one must pass through. To pass the security gate a review of the appropriate security requirements is conducted. (See below "Quality Gates").
- **Threat modeling** – design technique used to communicate information associated with a threat throughout the development team.
	- **STRIDE:** The term STRIDE refers to sources of threats: Spoofing, Tampering, Repudiation, Information disclosure, Denial of service, and Elevation of privilege.

| Threat | Mitigation |
| ----------- | ----------- |
| Spoofing (Impersonalization) | Authentication |
| Tampering  | Integrity Verification (Message Digests / CRCs) |
| Repudiation | Non-Repudiation (Digital Signatures, Keys, etc) |
| Information disclosure | Confidentiality Through Encryption |
| Denial of service | High Availability / Redundancy / Fault Tolerance |
| Elevation of privilege | Authorization |

- **Fuzzing** – a test technique where the tester applies a series of inputs to an interface in an automated fashion and examines the output for undesired behaviors.
- **Security reviews** – process to ensure that the security-related steps are being carried out and not being short-circuited.

## Software Development Methodologies

- **Waterfall model** – is a linear application development model that uses rigid phases; when one phase ends, the next begins.
- **Spiral model** – repeats steps of a project, starting with modest goals, and expanding outwards in ever wider spirals (called rounds). Each round of the spiral constitutes a project, and each round may follow traditional software development methodology such as Modified Waterfall. A risk analysis is performed each round.
- **Iterative Model** - the project is broken into smaller versions and developed incrementally.
- **Prototype model** – produces prototype and custome adds refinements until requirements are met. Prototyping is used to allow the users evaluate developer proposals and try them out before implementation.
- **Agile model**
	- **Scrum**  – contain small teams of developers, called the Scrum Team. They are supported by a [Scrum Master](http://en.wikipedia.org/wiki/Scrum_%28development%29), a senior member of the organization who acts like a coach for the team. Finally, the Product Owner is the voice of the business unit.
	- **Extreme Programming (XP)** – method that uses pairs of programmers who work off a detailed specification.
	- **Kanban** - meaning “visual board” is a project management method that helps visualize tasks.

## Bugs Concepts

The acronym **DREAD** refers to a manner of classifying bugs: Damage potential, Reproducibility, Exploitability, Affected user base, and Discoverability.

| Category  | Description |
| ----------- | ----------- |
| Bugs  | Errors in coding |
| Flaws | Errors in design |
| Behavioral anomalies  | Issues in how the application operates |
| Errors and faults | Outcome-based issues from other sources |
| Vulnerabilities | Items that can be manipulated to make the system operate improperly |

**Quality gates** and **bug bars** are used to establish minimum acceptable levels of security and privacy quality (to score bugs, in other words). A project team must negotiate quality gates (for example, all compiler warnings must be triaged and fixed prior to code check-in) for each development phase. A bug bar is a quality gate which is used to define the severity thresholds of security vulnerabilities—for example, no known vulnerabilities in the application with a “critical” or “important” rating at time of release. The bug bar, once set, should never be relaxed.
When a software user files a bug report, they must assign a STRIDE category to the bug, whether the bug is a client or server bug, and what scope the bug affects. Users can be software developers and QA staff.

# Testing

- **Test Strategy** - outlines the testing approach. High level types of tests.
- **Test Plan** - granular document that details the testing.
- **Test Case** - "What tests am I going to perform?"
- **Test Script** - "How am I going to perform the tests?"
- **Test Suite** - collection of test cases.

## Functional Testing

We test to check if the software is reliable, a.k.a. is functioning as it is supposed to.

- **Reliability** measures that the software functions as expected by the customer at all times. It is not just a measure of availability, but functionally complete availability.
- **Resiliency** is a measure of how strongly the software can perform when it is under attack by an adversary.
- **Recoverability** is the ability of an application to restore itself to expected levels of functionality after the security protection is breached or bypassed.

### Steps for Functional Testing
1. Identifying the functions (requirements) that the software is expected to perform
2. Creating input test data based on the function’s specifications
3. Determining expected output test results based on the function’s specifications
4. Executing the test cases corresponding to functional requirements
5. Comparing actual and expected outputs to determine functional compliance

### Types of Functional Testing
- **Unit Testing:** Conducted by developers during the implementation phase of SDLC. Breaks the functionality of software down into smaller parts and tests each part separate from the other parts for build and compilation and logic errors.
- **Logic Testing:** Validates the logic of the code / Is it well written?
- **Integration Testing:** Tests the "sum of its parts".
- **Regression Testing:** Validates that the software doesn't break previous functionality or security.

## Non-Functional Testing

Covers testing for the recoverability and environmental aspects of the software.

- **Performance Testing:** Will it meet the objectives of the business and satisfy requirements of the SLA? 
- **Load Testing:** What volume of tasks or users can the software handle? 
- **Stress Testing:** What is the breaking point of the software? There are two primary objectives: 
	- Does the software fail securely? 
	- Can the software recover gracefully? 
- **Scalability Testing:** Similar to load testing and helps identify performance bottlenecks.
- **Environment Testing:** Validates the security of the environment in which the software will operate.
- **Interoperability Testing:** Are the interfaces between disparate environments working?
- **Disaster Recovery Testing:** Can the critical services be restored within documented time constraints in the event of a disaster?
- **Simulation Testing:** Will the software function in the production environment? Requires the lab environment to be configured as much like production as possible.

## Other Testings

- **Privacy Testing:** Validates that sensitive information is protected appropriately.
- **UAT (User Acceptance Testing):** End user needs to be assured that the application will meet their specified requirements. Must happen before software is considered ready for release.
- All other testing should be completed (Unit, integration, regression, etc).
- Real-world usage scenarios of the software are identified and test cases are created to cover these scenarios.

# Monitoring

- Validate compliance to regulations and other governance requirements. 
- Demonstrate due diligence and due care on the part of the organization towards its stakeholders. 
- Provide evidence for audit defense. 
- Assist in forensics investigations by collecting and providing the requested evidence if tracked and audited. 
- Determine that the security settings in the environment are not below the levels prescribed in the minimum security baselines.


### Characteristics of good metrics include:

- **Consistency:** The results from the same data set must be the same or equivalent.
- **Quantitative:** Precise, objective, numeric values.
- **Objectivity:** Unbiased.
- **Relevance:** should have a direct bearing on a decision or judgement.
- **Inexpensive:** Should be cost-effective

## Monitoring Continued

- Ensure that the confidentiality, integrity and availability aspects of software.
- Assurance are not impacted adversely.
- Detect insider and external threats that are orchestrated against the organization.
- Validate that the appropriate controls are in place and working effectively.
- Identify new threats such as rogue devices and access points that are being introduced into the organization’s computing environment.
- Validate the overall state of security.

![Incidents](https://github.com/lukeciatt/csslp-notes/blob/main/Images/incidents.PNG) 

### Incident Response Process

![Incident_Response](https://github.com/lukeciatt/csslp-notes/blob/main/Images/incident_response.PNG) 

- **Preparation:** Establish incident response policies and procedures.
- **Detection and Analysis:** Continuously monitoring using monitoring. Log analysis process:
	- Collection 
	- Normalization 
	- Correlation 
	- Visualization
- Containment, Eradication and Recovery.
- **Post-Incident Analysis:** Lessons learned activities.

## Problem Management

![Problem Management](https://github.com/lukeciatt/csslp-notes/blob/main/Images/problem_management.PNG) 

The goal of incident management is to restore service while the goal of problem management is to improve service.

Disposal: End-of-Life (EOL) policy is established.

# Secure Software Requirements

## SMART Requirements (Specific Measurable Achievable Realistic Time)

- **Specific:** Non-generic, not open to misinterpretation.
- **Measurable:** Can be quantified and tested.
- **Achievable (Attainable):** Are the requirements physically/technically possible to meet? 
- **Realistic:** Similar to attainable but also includes budget and other issues (Ex: build a whole program from one day to another isn't realistic).
- **Time:** It must be tied to a measurable time frame, it is not enough to say "as soon as possible", it is necessary to say "by June 1st" for example.

## Types of Security Requirements

- Core Security (CIA / IAAA)
- General (Session / Errors / Configuration)
- Operational
- Other

Information Gathering Techniques: Brainstorming, Facilitated Workshops, Surveys, Questionnaires.

## Requirements Traceability Matrix (RTM)

The RTM is a grid that assists the development team in tracking and managing requirements and implementation details.

A **subject-object matrix** is used to identify allowable actions between subjects and objects based on use cases.
Once **use cases** are enumerated with subjects (roles) and the objects (components) are defined, a subject-object matrix can be developed.

### Use Case & Misuse Case Modeling

The use case describes the intended behavior of the software or system. Misuse cases, also known as abuse cases help identify security requirements by modeling negative scenarios. A negative scenario is an unintended behavior of the system.

At the end of each phase of the SDLC, reviews need to be conduct to ensure that the software performs as expected and meets business specifications.

# Secure Coding

## Race Condition
A race condition (in Sequencing & Time Requirements) is an undesirable situation that occurs when a device or system attempts to perform two or more operations at the same time, but because of the nature of the device or system, the operations must be done in the proper sequence to be done correctly. Race conditions are in fact one of the most common flaws observed in software
design. It is also referred to sometimes as race hazard.

## Side Channel Attacks (SCA)

Aims to gather information from or influence the program execution of a system by measuring or exploiting indirect effects of the system or its hardware -- rather than targeting the program or its code directly. Most commonly, these attacks aim to exfiltrate sensitive information, including cryptographic keys, by measuring coincidental hardware emissions. A side-channel attack may also be referred to as a sidebar attack or an implementation attack.

![Side Channel Attack](https://github.com/lukeciatt/csslp-notes/blob/main/Images/sca.png) 

## Memory Management (Preventing Buffer Overflows)

- **Locality of Reference:** Principle of locality, is the principle that subsequent data locations that are referenced when a program is run are often predictable and in proximity to previous locations based on time or space.
- **Dangling Pointers:** pointers which do not point to a valid object of the appropriate type in memory. These occur when the object that the pointer was originally referencing was deleted or de-allocated without the pointer value being modified.
- **Garbage Collection:** Attempts to reclaim memory which was allocated by the program, but is no longer referenced.
- **Type Safety:** Type safe code cannot access memory at arbitrary locations out of the range of memory address space that belongs to the object’s publicly exposed fields. It cannot access memory locations it is not authorized to access.
- **Code Access Security (CAS):** Prevents code from untrustworthy sources or unknown origins from having run time permissions to perform privileged operations. In addition to type safety, CAS concepts include the following:
	- Syntax Security (Declarative and Imperative)
	- Security Actions
	- Secure Class Libraries

**Tokenization** is the process of replacing sensitive data with unique identification symbols that still retain the needed information about the data, without compromising its security.

## Microsoft Security Development Lifecycle

[SDL](https://www.microsoft.com/en-us/sdl/) is software development process designed to enable development teams to build more secure software and address security compliance requirements.
The goals of the SDL, are twofold: to reduce the number of security-related design and coding defects, and to reduce the severity of any defects that are left. 

### SDC is built around the following three elements:

- **(Security) by Design** – the security thinking is incorporated as part of design process.
- **(Security) by Default** – the default configuration of the software is, by design, as secure as possible.
- **(Security) in Deployment** – security and privacy elements are properly understood and managed through the deployment process.

These three elements are also known as **SD3+C** (+ Communication).

[SDL components](https://www.microsoft.com/en-us/sdl/process):
- **Training** –  security training for all personnel, targeted to their responsibility associated with the development effort.
- **Requirements** –
	- Establishment of the security and privacy requirements for the software.
	- Creation of quality gates and bug bars. Defining minimum acceptable levels of security and privacy quality at the start helps a team understand risks associated with security issues, to identify and fix security bugs during development, and apply the standards throughout the entire project. Setting a meaningful bug bar involves clearly defining the severity thresholds of security vulnerabilities (for example, no known vulnerabilities in the application with a “critical” or “important” rating at the time of release) and never relaxing it once it’s been set.
	- Development of security and privacy risk assessment. Examining software design based on costs and regulatory requirements helps a team identify which portions of a project will require threat modeling and security design reviews before release and determine the Privacy Impact Rating of a feature, product, or service.
- **Design** – establish design requirements, perform attack/surface analysis/reduction and use threat modeling.
- **Implementation** – application of secure coding practices and the use of static program checkers to find common errors.
- **Verification** – perform dynamic analysis (tools that monitor application behavior for memory corruption, user privilege issues, and other critical security problems), fuzz testing, and conduct attack surface review.
- **Release** – conduct a final security review and create an incident response plan.
- **Response** – execute incident response plan.

# Software Acquisition and the Supply Chain

## Acquisition Lifecycle

![Acquisition Lifecycle](https://github.com/lukeciatt/csslp-notes/blob/main/Images/acquisition_lifecycle.PNG) 

## Security Principles

- **Least Privilege:** minimum set of rights for a minimum amount of time, based on job.
- **Separation of Duties:** Access to code and data is restricted so that tampering, unilateral control, collusion and fraud are improbable.
- **Location Agnostic Protection:** It is not the place where production occurs that determines the extent and effectiveness of the controls, but the implementation or lack thereof of the secure software development and delivery processes. Referred to as persistent protection.
- **Code Inspection:** Secure development lifecycle processes are in place to detect and identify the presence of malicious logic in code.
- **Tamper Resistance and Evidence:** The code and data is protected with technical controls such as hashing and certificate of authenticity so that unauthorized alterations are disallowed and when performed evident and restorable to its pristine state.
- **Chain of Custody:** The transfer of products from one supplier to another must be controlled, authorized, transparent and verifiable.

**Code escrow** is the activity of having a copy of the source code of the implemented software in the custody of a mutually agreed upon neutral third party known as the escrow agency or party.

Runtime Integrity Assurance = TPM Verification (if the software is signed cryptographically it should be verifiable with this)
