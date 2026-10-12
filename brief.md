Version: NAFATH-V4
Track: Cybersecurity

## Overview
A national service provider depends on software, AI models, mobile applications, internet networks, cybersecurity controls, and data to deliver reliable services. Because a weakness in one part of the software supply chain can affect the entire system, these areas are interconnected. Secret management and software configuration aid in preventing unwanted access to sensitive information. AI security helps reduce the risk of attacks that manipulate training data or model inputs. The security of mobile applications contributes to the protection of users' data. RPKI and BGP route monitoring are two network security techniques that help reduce the risk of unauthorized internet traffic redirection. Vulnerabilities like Log4Shell may be found and fixed with the use of cybersecurity procedures before attackers can use them. Finally, a Software Bill of Materials (SBOM) records software components and their dependencies, helping teams identify vulnerable components and respond to security risks.

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

## Open Question
