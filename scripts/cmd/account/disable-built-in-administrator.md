# Script - Disable Administrator Account

---

## Purpose

Disables the built-in Windows Administrator account after administrative tasks have been completed to improve system security.

---

## Requirements

- Windows 10 or Windows 11
- Command Prompt (Run as Administrator)
- Administrator privileges

---

## Script

```cmd
net user Administrator /active:no
```

---

## Expected Output

If executed successfully:

```text
The command completed successfully.
```

The built-in **Administrator** account is disabled and will no longer appear on the Windows sign-in screen.

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
- Ensure another administrator account is available before disabling the built-in Administrator account.
- Disabling the account helps reduce unnecessary security exposure.

---

## Version History

| Version | Date | Changes |
|----------|------|---------|
| 1.1 | 2026-07-03 | Added common error when not running Command Prompt as Administrator |
| 1.0 | 2026-07-03 | Initial documentation |