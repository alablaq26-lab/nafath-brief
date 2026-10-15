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

## Cybersecurity

## Data

## Misconception in My Track

## Open Question
