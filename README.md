# Microsoft Entra ID Identity & Access Management Lab
A hands-on Identity and Access Management (IAM) project utilizing Microsoft Entra ID to simulate identity administration for a fictional organization.

## Overview
This project covers the design and administration of an identity environment for Southstars Retail, a fictional retail organization with approximately 40 employees across five departments: HR, IT, Sales, Finance, and Operations.

The project focuses on foundational Identity and Access Management concepts including user and group management, role-based access control (RBAC), least privilege, authentication security, and identity lifecycle management.

The project environment was implemented with Microsoft Entra ID and reinforced with Microsoft Learn training and the Microsoft Applied Skills assessment: *Get started with identities and access using Microsoft Entra*.

## Objectives & Goals
- Configure and manage user identities in Microsoft Entra ID
- Create and manage department-based security groups
- Apply role-based access control principles
- Demonstrate least-privilege access
- Explore authentication and identity security controls
- Simulate employee transfers and access changes
- Simulate employee off-boarding
- Document an identity lifecycle management process
- Design security controls that could be implemented with Microsoft Entra ID Premium features

## Environment

| Component         | Details                                                      |
| ----------------- | ------------------------------------------------------------ |
| Cloud Platform    | Microsoft Azure                                              |
| Identity Platform | Microsoft Entra ID                                           |
| Tenant Edition    | Microsoft Entra ID Free                                      |
| Training          | Microsoft Learn                                              |
| Applied Skills    | Get started with identities and access using Microsoft Entra |

## Organization Design
**Organization**: Southstars Retail

**Industry**: Retail

**Employees**: 40

| Department | Employees |
| ---------- | --------: |
| HR         |         3 |
| IT         |         3 |
| Finance    |         4 |
| Operations |        15 |
| Sales      |        15 |
| **Total**  |    **40** |

Eight employee identities were created in the Entra tenant to represent a portion of the organization's identity environment.

## Identity & Group Management
The project uses security groups based on the organization's departments to organize users and simplify access management.

| Group      | Purpose                   |
| ---------- | ------------------------- |
| SG-HR      | HR department access      |
| SG-IT      | IT department access      |
| SG-Finance | Finance department access |
| SG-Sales   | Sales department access   |

Users were manually assigned to groups based on their simulated department. Group-based access management was chosen to allow access and permissions to be managed wholly rather than individually.

## RBAC (Role-Based Access Control)
