# Script - Delete Local User

---

## Purpose

Deletes an existing local user account from a Windows computer.

---

## Requirements

- Windows 10 or Windows 11
- Command Prompt (Run as Administrator)
- Administrator privileges

---

## Script

```cmd
net user <Username> /delete
```

Replace `<Username>` with the name of the local user to remove.

Example:

```cmd
net user jdoe /delete
```

---

## Expected Output

```text
The command completed successfully.
```

The specified local user account is removed.

---

## Common Error

If Command Prompt is not run as Administrator:

```text
System error 5 has occurred.

Access is denied.
```

If the specified user does not exist:

```text
The user name could not be found.
```

---

## Notes

- Run the command using an elevated (Administrator) Command Prompt.
- Deleting a user account does **not** automatically remove the user's profile folder (`C:\Users\<Username>`). Remove the profile separately if required.
- Verify that the correct account is selected before deletion.

---

## Version History

| Version | Date | Changes |
|----------|------|---------|
| 1.0 | 2026-07-08 | Initial documentation |