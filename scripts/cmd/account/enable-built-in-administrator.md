# Script - Enable Administrator Account

---

## Purpose

Enables the built-in Windows Administrator account for troubleshooting, system administration, or recovery tasks.

---

## Requirements

- Windows 10 or Windows 11
- Command Prompt (Run as Administrator)
- Administrator privileges

---

## Script

```cmd
net user Administrator /active:yes
```

---

## Expected Output

If executed successfully:

```text
The command completed successfully.
```

The built-in **Administrator** account is enabled and available on the Windows sign-in screen.

---

## Common Error

If Command Prompt is **not** run as Administrator:

```text
System error 5 has occurred.

Access is denied.
```

---

## Notes

- Run the command using an elevated (Administrator) Command Prompt.
- This command only enables the built-in Administrator account; it does not create a new administrator account.
- This command does not set or change the Administrator account password.
- Disable the account after use if it is no longer required.

---

## Version History

| Version | Date | Changes |
|----------|------|---------|
| 1.1 | 2026-07-03 | Added common error when not running Command Prompt as Administrator |
| 1.0 | 2026-07-03 | Initial documentation |