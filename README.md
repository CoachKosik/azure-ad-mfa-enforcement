<p align="center">
  <img src="screenshots/mfa_banner.png" width="100%">
</p>

<h1 align="center">🛡 Project 2 — Enforce MFA for All Users</h1>
<h3 align="center">Microsoft Entra ID ▸ Zero Trust Authentication ▸ Security Hardening</h3>

---

## 📌 Overview

This lab enforces **Multi-Factor Authentication (MFA)** as a baseline security requirement for all identities.

It simulates **real-world IAM analyst responsibilities**, including:

✔ Designing secure Conditional Access rules  
✔ Documenting enforcement logic for auditors & hiring managers  
✔ Preventing legacy insecure authentication methods  
✔ Testing policy behavior for different user personas

This is **Project 2** in a **4-part Enterprise IAM portfolio series**.

---

## 📚 Table of Contents

- [Objectives](#-objectives)
- [Baseline MFA Policy](#-baseline-mfa-policy)
- [Conditional Access Configuration](#-conditional-access-configuration)
- [Legacy Authentication Blocking](#-legacy-authentication-blocking)
- [Test Validation](#-test-validation)
- [What I Learned](#-what-i-learned)
- [Next Project](#-next-project-identity-lifecycle-jml)
- [Repo Structure](#-repo-structure)

---

## 🎯 Objectives

| Objective | Outcome |
|-----------|---------|
| Require MFA for all users | Modern authentication enforced |
| Block legacy auth | Prevent password-only logins |
| Align to Zero Trust | Verify explicitly on every sign-in |
| Provide audit evidence | Screenshot lab documentation |

---

## 🟦 Baseline MFA Policy

| Setting | Value |
|---------|-------|
| Policy Name | `01 - Require MFA for All Users` |
| Assignment | All users |
| Grant Controls | Require MFA |
| Mode | Enabled |

**Screenshot**

![Policy Overview](screenshots/CA-Policy01-Overview.png)

---

## 🔐 Conditional Access Configuration
<details open>
<summary><strong>📋 Assignments</strong></summary>

✔ All users included  
✖ No service principals  

![Assignments](screenshots/CA-Policy01-Assignments.png)

</details>

<details>
<summary><strong>🎛 Conditions</strong></summary>

🌐 All cloud apps  
🟦 No device exclusions  

![Conditions](screenshots/CA-Policy01-Conditions.png)

</details>

<details>
<summary><strong>🛑 Grant Controls</strong></summary>

✔ Require Multi-Factor Authentication  
⛔ No password-only auth permitted  

![Grant Controls](screenshots/CA-Policy01-Grant.png)

</details>

---

## 🚫 Legacy Authentication Blocking

| Policy | Action |
|--------|--------|
| `03 – Block Legacy Auth` | Block access |

**Why?**  
🔸 99% of breached accounts were *not using MFA*  
🔸 SMTP, POP, IMAP = **password-only** = attacker heaven

![Block Legacy Auth](screenshots/CA-Policy03-Grant.png)

---

## 🧪 Test Validation

| Test User | Country | Result |
|-----------|---------|--------|
| Eddie Spark | USA | MFA Prompt |
| Maverick Blaze | USA | MFA Prompt |
| Nathan Dash | USA | MFA Prompt |

---

## 🧠 What I Learned

✔ MFA cannot rely on end-user enrollment  
✔ Conditional Access provides scalable enforcement  
✔ Legacy authentication must be blocked explicitly  
✔ Documentation is **as important as configuration**

---

## ➤ **Next Project — Identity Lifecycle (JML)**

🔗 https://github.com/CoachKosik/Project-3-Entra-ID-Azure-AD-Identity-Lifecycle-JML

---

## 📂 Repo Structure

```text
azure-ad-mfa-enforcement/
│ README.md
└── screenshots/
├─ mfa_banner.png
├─ CA-Policy01-Overview.png
├─ CA-Policy01-Assignments.png
├─ CA-Policy01-Conditions.png
├─ CA-Policy01-Grant.png
├─ CA-Policy03-Grant.png
```

---

⭐ **If this project helped you, please STAR the repo**  
👀 Recruiters *do* check your GitHub activity  
🧑‍💻 Follow the full Zero Trust IAM portfolio → https://github.com/CoachKosik
