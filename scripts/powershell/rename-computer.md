# Script - Rename Computer

---

## Purpose

Changes the hostname (computer name) of a Windows computer using PowerShell.

---

## Requirements

- Windows 10 or Windows 11
- PowerShell (Run as Administrator)
- Administrator privileges

> **Note:** A system restart is required for the new computer name to take effect.

---

## Script

```powershell
Rename-Computer -NewName "NewPCName" -Restart
```

Replace `"NewPCName"` with the desired computer name.

Example:

```powershell
Rename-Computer -NewName "IT04-NETADMIN" -Restart
```

---

## Expected Output

The computer is renamed and automatically restarts.

After restarting, Windows will display the new computer name.

---

## Common Error

If PowerShell is not run as Administrator:

```text
Rename-Computer : Access is denied.
```

or

```text
Rename-Computer : Administrator privilege required to perform this operation.
```

---

## Notes

- Run the command in an elevated (Administrator) PowerShell session.
- Ensure the new computer name follows your organization's naming convention.
- Save any open work before running the command, as the computer will restart automatically.
- If you do not want the computer to restart immediately, omit the `-Restart` parameter and restart the computer manually later.

Example without automatic restart:

```powershell
Rename-Computer -NewName "IT04-NETADMIN"
```

---

## Version History


| Version | Date | Changes |
|----------|------|---------|
| 1.1 | 2026-07-20 | Removed unnecessary spacing |
| 1.0 | 2026-07-08 | Initial documentation |