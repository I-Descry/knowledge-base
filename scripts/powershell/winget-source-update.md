# Script - Update Winget Sources

---

## Purpose

Updates the Windows Package Manager (Winget) package sources to ensure the latest package information is available.

---

## Requirements

- Windows 10 or Windows 11
- PowerShell
- Winget installed
- Internet connection

---

## Script

```powershell
winget source update
```

---

## Expected Output

```text
Updating all sources...
Done
```

The Winget package sources are refreshed successfully.

---

## Common Error

```text
No internet connection.
```

or

```text
The 'winget' command is not recognized...
```

This typically indicates that Winget is not installed or is unavailable in the current environment.

---

## Notes

- Run this command before installing or upgrading packages if the package list may be outdated.
- An internet connection is required to retrieve the latest package metadata.
- This command updates the package sources only; it does not update installed applications.

---

## Version History


| Version | Date | Changes |
|----------|------|---------|
| 1.0 | 2026-07-23 | Initial documentation |