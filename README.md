<p align="center">
  <img src="screenshots/mfa_banner.png" 
       alt="Azure AD / Entra ID — MFA Enforcement Lab Banner" width="100%">
</p>

# 🔐 Project 2 — Microsoft Entra ID  
## Multi-Factor Authentication (MFA) Enforcement Lab

![Entra ID](https://img.shields.io/badge/Microsoft_Entra_ID-IAM-blue?style=flat-square)
![MFA](https://img.shields.io/badge/Authentication-MFA_Enforcement-blue?style=flat-square)
![Security](https://img.shields.io/badge/Identity_Security-Zero_Trust-blue?style=flat-square)
![Governance](https://img.shields.io/badge/Access_Governance-Method_Policies-blue?style=flat-square)

---

<details open>
  <summary><h2>📘 Executive Summary</h2></summary>

This project demonstrates how to **secure user identities in Microsoft Entra ID through Multi-Factor Authentication (MFA)** using:

✅ Authentication Method Policies  
✅ Group-based MFA enforcement  
✅ Registration Campaigns  
✅ User sign-in and MFA registration flow  

This is a core identity security function in modern enterprises and represents real responsibilities of IAM Analysts, Identity Engineers, and Access Governance specialists.

By targeting MFA to a specific group (`GG-MFA-Enforced`), this lab models a **controlled, least-privilege, zero-trust aligned rollout**, mirroring how organizations implement MFA in production.

</details>

---

<details open>
  <summary><h2 id="overview">🎯 Objective</h2></summary>

Implement and enforce Microsoft Authenticator as the required MFA method for a targeted user group while documenting:

- Authentication method policies  
- Group-scoped MFA enforcement  
- Registration campaign behavior  
- Real user experience during MFA onboarding  

All configurations and user flows are captured with screenshots for auditability.

</details>

---

<details open>
  <summary><h2 id="skills">✅ Skills Demonstrated</h2></summary>

- Identity & Access Management (IAM)  
- Microsoft Entra ID Administration  
- Authentication Method Policies  
- Multi-Factor Authentication Enforcement  
- Registration Campaign Deployment  
- User Sign-In & Security Info Setup  
- Access Governance & Least Privilege  
- Zero-Trust Authentication Principles  

</details>

---

<details open>
  <summary><h2 id="policy">🔑 1. Authentication Method Policy Configuration</h2></summary>

### ✅ Microsoft Authenticator enabled  
Only members of **GG-MFA-Enforced** can register or use the Authenticator app.

**Evidence:**  
![Authentication Methods Policy](screenshots/auth-methods-policy.png)

</details>

---

<details open>
  <summary><h2 id="targeted">🎯 2. Targeted MFA Enforcement (Group-Scoped)</h2></summary>

### ✅ Enforcement applied to the security group  
`GG-MFA-Enforced` is configured as a **required MFA group**, ensuring:

- Controlled rollout  
- Safe testing window  
- RBAC-aligned enforcement  
- No accidental enforcement on global admins  

**Evidence:**  
![Authenticator Enabled for Group](screenshots/mfa-authenticator-enabled.png)

</details>

---

<details open>
  <summary><h2 id="campaign">📣 3. Registration Campaign Setup</h2></summary>

### ✅ Registration Campaign Configured  
- Target: `GG-MFA-Enforced`  
- Prompts users to register strong authentication  
- Required on next sign-in  

**Evidence:**  
![Registration Policy](screenshots/mfa-registration-policy.png)

</details>

---

<details open>
  <summary><h2 id="signin">🔐 4. User Sign-In: “More Information Required”</h2></summary>

When the test user signs in, Entra ID blocks access until MFA setup is completed.

**Evidence:**  
![More Information Required](screenshots/mfa-more-information-required.png)

</details>

---

<details open>
  <summary><h2 id="registration">📱 5. Microsoft Authenticator Registration Flow</h2></summary>

User is guided through downloading Microsoft Authenticator and scanning the QR code.

**Evidence:**  
![Authenticator Registration Prompt](screenshots/mfa-authentication-prompt.png)

</details>

---

<details open>
  <summary><h2 id="success">✅ 6. MFA Registration Success</h2></summary>

After completing setup, MFA becomes mandatory for all future sign-ins.

**Evidence:**  
![MFA Registration Success](screenshots/mfa-registration-success.png)

</details>

---

<details>
  <summary><h2 id="governance">🔐 Access Governance & Security Rationale</h2></summary>

### ✅ Why MFA Enforcement Matters  
MFA is the single strongest defense against:

- Password spray  
- Phishing  
- Credential stuffing  
- Brute-force attempts  
- Compromised password reuse  

It reduces account compromise risk by **over 99%** (Microsoft reporting).

---

### ✅ Why Use a Targeted Group (`GG-MFA-Enforced`)  
- Safest way to roll out MFA  
- Allows phased testing  
- Prevents accidental lockout of admins  
- Supports identity governance at scale  

---

### ✅ Why Microsoft Authenticator?  
- Strongest built-in MFA method  
- Push notifications  
- Resistant to SIM-swap/SMS-interception  
- Compatible with advanced features:
  - Passwordless  
  - Number matching  
  - Phish-resistant MFA  

</details>

---

<details>
  <summary><h2 id="learned">📘 What I Learned</h2></summary>

- How to enforce MFA inside Entra ID  
- How to configure Authentication Method Policies  
- How to launch a Registration Campaign  
- How Entra ID guides the user during MFA onboarding  
- Why MFA is essential for Zero-Trust identity strategy  
- How to document IAM steps for audit and governance  

</details>

---

<details>
  <summary><h2 id="nextsteps">📋 Next Steps (Future IAM Projects)</h2></summary>

✅ Project 1 — Identity Basics (Users, Groups, RBAC)  
✅ Project 2 — **MFA Enforcement** (this project)  
✅ Project 3 — Joiner → Mover → Leaver lifecycle  
🔜 Conditional Access Policies  
🔜 Passwordless Authentication  
🔜 Privileged Identity Management (PIM)  
🔜 Secure Tier-0 Admin Identities  

</details>

