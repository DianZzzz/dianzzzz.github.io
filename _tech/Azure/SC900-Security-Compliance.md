---
layout: blog
topic: Azure
title: SC-900 Security Compliance
tags:  datascience azure cybersecurity security
comments: true
date: 2022-11-04
---

# SC-900 Security Compliance

- [Zero-Trust](#zero-trust)
- [Division of Responsibility](#division-of-responsibility)
- [CIA Triad](#cia-triad)
- [Four types of threats](#four-types-of-threats)
- [Cypher](#cypher)
- [Cryptopgraphic keys](#cryptopgraphic-keys)
- [Salting](#salting)
- [In-Transit vs At-Rest Encryption](#in-transit-vs-at-rest-encryption)
- [Security Information and Event Management (SIEM)](#security-information-and-event-management-siem)
- [Security Orchestration Automated Response (SOAR)](#security-orchestration-automated-response-soar)
- [Extended Detection and Response (XDR)](#extended-detection-and-response-xdr)
- [Endpoint Detection and Response (EDR)](#endpoint-detection-and-response-edr)
- [Cloud Access Security Brokers (CASB)](#cloud-access-security-brokers-casb)
- [Inventory](#inventory)
- [Attack vectors and attack surfaces](#attack-vectors-and-attack-surfaces)
- [Ingress vs Egress](#ingress-vs-egress)
- [STRIDE Methodology](#stride-methodology)
- [IDS/IPS](#idsips)
- [MITRE ATT&CK](#mitre-attck)
## Zero-Trust
- "Trust no one, verify everything" principle
- Verify Explicity: always authenticate and authorize based on all available data points
- Principle of Least Priviledge (PoLP): Limit user access with **Just-In-Time** and **Just-Enough-Access** (JIT/JEA) risk-based adaptive policeis and data protection
  - JIT: giving access to resources only during the time when needed
  - JEA: giving access to only the specific actions
- Assume Breach: Minimize blast radius and segment access. Verify end-to-end encryption and use analytics to get visibility, drive threat detection, and improve defenses.

## Division of Responsibility
![](/assets/2022-11-04-21-09-54.png)

## CIA Triad
- **Confidentiality**: protect data from unauthorized users by encryption
- **Integrity**: maintaining and assuring the accuracy and completeness of data over its entire lifecycle
- **Availability**: information needs to be available when needed

## Four types of threats
- **Dictionary attack**: attacker attempts to steal an identity by brute forcing into a target accounts by enumerating over a large number of known passwords
- **Disruptive attacks**: attacker attempts to disrupt a computer system or computer network for various reasons
- **Ransomware**: a malware that holds data, workstation or a network hostage until the ransom has been paid
- **Data breach**: when a malicious actor gains unauthorized accesss to a system

## Cypher
- An algo that performs encryption or decryption
- Cyphertext is the result of encryption performed on plaintext

## Cryptopgraphic keys
- Symmetric encryption: same key used for encoding and decoding
- Asymmetric encryption: different keys used for encoding and decoding

## Salting
- Add a random string to a password to increase its uniqueness without increasing user requirements and to mitigate password attacks like hashtables

## In-Transit vs At-Rest Encryption

- In-Transit
  - Data is secure when moving betwwen locations
  - e.g. Secure Sockets Layers (SSL)
- At-Rest
  - Data is secure when residing on storage 
  - e.g. Rivest-Shamir-Adleman (RSA)

## Security Information and Event Management (SIEM)

- Provides real-time analysis of security alerts generated by network hardware and application

## Security Orchestration Automated Response (SOAR)

- Collects data about security threats and respond to security events without human assistance by triggering action-driven automated workflows and processes to run seucirty tasks
- Can use AI and ml to provide recommendations and further automate responses

## Extended Detection and Response (XDR)

- A cross layered detection and response security system
- Uses a holistic approach to detect and response to threats by collaborating multiple data sources into a multi-vector solution

## Endpoint Detection and Response (EDR)

- Combines real time continuous monitoring and collection of endpoint data with rules-based automated responses and analysis capabilities
- EDR is designed to detect Advanced Persist Threat (APT), which not only breaches a security perimeter but also take up residence within a network to steal data over a long period of time

## Cloud Access Security Brokers (CASB)

- Sits between cloud servie users and cloud applications and monitors all activity and enforces security policies

## Inventory
- List of assets (software and hardware)
- Perimeter assets: assets exposed to the internet
- Core assets: assets within the org's private network

## Attack vectors and attack surfaces
- Attack vector: methods that a malicious actor uses to breach or infiltrate the network. The larger the inventory the greater the attack vectors
- Attack surface: the sum of attack vectors.

## Ingress vs Egress
- Ingress traffic: traffic entering a network boundary
- Egress traffic: traffic exiting a network boundary

## STRIDE Methodology

Categorizes threats into different categories:

- **S**poofing: illegally acessing and using another user's authentication information
- **T**ampering: malicious modificiation of data
- **R**epudiation: illegal operation in a system that lacks the ability to trace the prohiited operation
- **I**nformation Disclosure: exposure of information to individuals who are not supposed to have access to it
- **D**enial of Service: deny service to valid users
- **E**levation of Privilege: unprivileged user gains privileged access


## IDS/IPS

- Intrusion Detection System monitors a network or system for malicious activity or policy violations
  - Simple technique: signature-based detection, a signature is a set of rules which will be compared against observed events to identify possible incidents
  - Advanced technique: anomaly-based detection, compares what is considered normal activity with observed events in order to identify significant deviations
  - Profile technique: stateful protocol analysis, compares predetermined profiles of generally accepted definition for benign protocol activity for each protocol state against observed events in order to identify deviations
- Intrusion Protection System restricts access to a network or systems mitigate malicious activity or policy violations

## MITRE ATT&CK 
- A globally accessible knowledge base of adversary tactics and techniques 
- Used as a foundation for the development of specific threat models and methodologies in the private sector, government and cybersecurity community

