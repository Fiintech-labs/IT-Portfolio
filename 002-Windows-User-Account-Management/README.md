# Windows User Account Management

## Overview

This project demonstrates how a Help Desk technician creates and manages local Windows user accounts using built-in Windows command-line tools.

The lab covers account verification, user creation, permission validation, and documentation.

---

## Objectives

- Review existing local Windows user accounts.
- Verify that the requested username is available.
- Create a new local Windows user account.
- Verify the new account was created successfully.
- Confirm the default local group membership.
- Document all commands, outputs, screenshots, and findings.

---

## Tools

- Windows 10 Pro
- Command Prompt
- VS Code

---

## Commands Used

```cmd
net user
net user jsmith
net user jsmith Welcome@123 /add
net localgroup Users
```

---

## Project Structure

```
Documentation/
Outputs/
Screenshots/
README.md
```

---

## Skills Demonstrated

- Windows User Administration
- Command Prompt
- Local Account Management
- Technical Documentation
- Markdown

---

 ## Next Project

**003 – Windows Disk Management**