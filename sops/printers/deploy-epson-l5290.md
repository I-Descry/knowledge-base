# SOP - Deploy Epson L5290 Wireless Network Printer

---

## Overview

This Standard Operating Procedure (SOP) outlines the process for deploying an Epson L5290 wireless network printer, including hardware setup, wireless network configuration, static IP assignment, driver installation, and verification.

---

## Purpose

To ensure Epson L5290 printers are deployed consistently, securely, and configured correctly for use on the company network.

---

## Scope

This procedure applies to:

- New Epson L5290 printer deployments
- Wireless printer installations
- Company-managed Windows devices
- IT administrators responsible for printer deployment

---

## Roles & Responsibility

- **IT/Admin:** Installs, configures, and verifies the printer.
- **End User / Department:** Confirms the printer functions correctly after deployment.

---

## Inputs / Preconditions

Before starting, ensure the following are available:

- Epson L5290 printer
- Epson ink bottles
- Power outlet
- Wireless network (SSID and Password)
- Internet connection
- Administrator access to the network
- Winbox access
- Windows computer for installation

---

## Procedure

### 1. Unbox the Printer

- Open the printer box.
- Remove all packaging materials.
- Place the printer on a stable, flat surface near a power outlet.

---

### 2. Fill the Ink Tanks

- Open the ink tank covers.
- Fill each ink tank with its corresponding ink bottle.
- Ensure each ink color is placed in the correct tank.
- Close the ink tank covers after filling.

---

### 3. Power On the Printer

- Connect the power cable.
- Turn on the printer.
- Wait for the printer to complete its initial startup.

---

### 4. Complete Initial Printer Setup

Using the printer control panel, configure the following:

- Language
- Country/Region
- Date
- Time

Complete the initial setup wizard before proceeding.

---

### 5. Connect the Printer to Wi-Fi

Using the printer control panel, navigate to:

**Network Settings → Wi-Fi Setup → Wi-Fi (Recommended)**

When prompted, select **Yes**.

Choose:

**Wi-Fi Setup Wizard**

Wait for the printer to search for available wireless networks.

Select:

**Other SSIDs...**

Enter:

- SSID (Wireless Network Name)
- Wi-Fi Password

Wait for the printer to connect successfully to the wireless network.

---

### 6. Download and Install Epson Drivers

On the administrator computer:

1. Open a web browser.
2. Search for:

```text
Epson L5290 Driver
```

3. Open the official Epson Support website.
4. Select the operating system of the target computer (if it is not detected automatically).
5. Download the following:

- Printer Driver
- Scanner Driver

6. Run the downloaded installers.
7. Complete the installation by following the on-screen instructions.
8. Restart the computer if prompted.

---

### 7. Assign a Static IP Address

Open **Winbox**.

Navigate to:

**IP → DHCP Server → Leases**

Locate the printer in the lease list.

Verify the correct printer using its hostname or MAC address.

Right-click the lease and select **Make Static** (or change the lease from **Dynamic** to **Static**, depending on the RouterOS version).

Assign the printer according to the department's IP addressing scheme.

Example:

```text
Department: <Department Name>
IP Address: 192.168.x.xxx
```

Apply the changes.

---

### 8. Restart the Printer

Restart the printer to apply the newly assigned static IP address.

Wait for the printer to reconnect to the network.

---

### 9. Add the Printer to Windows

Open:

**Settings → Bluetooth & devices → Printers & scanners**

Select:

**Add Device**

Choose:

**Add a printer manually**

Select:

**Add a printer using a TCP/IP address or hostname**

Change **Device Type** to:

**TCP/IP Device**

Enter the printer's assigned static IP address in the **Hostname or IP Address** field.

Click **Next**.

---

### 10. Select the Printer Driver

When prompted:

Select **Epson L5290** from the list.

If Windows detects an existing driver, choose:

**Use the driver that is currently installed (Recommended)**

Click **Next**.

---

### 11. Configure Printer Name

Enter the printer name according to the company naming convention.

Example:

```text
<Department Name> Printer (Epson L5290)
```

Click **Next**.

---

### 12. Configure Printer Sharing

When prompted to share the printer:

Leave the default option unchanged unless printer sharing is required.

Click **Next**.

---

### 13. Print a Test Page

Click:

**Print a Test Page**

Verify:

- Printer responds successfully.
- Print quality is acceptable.
- Printer is accessible over the network.

Click **Finish**.

---

## Expected Output

- Printer successfully configured.
- Connected to the company Wi-Fi.
- Static IP address assigned.
- Printer and scanner drivers installed.
- Printer added successfully to Windows.
- Test page printed successfully.

---

## Verification

Verify the following:

- Printer appears in **Printers & Scanners**.
- Printer has the assigned static IP address.
- Printer responds to a ping request.
- Test page prints successfully.
- Scanner is detected and operational (if applicable).

---

## Estimated Duration

Approximately **20–30 minutes** per printer deployment.

---

## Rollback Procedure

If deployment fails:

1. Verify the Wi-Fi connection.
2. Confirm the static IP assignment.
3. Remove the printer from Windows.
4. Restart the printer.
5. Repeat the installation process.

---

## Security Considerations

- Connect the printer only to authorized company wireless networks.
- Assign a static IP address following the company's IP addressing scheme.
- Restrict administrative access to authorized IT personnel.
- Download drivers only from the official Epson Support website.

---

## Dependencies

- Epson L5290 printer
- Wireless network
- Internet connection
- Winbox
- DHCP Server
- Windows computer

---

## Common Issues

- Printer cannot connect to Wi-Fi.
- Incorrect SSID or Wi-Fi password.
- Printer receives the wrong IP address.
- Driver installation fails.
- Windows cannot detect the printer.
- Test page fails to print.

---

## Troubleshooting

### Printer Cannot Connect to Wi-Fi

- Verify the SSID.
- Confirm the Wi-Fi password.
- Ensure the printer is within wireless network range.

---

### Printer Not Found in DHCP Leases

- Verify the printer is connected to the network.
- Restart the printer.
- Refresh the DHCP lease list.

---

### Unable to Add Printer by IP Address

- Ping the assigned IP address.
- Verify the static IP assignment.
- Confirm the printer is online.

---

### Test Page Does Not Print

- Verify the correct Epson driver is installed.
- Confirm the printer status is **Online**.
- Restart the Windows Print Spooler service if necessary.

---

## Lessons Learned

Assigning a static IP address before deploying the printer prevents connection issues caused by changing DHCP leases. Installing the official Epson drivers before adding the printer by IP address also reduces installation issues and ensures full printer and scanner functionality.

---

## Related Documents

- 
- 
- 
- 
- 

---

## References

- Epson L5290 User Guide
- Epson Support Website

---

## Notes

Always assign a static IP address after the printer successfully connects to the wireless network. This ensures users can consistently connect to the printer without needing to update printer settings if the DHCP lease changes.

---

## Version History

| Version | Date | Changes |
|----------|------|---------|
| 1.0 | 2026-07-03 | Initial documentation |
| 1.1 | 2026-07-03 | Updated examples |