# Script - Add Local User

---

## Purpose

Creates a new local user account on a Windows computer.

---

## Requirements

- Windows 10 or Windows 11
- Command Prompt (Run as Administrator)
- Administrator privileges

---

## Script

```cmd
net user <Username> <Password> /add
```

Replace the placeholders with the desired username and password.

Example:

```cmd
net user IT P@ssw0rd123 /add
```

---

## Expected Output

```text
The command completed successfully.
```

The new local user account is created.

---

## Common Error

If Command Prompt is not run as Administrator:

```text
System error 5 has occurred.

Access is denied.
```

If the user already exists:

```text
The account already exists.
```

---

## Notes

- Run the command using an elevated (Administrator) Command Prompt.
- This command creates a **standard local user**.
- To grant administrator privileges, add the user to the local **Administrators** group.

Example:

```cmd
net localgroup Administrators <Username> /add
```

---

## Version History

| Version | Date | Changes |
|----------|------|---------|
| 1.0 | 2026-07-08 | Initial documentation |