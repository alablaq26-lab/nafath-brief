Version: NAFATH-V4
Track: Software

## Overview
A national service provider depends on code it did not write, models it did not train, and routes it does not control. Each of the six fields covers a different way an attacker could compromise these dependencies without being noticed. Software configuration rules keep secrets out of source code. AI security explains how training data and model inputs can be manipulated. Mobile standards help verify the apps that citizens use. Networking controls protect the internet paths that carry traffic to the provider. Cybersecurity lessons from past vulnerabilities show how quickly one flaw can spread. Data inventories such as an SBOM reveal which components are inside each product, so teams can react fast when a flaw appears.

## Software
The Twelve-Factor App says configuration should be stored in the environment, using environment variables. Configuration means anything that changes between deployments, such as database addresses and credentials for external services. It must be kept out of the code because code is often shared, copied and stored in version control, so a secret in the code can leak. Separating them lets one codebase run unchanged in staging and production.

Resource: The Twelve-Factor App - III. Config - https://12factor.net/config

## AI
NIST groups adversarial attacks on predictive machine learning into three main categories. Evasion attacks change inputs at deployment time, for example a slightly altered image, so the model gives a wrong answer. Poisoning attacks corrupt the training data or the model itself, so the model learns wrong behaviour in advance. Privacy attacks try to extract information about training data or the model. The key difference is timing and target: inputs at use time versus data during training.

Resource: NIST AI 100-2 E2025 - Adversarial Machine Learning: A Taxonomy and Terminology of Attacks and Mitigations - https://csrc.nist.gov/pubs/ai/100/2/e2025/final

## Mobile
The OWASP MASVS is an industry standard that lists security requirements for mobile apps on Android and iOS. Its controls are grouped into areas such as storage, cryptography, authentication, network communication, platform interaction, code quality and resilience. It is used as a checklist: testers verify each control using the OWASP Mobile Application Security Testing Guide (MASTG), and teams can use the results to show that an app meets its security requirements.

Resource: OWASP Mobile Application Security Verification Standard (MASVS) - https://mas.owasp.org/MASVS/

## Networking
BGP lets networks announce which IP prefixes they can reach, and routers trust those announcements. In a hijack, a network falsely announces a prefix it does not own, or a more specific one, so routers send traffic to the attacker. RPKI lets prefix holders publish signed Route Origin Authorizations naming which AS may originate a prefix, so routers can reject invalid origins. RPKI does not validate the AS path, so path manipulation and route leaks remain possible.

Resource: RFC 6811 - BGP Prefix Origin Validation - https://www.rfc-editor.org/rfc/rfc6811

## Cybersecurity
Log4Shell was a flaw in Apache Log4j 2, a very common Java logging library. Its JNDI lookup feature could load and run code from an attacker-controlled LDAP server when a crafted string was logged, so one request could give remote code execution. It was rated critical, CVSS 10.0, because it needed no login, was easy to exploit over the network, and the library was everywhere. The first fix was Log4j 2.15.0, with later releases closing related gaps.

Resource: Apache Logging Services - Security (known vulnerabilities) - https://logging.apache.org/security.html

## Data
An SBOM is a formal, machine-readable inventory of the components and dependencies inside a piece of software, like an ingredient list. It helps organizations find affected products quickly when a vulnerability is announced. The NTIA minimum data fields are: supplier name, component name, version of the component, other unique identifiers, dependency relationship, author of the SBOM data, and timestamp. The NTIA also expects automation support and regular updates.

Resource: The Minimum Elements For a Software Bill of Materials (SBOM) - https://www.ntia.doc.gov/report/2021/minimum-elements-software-bill-materials-sbom

## Misconception in My Track

## Open Question
