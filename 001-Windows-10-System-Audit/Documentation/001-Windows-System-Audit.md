# 001 – Windows System Audit

## Scenario

A workstation has been prepared for deployment.

Before assigning it to a user, system information needs to be documented for inventory and future troubleshooting.

---

## Objective

Collect important Windows system information.

---

## Tools Used

- Settings
- Command Prompt
- Task Manager
- Device Manager
- Computer Management

---

## Commands Used

```cmd
hostname
whoami
systeminfo
ipconfig /all
net user
```

---

## Evidence Collected

### Output Files

- hostname.txt
- whoami.txt
- systeminfo.txt
- ipconfig.txt
- netuser.txt
---
### Screenshots

- VS Code documentation
- Command Prompt (running audit commands)
- Project folder structure

## Outcome

Successfully completed a Windows 10 workstation audit by collecting system identity, operating system details, network configuration, and local user information. All outputs were documented and stored for future troubleshooting and inventory purposes.

### Findings

- Computer Name: STURNNER
- Logged-in User: hp\sturnner
- Operating System: Windows 10 Pro (64-bit)
- System Manufacturer: Hewlett-Packard
- Model: HP EliteBook Folio 9480m
- Installed RAM: 8 GB
- Network Configuration: Collected (see ipconfig.txt)
- Local User Accounts: Collected (see netuser.txt)
- Audit Status: Successful
---

## Lessons Learned

- Used Command Prompt to collect system information.
- Learned how to document technical findings using Markdown.
- Practiced saving command outputs as evidence files.
- Improved understanding of Windows system inventory and basic workstation auditing.

## Recommendations

- Verify Windows is fully updated before deployment.
- Confirm antivirus is enabled and up to date.
- Ensure device drivers are current.
- Remove unused local user accounts if applicable.
- Record the asset in the organization's inventory system.
