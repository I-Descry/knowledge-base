# SOP - Configure Company cPanel Email in Classic Outlook (IMAP/SMTP)

---

## Overview

This procedure describes how to manually configure a company cPanel email account in Microsoft Outlook Classic using the IMAP protocol. The configured email account is a designated forwarder of a group email, allowing the user to receive emails forwarded from the group email while sending emails using their own company email address.

---

## Purpose

To manually configure a company cPanel email account in Microsoft Outlook Classic using the secure IMAP and SMTP settings retrieved from cPanel.

---

## Scope

This SOP applies to IT personnel responsible for configuring company email accounts in Microsoft Outlook Classic for employees.

---

## Roles & Responsibility

| Role | Responsibility |
|------|----------------|
| IT Administrator | Retrieve the email server settings from cPanel, configure Outlook, and verify email functionality. |
| Employee | Provide the assigned company email credentials and verify successful email sending and receiving. |

---

## Inputs / Preconditions

- Administrator access to the company's cPanel account.
- Company email account already created in cPanel.
- The company email account is configured as a forwarder of a group email.
- Username and password of the company email account.
- Microsoft Outlook Classic installed.
- Internet connection.

---

## Procedure

### Part 1 - Retrieve the IMAP/SMTP Settings from cPanel

1. Log in to the company cPanel using the administrator account.

2. Navigate to:

```
Dashboard
→ Tools
→ Email
→ Email Accounts
```

3. Search for the company email account that is configured as a forwarder of the group email.

4. Click **Manage**.

5. Under **Manage an Email Account**, click **Check Email**.

6. A new browser tab will open.

7. From the left sidebar, select:

```
Webmail Home
```

8. Scroll down to **Other Webmail Features**.

9. Select **Configure Mail Client**.

10. Scroll to **Secure SSL/TLS Settings (Recommended)**.

11. Record the following information:

### Incoming Mail

- Incoming Server (Domain)
- IMAP Port
- POP3 Port (optional)

### Outgoing Mail

- Outgoing Server (Domain)
- SMTP Port

---

### Part 2 - Configure Microsoft Outlook Classic

1. Open **Microsoft Outlook Classic**.

2. Select:

```
File
→ Add Account
```

3. Enter the complete company email address.

4. Select **Advanced Options**.

5. Check:

```
Let me set up my account manually
```

6. Click **Connect**.

7. Select **IMAP**.

8. Configure the Incoming Mail settings.

| Setting | Value |
|---------|-------|
| Server | IMAP Server from cPanel |
| Port | 993 |
| Encryption | SSL/TLS |
| SPA | Leave Unchecked |

9. Configure the Outgoing Mail settings.

| Setting | Value |
|---------|-------|
| Server | SMTP Server from cPanel |
| Port | 465 |
| Encryption | SSL/TLS |
| SPA | Leave Unchecked |

10. Enter the email account password.

11. Complete the Outlook setup.

---

### Part 3 - Verify the Configuration

1. Confirm that Outlook successfully synchronizes the mailbox.

2. Verify that emails sent to the group email are received by the configured company email account through the forwarder.

3. Send a test email to an internal recipient.

4. Send a test email to an external recipient.

5. Confirm that both emails are delivered successfully.

---

## Expected Output

- The company email account is successfully configured in Microsoft Outlook Classic.
- Outlook synchronizes the mailbox without errors.
- Emails sent to the group email are successfully forwarded to the configured company email account.
- The configured company email can successfully send emails to both internal and external recipients.

---

## Verification

Verify the following:

- Outlook connects without prompting for repeated credentials.
- Incoming emails are received successfully.
- Outgoing emails are delivered successfully.
- Email synchronization functions correctly.
- Group email forwarding is working as expected.

---

## Estimated Duration

Approximately **10–20 minutes** per email account.

---

## Rollback Procedure

If the configuration fails:

1. Remove the email account from Outlook.
2. Verify the IMAP/SMTP settings in cPanel.
3. Reconfigure the email account.
4. If necessary, reset the email password in cPanel before attempting the configuration again.

---

## Security Considerations

- Only authorized IT personnel should access the administrator cPanel account.
- Keep company email credentials confidential.
- Do not save passwords in unsecured locations.
- Always use the Secure SSL/TLS configuration recommended by cPanel.

---

## Dependencies

- cPanel Email Accounts
- cPanel Webmail
- Microsoft Outlook Classic
- Internet connection

---

## Common Issues

| Issue | Possible Cause |
|-------|----------------|
| Authentication failed | Incorrect username or password |
| Unable to connect to server | Incorrect IMAP/SMTP server or port |
| Outlook repeatedly requests password | Incorrect credentials or authentication issue |
| Emails are not received | Forwarder is not configured correctly |
| Unable to send emails | Incorrect SMTP settings or blocked port |

---

## Troubleshooting

- Verify the email credentials.
- Confirm the IMAP and SMTP server settings from cPanel.
- Ensure SSL/TLS is selected.
- Verify that the email account is configured as a forwarder of the group email.
- Test the connection using Outlook's account settings.
- Restart Outlook after completing the configuration.

---

## Lessons Learned

- Always retrieve the latest IMAP and SMTP settings directly from cPanel instead of relying on previously documented server information.
- Test both incoming and outgoing email functionality before handing over the device to the user.
- Verify that the forwarder configuration is functioning correctly before troubleshooting Outlook.

---

## Related Documents

- SOP - Create Employee Email Account in cPanel
- SOP - Reset Employee Email Password in cPanel
- SOP - Create Group Email Forwarders in cPanel

---

## References

- cPanel Email Accounts
- Microsoft Outlook Classic

---

## Notes

This procedure is intended for company email accounts hosted in cPanel that are configured as forwarders of a group email. The configured account receives forwarded emails while sending emails using its own company email address.

---

## Version History

| Version | Date | Changes |
|----------|------|---------|
| 1.0 | 2026-07-29 | Initial documentation |