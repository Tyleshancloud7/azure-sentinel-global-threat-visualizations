

## Overview

This project demonstrates how Microsoft Sentinel Workbooks can visualize security events geographically using Azure logs.

These maps help security analysts quickly detect suspicious global activity patterns.

---

## Entra ID Authentication Success

Successful login activity from users across the world.

![Authentication Success Map]

---<img width="2134" height="998" alt="Image 3-4-26 at 2 27 PM" src="https://github.com/user-attachments/assets/691011ed-f52d-41f1-be57-fb86bc10ef61" />


## Entra ID Authentication Failures

Failed login attempts that could indicate password spraying or brute-force attacks.

![Authentication Failures Map]

---<img width="1942" height="1058" alt="Image 3-4-26 at 2 26 PM" src="https://github.com/user-attachments/assets/690bb16f-6487-4fdf-a3a3-29828e1062d8" />


## Azure Resource Creation

Shows administrative actions creating new resources in Azure.

![Resource Creation Map]

---<img width="2100" height="1044" alt="Image 3-4-26 at 2 25 PM" src="https://github.com/user-attachments/assets/0e9fb371-e6a9-4ab4-90fb-21972eae9878" />


## VM Authentication Failures

Displays failed login attempts targeting Azure virtual machines.

![VM Authentication Failures Map]

---<img width="2210" height="1058" alt="Image 3-4-26 at 2 24 PM" src="https://github.com/user-attachments/assets/9b1fa34a-6520-41d0-9532-13bc3a04c88b" />


## Malicious Traffic Entering the Network

Visualizes potential malicious inbound traffic detected in the environment.

![Malicious Traffic Map]

---<img width="2040" height="1058" alt="Image 3-4-26 at 1 46 PM" src="https://github.com/user-attachments/assets/9408a5d1-727d-4bc5-9374-60818c861ac6" />


## Security Investigation Summary

During analysis of the Microsoft Sentinel workbook visualizations, several patterns were identified across authentication and network activity.

### Key Observations

• High authentication activity originating from the United States, which represents expected user behavior within the lab environment.

• Multiple authentication attempts originating from international locations including Europe and Asia.

• Clusters of failed authentication attempts suggesting possible password spraying or brute-force login activity.

• Suspicious inbound traffic targeting exposed virtual machines from various global regions.

### Potential Security Risks

The geographic distribution of authentication failures may indicate:

- Brute force authentication attempts
- Password spraying attacks
- Automated bot login attempts
- Compromised credentials being tested from multiple locations

Additionally, malicious inbound traffic could represent reconnaissance activity attempting to identify vulnerable services.

### Investigation Approach

To analyze this activity, Microsoft Sentinel workbooks were used to visualize log data geographically using the following sources:

- Entra ID Signin Logs
- Azure Activity Logs
- Virtual Machine Authentication Logs
- Network Security Logs

By mapping activity using IP geolocation, it becomes easier to identify abnormal patterns and prioritize investigation of suspicious login sources.

### Detection Opportunities

Based on the observed activity, the following detections could be implemented:

- Alert on excessive failed login attempts from a single IP address
- Alert on authentication attempts from unfamiliar geographic regions
- Detect successful logins following multiple failed attempts
- Monitor unusual administrative resource creation activity

These detection strategies help security teams respond quickly to potential threats within cloud environments.



## Skills Demonstrated

- Microsoft Sentinel
- Azure Workbooks
- KQL (Kusto Query Language)
- Threat Hunting
- Cloud Security Monitoring
- SIEM Visualization

---

## Tools Used

- Microsoft Azure
- Microsoft Sentinel
- Azure Log Analytics
- KQL Queries
