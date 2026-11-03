# TSM Apex Infrastructure Lab

![Status](https://img.shields.io/badge/status-active%20development-blue)
![Platform](https://img.shields.io/badge/platform-Windows%20Server-0078D4)
![Directory](https://img.shields.io/badge/directory-Active%20Directory-5E5E5E)
![Virtualisation](https://img.shields.io/badge/virtualisation-Oracle%20VirtualBox-183A61)
![Environment](https://img.shields.io/badge/environment-isolated%20lab-green)

## Overview

**TSM Apex Infrastructure Lab** is a personal network and systems administration project created to demonstrate practical experience with Windows Server, Active Directory Domain Services, DNS, Group Policy, domain-connected devices, role-based access control, and Windows file services.

The environment is implemented as an isolated virtual lab using Oracle VirtualBox.

The current infrastructure provides the internal foundation for the planned TSM platform:

- `tsmapex.com` is intended to become the main public domain for TSM Apex.
- `tsmsouthafrica.co.za` is intended to host South African traffic-service websites and applications.
- `ad.tsmapex.com` is the private Active Directory namespace for employees, servers, computers, policies, and internal services.

The public websites and customer-facing services are not yet deployed. This repository currently documents the operational Windows domain infrastructure built around `TSM-DC01` and `TSM-CL01`.

---

## Project Objectives

The project aims to:

- Build and administer a functional Windows Active Directory domain.
- Centralise employee identity and computer management.
- Configure internal DNS and domain-controller discovery.
- Organise central and regional resources through dedicated OUs.
- Apply workstation security controls through Group Policy.
- Separate standard employee accounts from privileged administrative accounts.
- Control resource access through security-group membership.
- Provide private employee home folders.
- Provide protected departmental shared folders.
- Validate the environment from a domain-connected Windows client.
- Prepare the internal foundation for future TSM websites and applications.

---

## Current Architecture

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
        ├── Joined to ad.tsmapex.com
        ├── Uses TSM-DC01 for DNS
        ├── Receives computer and user policies
        ├── Receives a private H: drive
        └── Receives role-based departmental storage
