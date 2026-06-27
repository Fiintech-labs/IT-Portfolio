# Ticket #002 – Windows User Account Management

## Scenario

A new employee has joined the company.

The Help Desk team is responsible for verifying that the requested username is available before creating a new local Windows account. This prevents duplicate accounts and ensures proper account management.

---

## Objectives

- Review existing local Windows user accounts.
- Verify that a requested username is available.
- Create a new local user account using Command Prompt.
- Verify that the new user account was created successfully.
- Verify the default permission level assigned to a new local user.
- Validate the user's group membership.
- Document all commands, outputs, screenshots, and findings.
- Apply Help Desk best practices for user account management and documentation.

---

## Tools Used

* Command Prompt
* Windows 10 Pro
* VS Code

---

## Task 1 – Review Existing Local User Accounts

### Command

```cmd
net user
```

### Purpose

Display all existing local user accounts on the workstation before making any changes.

### Evidence

**Output File**

* [net-user-before.txt](../Outputs/net-user-before.txt)

**Screenshot**

![Existing Local User Accounts](../Screenshots/01-existing-users.png)

### Result

The workstation contains the following local accounts:

* Administrator
* DefaultAccount
* Guest
* hp
* WDAGUtilityAccount

These accounts were documented to establish a baseline of the workstation before any user account changes were made.

---

## Task 2 – Verify Username Availability

### Command

```cmd
net user jsmith
```

### Purpose

Confirm that the requested username **jsmith** does not already exist before creating a new account.

### Evidence

**Output File**

* [user-check-before.txt](../Outputs/user-check-before.txt)

**Screenshot**

![Username Verification](../Screenshots/02-user-verification.png)

### Result

Windows returned a message indicating that the username **jsmith** could not be found.

This confirms the username is available and can safely be created.

---

## Task 3 – Create a New Local User

### Command

```cmd
net user jsmith Welcome@123 /add
```

### Purpose

Create a new local Windows user account for the new employee.

### Evidence

**Output File**

- [create-user.txt](../Outputs/create-user.txt)

**Screenshot**

![Create Local User](../Screenshots/03-create-user.png)

### Result

The local user account **jsmith** was successfully created.

---

## Task 4 – Verify User Account and Group Membership

### Command

```cmd
net user jsmith
```

### Purpose

- Verify the account exists.
- Review account properties.
- Confirm the assigned local group membership.

### Evidence

**Output File**

- [verify-user.txt](../Outputs/verify-user.txt)

**Screenshot**

![Verify User](../Screenshots/04-verify-user.png)

### Result

The account **jsmith** exists and its properties were successfully verified.

Windows automatically assigned the account to the **Users** local group, confirming the default permission level for newly created local accounts.


## Findings

- Existing local user accounts were documented.
- Username **jsmith** was available.
- A new local user account was successfully created.
- The account was automatically assigned to the **Users** local group.
- The user account properties and group membership were successfully verified.
---

## Lessons Learned

- Learned how to view existing Windows local accounts.
- Learned how to create local user accounts using Command Prompt.
- Learned how Windows automatically assigns new users to the Users group.
- Practiced verifying user account information.
- Improved Markdown documentation skills.

---

## Recommendations

- Verify username availability before creating new accounts.
- Apply the principle of least privilege when assigning permissions.
- Remove unused or inactive local accounts periodically.
- Store audit evidence for future troubleshooting and compliance.
- Follow a consistent documentation standard for all Help Desk activities.