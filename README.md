<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

# 🛡️ Group Policy & Account Management in Active Directory

Here, I explored managing user accounts and security policies within an Active Directory domain using Group Policy. Key objectives include configuring account lockout policies, resetting user passwords, unlocking accounts, and auditing failed login attempts — essential tasks for IT administrators.

---

## Lab Overview

### 1. Opening Group Policy Management
![Open GPO](Group%20Policy%20and%20Managing%20Accounts/1.%20In%20our%20Domain%20run%20Group%20Policy%20.png)

We begin by launching **Group Policy Management** from the Domain Controller. This tool allows us to edit domain-wide security settings.

---

### 2. Editing the Default Domain Policy
![Edit Policy](Group%20Policy%20and%20Managing%20Accounts/2.%20Edit%20Default%20Domain%20policy.png)

We select and edit the **Default Domain Policy**, which applies to all users and computers in the domain.

---

### 3. Setting Account Lockout Duration
![Lockout Duration](Group%20Policy%20and%20Managing%20Accounts/3.%20Setting%20Lockout%20duration%20.png)

We configure how long an account remains locked out after failed login attempts.

---

### 4. Defining Max Failed Login Attempts
![Max Attempts](Group%20Policy%20and%20Managing%20Accounts/4.%20Setting%20the%20max%20login%20attempts.png)

We set the **threshold for invalid logon attempts** before an account gets locked out — a critical setting for preventing brute-force attacks.

---

### 5. Forcing Group Policy Update
![Force GPO](Group%20Policy%20and%20Managing%20Accounts/5.%20Force%20Group%20Policy%20Update%20using%20admin%20.png)

After configuring the policy, we **force a Group Policy update** across the domain using PowerShell to apply the changes immediately.

---

### 6. Locking Out a Test Account
![Locked Out](Group%20Policy%20and%20Managing%20Accounts/6.%20Locked%20ourself%20out%20for%20testing%20.png)

To test our settings, we intentionally lock ourselves out by entering incorrect passwords multiple times.

---

### 7. Finding Locked-Out Users
![Find User](Group%20Policy%20and%20Managing%20Accounts/7.%20Find%20locked%20out%20user%20.png)

We use Active Directory Users and Computers to **identify which accounts are locked**.

---

### 8. Unlocking a User Account
![Unlock User](Group%20Policy%20and%20Managing%20Accounts/8.%20Unlock%20our%20user.png)

The locked-out account is manually unlocked by an administrator.

---

### 9. Resetting a User’s Password
![Reset Password](Group%20Policy%20and%20Managing%20Accounts/9.%20Reset%20user%20password%20.png)

We reset the password for the locked user — a common support task.

---

### 10. Reset + Unlock Confirmation
![Reset and Unlock](Group%20Policy%20and%20Managing%20Accounts/10.%20Reset%20Password%20&%20Unlock%20.png)

Both unlocking the account and resetting the password are confirmed, restoring user access.

---

### 11–12. Auditing Failed Logins via Event Viewer
![Failed Login Logs](Group%20Policy%20and%20Managing%20Accounts/11.%20Observing%20failed%20login%20Logs.png)
![More Logs](Group%20Policy%20and%20Managing%20Accounts/12.%20Logs%20for%20failed%20login%20attempts%20.png)

We use **Event Viewer** to audit failed login attempts and confirm that our lockout policies are being logged for review.

---

## 🚀 Skills Demonstrated

- Group Policy Management (GPMC)
- Account Lockout Policy Configuration
- User Unlocking & Password Reset
- Event Viewer Log Analysis
- Active Directory User Management

---

## 💼 Why This Matters

Group Policy and account management are critical for maintaining a secure and functional enterprise network. This lab proves I can manage users effectively, respond to incidents, and enforce domain-wide security settings.

---
