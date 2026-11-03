# TSM Apex Infrastructure Lab

![Status](https://img.shields.io/badge/Status-Active%20Development-2563EB)
![Platform](https://img.shields.io/badge/Platform-Windows%20Server-0078D4)
![Directory](https://img.shields.io/badge/Directory-Active%20Directory-475569)
![Virtualisation](https://img.shields.io/badge/Virtualisation-Oracle%20VirtualBox-183A61)
![Environment](https://img.shields.io/badge/Environment-Isolated%20Lab-15803D)

## Overview

**TSM Apex Infrastructure Lab** is a personal systems and network administration project built to demonstrate practical experience with Microsoft Windows Server, Active Directory Domain Services, DNS, Group Policy, Windows client administration, role-based access control, and secure file services.

The environment runs as an isolated virtual lab using Oracle VirtualBox. It currently consists of a Windows Server domain controller and a Windows 11 Enterprise domain-connected client.

This repository documents the implemented infrastructure, configuration decisions, validation results, and selected technical evidence.

> This is a development and learning environment. It is not presented as a production deployment.

---

## Project Objectives

The project demonstrates the ability to:

- Deploy and configure a Windows Server domain controller
- Create and administer an Active Directory forest
- Configure Active Directory-integrated DNS
- Design a structured organisational-unit hierarchy
- Manage employee and administrative identities
- Implement role-based access through security groups
- Join and administer Windows client devices
- Configure computer and user Group Policies
- Provide private employee storage
- Configure secure departmental file services
- Validate authentication, policy application, DNS, and access controls
- Document infrastructure securely for a public technical portfolio

---

## Lab Architecture

```text
Physical Windows Host
│
└── Oracle VirtualBox
    │
    ├── TSM-DC01
    │   ├── Windows Server 2025
    │   ├── Active Directory Domain Services
    │   ├── Active Directory-integrated DNS
    │   ├── Group Policy Management
    │   ├── Employee home folders
    │   └── Departmental file services
    │
    └── TSM-CL01
        ├── Windows 11 Enterprise
        ├── Active Directory domain membership
        ├── Internal DNS resolution
        ├── Computer and user Group Policy
        ├── Private employee storage
        └── Role-based departmental access
