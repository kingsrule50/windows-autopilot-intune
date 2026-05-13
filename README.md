# 🚀 Windows Autopilot & Microsoft Intune Deployment Lab

![Status](https://img.shields.io/badge/status-completed-brightgreen)
![Platform](https://img.shields.io/badge/platform-Microsoft%20Intune-blue)
![Focus](https://img.shields.io/badge/focus-Windows%20Autopilot-purple)
![Security](https://img.shields.io/badge/security-Entra%20ID-orange)

# 📌 Project Overview

This project demonstrates a complete Windows Autopilot and Microsoft Intune deployment workflow within a segmented enterprise lab environment.

The lab simulates a real-world enterprise endpoint onboarding process using:

- Microsoft Intune
- Microsoft Entra ID
- Windows Autopilot
- MFA Enforcement
- Windows Hello for Business
- Device Compliance Validation
- Endpoint Provisioning
- Network Segmentation

The objective of this project was to build a secure, cloud-managed Windows deployment workflow aligned with modern enterprise identity and endpoint management practices.

---

# 🏗️ Lab Environment

| Component | Purpose |
|---|---|
| VMware Workstation Pro | Virtualization platform |
| Windows 11 Pro VM | Autopilot target endpoint |
| Microsoft Intune | Endpoint management |
| Microsoft Entra ID | Identity and authentication |
| Microsoft Authenticator | MFA approval |
| Windows Hello | Passwordless authentication |
| pfSense | Network segmentation and routing |

---

# 🌐 Network Segmentation

| Network | Purpose |
|---|---|
| 192.168.10.0/24 | Internal Windows / Management Network |
| 192.168.20.0/24 | Isolated Kali Security Testing Network |
| 10.10.10.0/24 (vmnet5) | Dedicated segmented Host-Only Lab Network |
| pfSense Firewall | Traffic routing and segmentation |

---

# 🎯 Project Objectives

- Deploy a Windows 11 endpoint using Windows Autopilot
- Register devices into Microsoft Intune
- Configure cloud-based endpoint enrollment
- Enforce MFA authentication using Microsoft Authenticator
- Configure Windows Hello for Business
- Validate device compliance inside Intune
- Demonstrate device inventory visibility
- Demonstrate endpoint reset and recovery workflows
- Simulate enterprise-grade endpoint onboarding
- Demonstrate segmented enterprise lab networking

---

# 🔐 Technologies Demonstrated

## Identity & Access Management

- Microsoft Entra ID
- MFA Enforcement
- Conditional Access Concepts
- Passwordless Authentication
- Windows Hello for Business

## Endpoint Management

- Microsoft Intune
- Windows Autopilot
- Device Enrollment
- Compliance Validation
- Endpoint Inventory Management
- Device Reset & Recovery

## Security Concepts

- Secure Endpoint Provisioning
- Cloud Identity Integration
- MFA Enforcement
- Enterprise Enrollment Workflow
- Zero Touch Deployment Concepts
- Segmented Network Security

---

# 🛠️ Deployment Workflow

## 1. VMware Network Segmentation

VMware Virtual Network Editor was configured with isolated host-only networks to support segmented enterprise lab traffic and secure testing boundaries.

- vmnet3 → 192.168.10.0/24
- vmnet2 → 192.168.20.0/24
- vmnet5 → 10.10.10.0/24

![VMware Network Segmentation](screenshots/vmware-network-segmentation.png)

---

## 2. Windows Device Sign-In

The Windows 11 endpoint was connected to Microsoft Entra ID using an organizational account.

![Entra ID Sign-In](screenshots/entra-id-device-signin.png)

---

## 3. MFA Authentication Approval

Microsoft Authenticator was used to approve the sign-in request during enrollment.

![MFA Approval](screenshots/mfa-authenticator-approval.png)

---

## 4. Device Join Success

The device was successfully joined to the Microsoft Entra ID tenant.

![Entra ID Join Success](screenshots/entra-id-device-join-success.png)

---

## 5. Windows 11 Validation

The Windows 11 version and operating system details were validated prior to enrollment.

![Windows 11 Validation](screenshots/windows11-version-validation.png)

---

## 6. Install Windows Autopilot Script

PowerShell was used to install the Get-WindowsAutopilotInfo script required for hardware hash extraction.

![Install Script](screenshots/install-get-windowsautopilotinfo-script.png)

---

## 7. Generate Hardware Hash

The device hardware hash was generated and exported into a CSV file for Autopilot registration.

![Generate Hardware Hash](screenshots/generate-autopilot-hardware-hash.png)

---

## 8. Upload Hardware Hash CSV

The generated Autopilot CSV file was uploaded into Microsoft Intune.

![Upload CSV](screenshots/upload-autopilot-hardware-hash-csv.png)

---

## 9. CSV Validation Success

The uploaded hardware hash file was successfully validated inside Intune.

![CSV Validation](screenshots/autopilot-csv-validation-success.png)

---

## 10. Autopilot Device Registration

The Windows device successfully appeared within the Windows Autopilot devices inventory.

![Autopilot Registration](screenshots/autopilot-device-registration-success.png)

---

## 11. Autopilot Profile Creation

An Autopilot deployment profile was created and configured for enterprise deployment.

![Autopilot Profile Creation](screenshots/autopilot-profile-creation.png)

---

## 12. Group Assignment

The deployment profile was assigned to the target deployment group.

![Group Assignment](screenshots/autopilot-profile-group-assignment.png)

---

## 13. Device Group Membership

The enrolled endpoint successfully appeared within the assigned deployment group.

![Device Group Membership](screenshots/autopilot-device-group-membership.png)

---

## 14. OOBE Deployment Experience

The device entered the Windows Autopilot Out-of-Box Experience (OOBE) deployment process.

![OOBE Configuration](screenshots/autopilot-oobe-configuration.png)

---

## 15. Organization Sign-In

The user authenticated using organizational credentials during deployment.

![Organization Sign-In](screenshots/autopilot-organization-signin.png)

---

## 16. Network Connection Validation

Network connectivity was validated during the provisioning workflow across segmented VMware host-only networks.

![Network Connection](screenshots/autopilot-network-connection.png)

---

## 17. Device Provisioning

Windows Autopilot automatically provisioned the endpoint using assigned cloud policies.

![Device Provisioning](screenshots/autopilot-device-provisioning.png)

---

## 18. Windows Hello Enrollment

Windows Hello for Business enrollment was initiated.

![Windows Hello Enrollment](screenshots/windows-hello-enrollment.png)

---

## 19. Windows Hello PIN Setup

The user configured a secure Windows Hello PIN.

![PIN Setup](screenshots/windows-hello-pin-setup.png)

---

## 20. Windows Hello Completion

Windows Hello for Business enrollment completed successfully.

![Windows Hello Complete](screenshots/windows-hello-complete.png)

---

## 21. Intune Device Inventory

The endpoint appeared within the Microsoft Intune managed device inventory.

![Intune Inventory](screenshots/intune-device-inventory.png)

---

## 22. Device Compliance Validation

The endpoint successfully passed Intune compliance validation.

![Compliance Validation](screenshots/intune-device-compliance-validation.png)

---

## 23. Windows Recovery & Reset Workflow

Remote reset and recovery operations were demonstrated for enterprise device lifecycle management.

### Recovery Reset

![Recovery Reset](screenshots/windows-recovery-reset.png)

### Reset Configuration

![Reset Configuration](screenshots/windows-reset-configuration.png)

### Reset Confirmation

![Reset Confirmation](screenshots/windows-reset-confirmation.png)

---

# 📊 Key Skills Demonstrated

- Windows Autopilot Deployment
- Microsoft Intune Administration
- Microsoft Entra ID Integration
- Endpoint Provisioning
- MFA Enforcement
- Windows Hello for Business
- Cloud Endpoint Enrollment
- Device Compliance Validation
- Endpoint Lifecycle Management
- Enterprise Identity Integration
- PowerShell Automation
- Endpoint Security Management
- Network Segmentation
- VMware Lab Administration

---

# 🔍 Security Benefits Demonstrated

- Centralized cloud device management
- MFA-protected authentication workflow
- Secure endpoint onboarding
- Reduced manual deployment effort
- Enterprise-grade identity integration
- Compliance-based endpoint validation
- Standardized endpoint configuration
- Modern passwordless authentication support
- Segmented lab network isolation

---

# 🧠 Lessons Learned

This project reinforced the importance of:

- Cloud-managed endpoint provisioning
- Secure identity integration
- MFA enforcement during enrollment
- Endpoint compliance validation
- Structured deployment workflows
- Enterprise device lifecycle management
- Network segmentation and isolation

The deployment also demonstrated how Windows Autopilot and Intune simplify large-scale endpoint onboarding while improving security and operational consistency.

---

# 📁 Repository Structure

```text
windows-autopilot-intune-deployment/
├── README.md
├── screenshots/
├── report/
├── diagrams/
└── scripts/
```

---

# 👨‍💻 Author

Chinedu Kingsley Asuzu

- Cybersecurity Analyst
- Microsoft 365 Cloud & Security Engineer
- GRC & Identity Security Enthusiast

GitHub: https://github.com/kingsrule50

---

# ⭐ Final Outcome

This project successfully demonstrated a complete Windows Autopilot deployment lifecycle using Microsoft Intune and Microsoft Entra ID.

The lab reflects real-world enterprise endpoint onboarding, identity integration, MFA enforcement, segmented network security, and device compliance workflows commonly used within modern cloud-managed environments.
