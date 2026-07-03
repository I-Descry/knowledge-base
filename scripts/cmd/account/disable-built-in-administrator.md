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

```text
The command completed successfully.
```

The built-in **Administrator** account is disabled and will no longer appear on the Windows sign-in screen.

---

## Notes

- Run the command using an elevated Command Prompt.
- Ensure another administrator account is available before disabling the built-in Administrator account.
- Disabling the account helps reduce unnecessary security exposure.

---

## Version History

| Version | Date | Changes |
|----------|------|---------|
| 1.0 | 2026-07-03 | Initial documentation |