# Windows 10 System Audit

## Overview

This project demonstrates how to perform a basic workstation audit before a computer is deployed to an end user.

The audit collects essential hardware, operating system, network, and user account information for inventory, documentation, and future troubleshooting.

---

## Scenerio

A Windows 10 workstation has been prepared for deployment.

Before assigning the device to an employee, the IT Support technician must verify the workstation specifications, document the system configuration, collect network information, and record local user details.

---

## Objectives

- Verify workstation identity.
- Collect operating system information.
- Document hardware specifications.
- Review network configuration.
- Identify local user accounts.
- Record audit evidence using screenshots and command outputs.

---

## Tools Used

- Windows Settings
- Command Prompt
- Task Manager
- Visual Studio Code
- Windows 10 Pro

---

## Command Used

```cmd
hostname
whoami
systeminfo
ipconfig /all
net user
```

---

## Skills

- Windows Administration
- Command Prompt
- System Information Collection
- Documentation

---


## Project Structure

```
001-Windows-10-System-Audit/
│
├── Documentation/
├── Outputs/
├── Screenshots/
└── README.md
```
---

## Documentation

Full project documentation is available in:

`Documentation/001-Windows-10-System-Audit.md`

---

## Status

✅ Complete

---

## Related Projects

- 001 – Windows Workstation System Audit
- 002 – Windows User Account Management *(Next Project)*