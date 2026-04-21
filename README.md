# Week-04-Group-Policy-Targeting-and-Enterprise-Control
Week 4 focused on advanced Active Directory Group Policy concepts including inheritance, precedence, security filtering, and OU-based targeting. Built and tested enterprise-style GPO configurations, troubleshot policy conflicts, and validated system behavior through structured analysis and recovery.
# Week 4 - Group Policy Targeting & Enterprise Control

## Overview
Week 4 focuses on advancing Active Directory Group Policy skills with an emphasis on inheritance, scope control, security filtering, and enterprise-level policy targeting. This week builds on foundational GPO concepts by introducing real-world administrative structures used in production environments.

The lab environment simulates a Windows Server Active Directory domain with multiple Organizational Units (OUs) and client machines to demonstrate how policies are applied, inherited, and controlled across different scopes.

---

## Lab Objectives

- Understand Group Policy inheritance and precedence
- Implement security-based GPO targeting
- Design proper OU structures for enterprise environments
- Differentiate between user and computer policy processing
- Troubleshoot policy application issues using structured methods
- Validate Group Policy behavior in a controlled environment

---

## Environment

- Windows Server Active Directory Domain Controller
- Windows 10/11 Client Machine
- Multiple Organizational Units (OUs):
  - IT OU
  - Lab-Workstations OU
- Group Policy Management Console (GPMC)

---

## Key Concepts Covered

### Group Policy Inheritance & Precedence
Understanding how policies are applied in the LSDOU order:
- Local
- Site
- Domain
- Organizational Unit

Also covered:
- Block Inheritance
- Enforced policies
- Policy conflict resolution

---

### Security Filtering
Explored how GPOs can be targeted using:
- Authenticated Users (default scope)
- Security groups (enterprise best practice)
- Permission-based application control

---

### OU-Based Policy Targeting
Configured and tested how Group Policy Objects behave when linked to different Organizational Units and how scope directly affects policy enforcement.

---

### User vs Computer Configuration
Analyzed how:
- User policies apply at logon
- Computer policies apply at startup
- Policy processing order affects final system behavior

---

## Troubleshooting Activities

During the lab, multiple issues were intentionally encountered and resolved:

- Overlapping GPO links across multiple OUs causing conflicting policy application
- Misinterpretation of policy scope leading to unexpected restrictions
- Identification of active policy settings affecting system behavior

### Troubleshooting Methods Used:
- Group Policy Results analysis (GUI-based)
- Scope and inheritance validation
- GPO setting inspection within Administrative Templates
- Controlled rollback of policy configurations
- Logon/logoff validation testing

---

## Issues Identified & Resolved

### Initial Problem:
Users experienced unexpected restrictions including:
- Command Prompt access blocked
- Run command (Win + R) disabled
- Control Panel access restricted

### Root Cause:
- Multiple restrictive settings enabled within a single GPO
- GPO linked across multiple OUs, creating overlapping enforcement paths

### Resolution:
- Removed duplicate GPO links from conflicting OUs
- Disabled restrictive settings within the GPO
- Revalidated system functionality after policy refresh

---

## Final Results

After remediation:
- Command Prompt access restored
- Run dialog functionality restored
- Control Panel access restored
- Group Policy behavior stabilized and predictable

---

## Key Skills Developed

- Active Directory OU design and management
- Group Policy Object configuration and targeting
- Policy inheritance and precedence analysis
- Security filtering and access control
- Troubleshooting enterprise Windows environments
- Systematic rollback and validation techniques

---

## Conclusion

This lab reinforced the importance of structured Group Policy design, proper OU architecture, and controlled troubleshooting methods in enterprise environments. It demonstrated how misconfigured scope and overlapping policies can impact end-user systems, and how systematic analysis can restore stability.

The experience builds foundational skills for roles in System Administration, IT Support, and Infrastructure Engineering.
