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
Role-Based Access Control

The project uses Microsoft Entra administrative roles to demonstrate differentiated administrative privileges.

| User              | Job Title             | Entra Role             |
| ----------------- | --------------------- | ---------------------- |
| Alexa Morgan      | IT Administrator      | User Administrator     |
| Jordan Leigh      | IT Support Specialist | Helpdesk Administrator |
| Other employees   | Various               | None                   |

Alexa Morgan was assigned the User Administrator role because her responsibilities require broader identity-management capabilities. Jordan Leigh was assigned the Helpdesk Administrator role to provide more limited support-related administrative capabilities.

The remaining employees were not assigned Entra administrative roles because their job responsibilities do not require identity administration privileges.

This design demonstrates the principle of least privilege by limiting administrative access based on job responsibilities.

## Authentication & Security
### Security Defaults

Security Defaults were enabled in the project tenant. The configuration provides baseline identity protection and MFA requirements within the capabilities of the Microsoft Entra ID Free edition.

### Authentication Methods

Available authentication methods were reviewed in the Entra admin center, including methods such as Microsoft Authenticator, SMS, and voice-based authentication.

### SSPR

Self-Service Password Reset was studied through Microsoft Learn and the Applied Skills assessment. Full SSPR password-reset functionality was not implemented in the project tenant due to licensing limitations.

### Conditional Access

A Conditional Access policy was designed to require MFA for privileged administrative accounts:

Policy: Require MFA for privileged users

Purpose: Protect accounts with elevated Entra permissions.

Reasoning: Alexa Morgan has the User Administrator role, meaning compromise of her account could allow an attacker to modify identities in Southstars Retail's tenant. Requiring MFA provides an additional layer of protection against credential compromise.

This policy was not implemented in the project tenant because Conditional Access requires Microsoft Entra ID Premium licensing. Conditional Access functionality was instead practiced through Microsoft's Applied Skills assessment environment.

## Identity Lifecycle Management

**Identity Lifecycle Management**

The project demonstrates the Joiner -> Mover -> Leaver identity lifecycle model.

**Joiner**

New employees receive:

- An Entra identity
- Department information
- Appropriate group membership
- Required access based on their job responsibilities

**Mover**

Scenario: Rex Anderson transferred from Sales to HR.

Actions performed:

- Updated department from Sales to HR
- Updated job title to HR Specialist
- Removed SG-Sales membership
- Added SG-HR membership
- Reviewed access to prevent unnecessary privilege retention

**Leaver**

Scenario: Emmanuel David left Southstars Retail.

Actions performed:

- Disabled the Entra account
- Removed SG-HR membership
- Reviewed administrative role assignments
- Confirmed the account no longer had active organizational access

These scenarios demonstrate the importance of reviewing and modifying access when an employee's organizational status changes. Removing outdated access helps prevent privilege creep and reduces the risk of unauthorized access.

## Lessons Learned

This project provided hands-on experience with foundational IAM concepts using Microsoft Entra ID. I gained practical experience managing users and groups, assigning administrative roles, applying least-privilege principles, and handling identity lifecycle events.

The project also demonstrated the difference between implementing an identity control and designing one. Several advanced Entra capabilities required licensing beyond the Free edition, requiring me to identify those limitations and use Microsoft's training environments to gain additional hands-on experience.

The lifecycle exercises reinforced the importance of reviewing access when users change roles and promptly removing access when employees leave an organization.

## Project Limitations

This project was conducted using Microsoft Entra ID Free. Some advanced identity security and access-management capabilities require Microsoft Entra ID Premium licensing.

Conditional Access and full SSPR functionality were therefore not implemented directly in the project tenant. These capabilities were studied through Microsoft Learn and practiced through Microsoft's Applied Skills assessment environment where applicable.

The organization and employee identities used in this project are entirely fictional.
