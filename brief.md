Version: NAFATH-V4
Track: Cybersecurity

## Overview
A national service provider depends on software, AI models, mobile applications, internet networks, cybersecurity controls, and data to deliver reliable services. A weakness in one part of the software supply chain can affect the entire system. Secret management and secure configuration help prevent unauthorized access to sensitive information. AI security helps reduce attacks that manipulate training data or model inputs. Mobile application security helps protect users' data. RPKI and BGP route monitoring can reduce risks of unauthorized internet traffic redirection. Cybersecurity procedures help identify and fix vulnerabilities such as Log4Shell before attackers exploit them. A Software Bill of Materials (SBOM) records software components and dependencies, helping teams identify vulnerable components. This raises a cybersecurity question: how can organizations identify vulnerable third-party components and update them without disrupting essential services?

## Software
Secure software depends on more than writing correct code. Developers must also protect configuration settings, credentials, and connections to external services. Storing passwords or API keys directly in source code can expose them when a repository is shared or leaked. The Twelve-Factor App recommends separating configuration from code and using environment variables for deployment-specific settings. These practices reduce accidental exposure and make applications easier to manage securely across environments.

Resource: The Twelve-Factor App — III. Config
https://www.12factor.net/config

## AI
AI systems introduce security risks throughout their life cycle, including training, testing, and deployment. Attackers may poison training data to influence a model's behavior or create inputs that cause incorrect predictions. Other attacks may target the model or attempt to reveal sensitive information. The NIST adversarial machine learning report classifies these attack types and discusses mitigation approaches. Understanding these risks helps teams evaluate AI systems rather than assuming that a model is secure simply because it performs well.

Resource: NIST — Adversarial Machine Learning: A Taxonomy and Terminology of Attacks and Mitigations
https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-2e2023.pdf

## Mobile
Mobile applications can expose sensitive information if they do not protect stored data, user authentication, and network communication. Security testing should examine how an app handles credentials, permissions, untrusted input, and communication with remote services. The OWASP Mobile Application Security Verification Standard (MASVS) provides security controls for assessing mobile apps across areas such as storage, cryptography, authentication, and networking. Using these controls during development and testing can help teams identify weaknesses before attackers exploit them.

Resource: OWASP — About the Standard
https://mas.owasp.org/MASVS/02-Frontispiece/

## Networking
Internet routing relies on Border Gateway Protocol (BGP) to exchange route information between autonomous systems. Incorrect or malicious route announcements can redirect traffic away from its intended destination. Resource Public Key Infrastructure (RPKI) supports route origin validation by checking whether the autonomous system announcing an IP prefix is authorized to originate it. This helps reduce certain routing risks, although it does not prevent every type of BGP attack.

Resource: RFC Editor — RFC 6811: BGP Prefix Origin Validation
https://www.rfc-editor.org/rfc/rfc6811.html

## Cybersecurity
Software vulnerabilities can threaten systems when attackers exploit weaknesses before they are fixed. A well-known example is CVE-2021-44228, commonly called Log4Shell, which affected certain versions of Apache Log4j and could allow remote code execution. Organizations should identify affected software components, check whether vulnerable versions are in use, and apply appropriate security updates. Keeping an inventory of dependencies and monitoring official security advisories can help teams respond to vulnerabilities more effectively.

Resource: Apache Logging Services — Security
https://logging.apache.org/security.html

## Data
Data security includes protecting information and understanding the software components that process or store it. A Software Bill of Materials (SBOM) is a formal record of the components used to build a software product and their supply-chain relationships. It can help organizations identify affected components when new vulnerabilities are discovered and manage software risks. However, an SBOM alone does not secure an application; it supports security work by improving visibility into software dependencies.

Resource: National Telecommunications and Information Administration — The Minimum Elements for an SBOM
https://www.ntia.gov/files/ntia/publications/sbom_minimum_elements_report.pdf

## Misconception in My Track
A common misconception in cybersecurity is that a software vulnerability can only affect a system when attackers directly access its main application. However, vulnerabilities in third-party libraries can also put applications at risk. Log4Shell (CVE-2021-44228) affected certain versions of Apache Log4j 2, and attackers could exploit the vulnerable logging functionality to execute code remotely under the relevant conditions. Developers and security teams should therefore check dependencies, identify vulnerable versions, and apply appropriate updates instead of focusing only on their own application code.

Evidence: Apache Logging Services — Security, section “CVE-2021-44228”
https://logging.apache.org/security.html

## Open Question
How can organizations continuously identify vulnerable third-party software components and respond quickly to newly discovered vulnerabilities without disrupting essential services?
