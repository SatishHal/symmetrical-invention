---
title: "Implement Intune Conditional Access & Endpoint Security"
date: 2025-08-23
categories:
  - projects
  - endpoint-security
tags:
  - Intune
  - Conditional Access
  - Endpoint Security
  - Entra ID
  - Microsoft 365
layout: single
author_profile: true
read_time: true
---

I implemented Intune policies to secure devices, enforce compliance, and streamline access to corporate resources. By doing this It ensures devices are secure, compliant, and only authorized devices can access corporate resources. 

Step-by-Step: 

Implement Intune Conditional Access & Endpoint Security 

Lab Prerequisites 

Windows 11 VM (Pro, 22H2 or later recommended) 

Microsoft Entra ID (Azure AD) with admin privileges 

Intune subscription (included with Microsoft 365 E3/E5 or trial) 

User account for testing (in Entra ID, member of Corporate Users group) 

 

Step 1: 

Prepare Your Entra ID Environment 

Sign in to the Microsoft Entra Admin Center. 

Create a security group for your test users: 

Name: Corporate Users 

Type: Security 

Membership: Assigned 

Add your test user(s) to this group. 

 

Step 2: 

Configure Device Compliance Policies in Intune 

Go to Microsoft Endpoint Manager Admin Center. 

Navigate to: Devices → Compliance policies → Policies → Create Policy. 

Platform: Windows 10 and later 

Settings to configure: 

Require BitLocker encryption: Yes 

Require antivirus (Windows Defender): Yes 

Require firewall: Yes 

Minimum OS version: Windows 11 22H2 (for lab consistency) 

Assign the policy to the Corporate Users group. 

Save and create the policy. 

 

Step 3: 


Configure Endpoint Security Profiles 

In Endpoint Manager: Endpoint security → Security baselines → + Create profile 

Platform: Windows 10 and later 

Profile type: Microsoft Defender for Endpoint Security Baseline 

Configure key security settings: 

Turn on real-time protection 

Enable network protection 

Enforce automatic updates 

Assign the profile to the Corporate Users group. 

 

Step 4: 


Create Conditional Access Policy 

Go to Entra Admin Center → Security → Conditional Access → + New Policy 

Name: Require Compliant Device for Cloud Apps 

Assignments: 

Users: Corporate Users group 

Cloud apps: All cloud apps (or select specific apps like Microsoft Teams, SharePoint) 

Conditions (optional for lab testing): 

Locations: Include All, Exclude Trusted IPs if needed 

Device platforms: Windows 

Access controls → Grant: Require device to be marked as compliant 

Enable policy: On 

Save policy 

 

Step 5: 


Test Conditional Access 

Log in to your Windows 11 VM with your test user account. 

Go to a Microsoft 365 app (Teams, SharePoint, or Outlook web). 

If device is non-compliant, access should be blocked. 

Apply the compliance policy to make the device compliant. 

Refresh the browser/app and verify access is now granted. 

 

Step 6: 


Monitor Compliance & Reports 

In Endpoint Manager: Devices → Monitor → Device compliance 

Check that your VM is showing compliant 

Review policy results and remediation actions if required 

 

Step 7: 


Optional – Automate Remediation 

Configure automatic remediation for non-compliant devices: 

Navigate: Devices → Compliance policies → Settings 

Enable automatic action to notify user or block access until compliant 

 

✅ Result 


Device is now securely enrolled in Intune 

Compliance policies ensure security requirements (BitLocker, firewall, antivirus) 

Conditional Access ensures only compliant devices access corporate resources 

Endpoint Security profiles enforce Microsoft Defender baseline settings 
