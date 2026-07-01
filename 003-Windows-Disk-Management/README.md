# 003 – Windows Disk Management

## Overview

This project demonstrates how a Help Desk technician inspects and verifies Windows disk configuration using both graphical and command-line tools. The lab covers reviewing physical disks, examining partition layouts, verifying storage capacity, identifying the file system, checking disk health, and documenting the results following Help Desk best practices.

---

## Objectives

- Review the installed physical disk.
- Examine the disk partition layout.
- Verify available storage capacity.
- Identify the file system in use.
- Check the overall health of the disk.
- Document all commands, outputs, screenshots, and findings.

---

## Tools Used

- Windows 10 Pro
- Disk Management
- Command Prompt
- VS Code

---

## Commands Used

```cmd
wmic logicaldisk get caption,freespace,size
fsutil fsinfo volumeinfo C:
chkdsk
wmic diskdrive get model,interfacetype,mediatype,size,status
```

---

## Project Structure

```text
Documentation/
Outputs/
Screenshots/
README.md
```

---

## Skills Demonstrated

- Windows Disk Management
- Storage Capacity Verification
- Disk Partition Analysis
- File System Identification
- Disk Health Assessment
- Command Prompt Administration
- Windows System Troubleshooting
- Technical Documentation
- Markdown Documentation

---

## Related Projects

- 001 – Windows Workstation System Audit
- 002 – Windows User Account Management 
- 003 – Windows Disk Management 
- 004 – Windows Computer Management *(Next Project)*