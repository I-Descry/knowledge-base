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

```text
The command completed successfully.
```

The built-in **Administrator** account is enabled and available on the Windows sign-in screen.

---

## Notes

- Run the command using an elevated Command Prompt.
- This command only enables the built-in Administrator account; it does not create a new administrator account.
- This command does not set or change the Administrator account password.
- Disable the account after use if it is no longer required.

---

## Version History

| Version | Date | Changes |
|----------|------|---------|
| 1.0 | 2026-07-03 | Initial documentation |