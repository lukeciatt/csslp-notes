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

![Simple Quantitative Risk Calculation](http://img.png)
