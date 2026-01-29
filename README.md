Nmap-Based Network Security Analysis using Machine Learning
Overview

This project focuses on defining a machine learning problem in the cybersecurity domain using Nmap-generated network scanning data. The objective is to analyze port and service information obtained from Nmap scans and formulate a structured ML problem that can assist in identifying potentially vulnerable network configurations.

This repository is created as part of a Cyber Security Lab experiment and emphasizes problem definition, data identification, assumptions, feasibility, and impact analysis, rather than full model deployment.

 Problem Statement

Develop a machine learning model that analyzes Nmap scan results to classify network ports and services as safe or potentially vulnerable, enabling faster security assessment and proactive risk mitigation.

 Domain Description

The domain of network security involves monitoring systems for open ports, running services, and misconfigurations that could be exploited by attackers.
Nmap is a widely used security assessment tool that provides detailed insights into:

Open and closed ports

Running services

Service versions

Protocol usage

Manual analysis of such data is time-consuming. Machine Learning can assist in automating this analysis by learning patterns associated with insecure configurations.

 Dataset Description
 Data Source

Dataset is self-generated using Nmap scans.

Scans are performed only on:

Localhost

Virtual Machines

Authorized lab environments

 Features Used
Feature Name	Description
IP Address	Target system IP
Port Number	Network port scanned
Protocol	TCP / UDP
Port State	Open / Closed / Filtered
Service Name	Service running on the port
Service Version	Detected service version
Scan Type	SYN / TCP Connect / Version Scan
 Data Format

CSV / XML

Easily convertible for ML preprocessing

 Output Definition

Output Type: Binary Classification

0 → Safe

1 → Potentially Vulnerable

Evaluation Metrics:

Accuracy

Precision

Recall

F1-score

Interpretability:

Feature importance analysis

Rule-based explanations (e.g., open ports with outdated services)

 Assumptions and Constraints
 Assumptions

Open ports running uncommon or outdated services indicate higher security risk

Nmap scan data sufficiently reflects network security posture

Lab-generated data is representative of real-world scenarios

 Constraints

Limited dataset size

Scans restricted to authorized systems only

No real exploit execution involved

 Ethical Considerations

No unauthorized scanning performed

No sensitive or personal data collected

Experiment conducted in an isolated lab environment

 Feasibility and Impact
 Feasibility

Nmap provides structured and reliable scan data

Lightweight ML models (Decision Tree, Logistic Regression) can be applied

Dataset creation is fully controlled and reproducible

 Impact

Reduces manual effort in analyzing network scan reports

Assists in early detection of risky configurations

Useful for network administrators and security analysts

Can be extended to intrusion detection and vulnerability assessment systems
