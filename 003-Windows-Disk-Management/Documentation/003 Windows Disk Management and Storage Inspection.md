# Ticket #003 – Windows Disk Management and Storage Inspection

## Scenario

A user reports that their Windows workstation is running low on available storage space.

The Help Desk technician is assigned to review the workstation's disk configuration, verify storage allocation, inspect the file system, assess disk health, and document the current state before recommending corrective actions.

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

- Disk Management
- Command Prompt
- Windows 10 Pro
- VS Code

---

## Task 1 — Review Physical Disk and Partition Layout

### Tool

```text
Computer Management
→ Disk Management

or

Win + X
→ Disk Management
```

### Purpose

Review the installed physical disk, identify all partitions, and verify the current disk layout before performing any storage management tasks.

### Evidence

**Output File**
- [01-disk-overview.txt](../Outputs/01-disk-overview.txt)

**Screenshot**
![Disk Overview](../Screenshots/01-disk-overview.png)

### Result

The workstation contains one installed physical hard disk (Disk 0) with a total capacity of approximately 465 GB.

The disk is Online and contains the following partitions:

- System Reserved
- Windows (C:)
- Recovery Partition

No disk configuration issues were observed.

---

## Task 2 — Verify Disk Capacity

### Command

```cmd
wmic logicaldisk get caption,freespace,size
```

### Purpose

Display the total storage capacity and available free space for all logical drives.

### Evidence

**Output File**
- [02-disk-capacity.txt](../Outputs/02-disk-capacity.txt)

**Screenshot**
![Disk Capacity](../Screenshots/02-disk-capacity.png)

### Result

The Windows (C:) drive has sufficient available storage and its total capacity was successfully verified.

---

## Task 3 — Verify File System

### Command

```cmd
fsutil fsinfo volumeinfo C:
```

### Purpose

Identify the file system used by the Windows operating system partition.

### Evidence

**Output File**
- [03-file-system-info.txt](../Outputs/03-filesystem-info.txt)

**Screenshot**
![File System Info](../Screenshots/03-file-system-info.png)

### Result

Confirmed that the Windows operating system partition is formatted using the NTFS file system.

---

## Task 4 — Perform a Disk Health Check

### Command

```cmd
chkdsk
```

### Purpose

Verify the integrity of the file system and detect any disk-related errors.

### Evidence

**Output File**
- [04-disk-health.txt](../Outputs/04-disk-health.txt)

**Screenshot**
![Disk Health](../Screenshots/04-disk-health.png)

### Result

Windows reported no file system errors. The disk is healthy and functioning normally.

---

## Task 5 — Identify the Physical Disk Hardware

### Command

```cmd
wmic diskdrive get model,interfacetype,mediatype,size,status
```

### Purpose

Retrieve hardware information about the installed physical disk, including its model, interface type, media type, capacity, and operational status.

### Evidence

**Output File**
[05-disk-hardware.txt](../Outputs/05-disk-hardware.txt)

**Screenshot**
![Disk Hardware](../Screenshots/05-disk-hardware.png)

### Result

The installed physical disk was successfully identified and confirmed to be operating normally with a status of OK.

---

## Findings

- One physical hard disk was detected.
- The disk is online and operating normally.
- Three partitions were identified and verified:
  - System Reserved
  - Windows (C:)
  - Recovery Partition
- The Windows partition uses the NTFS file system.
- Available storage capacity was successfully verified.
- No disk integrity issues were detected.


## Lessons Learned

- Learned how to inspect physical disks using Disk Management.
- Learned how to identify disk partitions and their purpose.
- Learned how to verify disk capacity using Command Prompt.
- Learned how to identify the Windows file system.
- Learned how to perform a basic disk health check.
- Review disk usage before expanding or creating partitions.
- Improved Windows storage management and documentation skills.


## Recommendations

- Monitor available disk space regularly.
- Perform routine disk health checks.
- Remove unnecessary files when storage becomes limited.
- Avoid modifying partitions without proper backups.
- Document disk configurations before making storage-related changes.