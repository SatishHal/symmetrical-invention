---
title: "SaaS Application Access Hardening"
categories:
  - projects
tags:
  - IT Help Desk
  - SaaS Support
  - Security
  - Entra ID
  - Conditional Access
layout: single
author_profile: true
read_time: true
---
## Overview
Implemented secure access controls for SaaS applications to ensure only authorized users on compliant devices could access company resources.

## Step 1: Identify the Access Risk
During daily IT support operations, SaaS applications were accessible from unmanaged devices, creating security risks and repeated support tickets.

## Step 2: Define the Security Objective
The goal was to enforce consistent authentication, reduce unauthorized access, and improve visibility into SaaS sign-ins.

## Step 3: Inventory SaaS Applications
Reviewed enterprise applications in Entra ID and identified business-critical SaaS platforms requiring access hardening.

## Step 4: Review Authentication Settings
Assessed MFA enforcement, user assignments, and existing Conditional Access policies for gaps.

## Step 5: Organize Users & Groups
Implemented role-based Entra ID groups and removed direct user assignments.

## Step 6: Configure Conditional Access
Applied MFA and device-compliance requirements using Conditional Access policies.

## Step 7: Integrate Device Compliance
Linked SaaS access to Intune-managed, compliant devices.

## Step 8: Test Access Scenarios
Tested sign-ins from compliant and non-compliant devices to validate behavior.

## Step 9: Support Users During Rollout
Assisted users with MFA setup, device enrollment, and remediation steps.

## Step 10: Documentation
Documented common errors, remediation steps, and escalation paths.

## Step 11: Monitor Logs
Reviewed Entra ID sign-in logs and Conditional Access results.

## Step 12: Policy Refinement
Adjusted policies based on support feedback and monitoring.

## Outcome
- Improved SaaS security posture  
- Reduced authentication-related tickets  
- Improved consistency in access enforcement  

## Tools Used
- Microsoft Entra ID  
- Conditional Access  
- Microsoft Intune  
- Microsoft Authenticator  
- ServiceNow
