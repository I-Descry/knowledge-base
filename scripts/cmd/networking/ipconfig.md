# Script - ipconfig

---

## Purpose

Displays and manages the IP configuration of network adapters on a Windows computer. Commonly used for network diagnostics and troubleshooting.

---

## Requirements

- Windows 10 or Windows 11
- Command Prompt

> **Note:** Some commands require Command Prompt to be run as **Administrator**.

---

## Syntax

```cmd
ipconfig [option]
```

---

## Commands

### Display Current IP Configuration

```cmd
ipconfig
```

Displays the current IPv4 address, subnet mask, and default gateway for active network adapters.

---

### Display Detailed Network Information

```cmd
ipconfig /all
```

Displays detailed information for all network adapters, including:

- Host Name
- Physical (MAC) Address
- DHCP Status
- IPv4 Address
- IPv6 Address
- DNS Servers
- Default Gateway
- DHCP Lease Information

---

### Release Current IP Address

```cmd
ipconfig /release
```

Releases the current DHCP-assigned IP address.

> **Note:** This command only applies to network adapters configured to obtain an IP address automatically (DHCP).

---

### Renew IP Address

```cmd
ipconfig /renew
```

Requests a new IP address from the DHCP server.

---

### Flush DNS Cache

```cmd
ipconfig /flushdns
```

Clears the local DNS Resolver Cache.

Expected output:

```text
Windows IP Configuration

Successfully flushed the DNS Resolver Cache.
```

---

### Display DNS Cache

```cmd
ipconfig /displaydns
```

Displays the contents of the local DNS Resolver Cache.

---

### Register DNS

```cmd
ipconfig /registerdns
```

Refreshes DHCP leases and re-registers the computer's DNS records.

---

## Common Error

Some commands require an elevated Command Prompt.

If Command Prompt is not run as Administrator:

```text
The requested operation requires elevation.
```

---

## IT Use Cases

Common scenarios where `ipconfig` is used:

- Verify a computer's IP address
- Check the default gateway
- Confirm DNS server configuration
- Troubleshoot network connectivity
- Renew a DHCP-assigned IP address
- Flush the DNS cache after DNS changes
- Gather network information for remote support

---

## Notes

- `ipconfig` is one of the most commonly used networking commands in Windows.
- `/all` provides the most detailed network information.
- `/release` and `/renew` only work on DHCP-enabled network adapters.
- `/flushdns` is useful when troubleshooting DNS resolution issues.
- Administrator privileges are required for some `ipconfig` options.

---

## Version History

| Version | Date | Changes |
|----------|------|---------|
| 1.0 | 2026-07-03 | Initial documentation |