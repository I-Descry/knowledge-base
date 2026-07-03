# SOP - Create Department Group Email and Configure Email Forwarders

---

## Overview

This Standard Operating Procedure (SOP) outlines the process for creating a department group email account in cPanel and configuring email forwarders to distribute incoming emails to designated employee mailboxes.

---

## Purpose

To ensure department group email accounts are created consistently and that incoming emails are automatically forwarded to the appropriate employees.

---

## Scope

This procedure applies to:

- Department group email accounts
- Shared departmental mailboxes
- Company email domains managed through cPanel
- IT administrators responsible for email management

---

## Roles & Responsibility

- **IT/Admin:** Creates the group email account and configures email forwarders.
- **Department Head / Supervisor:** Provides the required group email name and recipient list.
- **Employees:** Receive forwarded emails through their individual mailboxes.

---

## Inputs / Preconditions

Before starting, ensure the following are available:

- Approved request for a department group email
- Group email name
- List of employee email addresses
- Company email domain
- cPanel administrator credentials

---

## Procedure

### 1. Log in to cPanel

Open the cPanel login page.

Log in using the **administrator (Admin) account**.

Enter the administrator credentials:

```text
Username: <Admin Username>
Password: <Admin Password>
```

After successful authentication, the **cPanel Dashboard** will be displayed.

---

### 2. Open Email Accounts

From the **cPanel Dashboard**, navigate to:

**Tools → Email Accounts**

---

### 3. Create the Group Email Account

Click **Create**.

Enter the following information:

- **Username**

Example:

```text
departmentgroupemail
```

The complete email address will be:

```text
departmentgroupemail@companydomain.com
```

---

### 4. Configure the Password

Enter the company-approved password.

> **Note:** cPanel requires a password strength of **65** or higher.

---

### 5. Create the Mailbox

Review the information.

Click **Create**.

Wait for the confirmation message indicating that the mailbox has been successfully created.

---

### 6. Open Forwarders

Return to the **cPanel Dashboard**.

Navigate to:

**Forwarders**

---

### 7. Add a Forwarder

Click **Add Forwarder**.

---

### 8. Configure the Forwarder

Under **Address to Forward**, enter the newly created group email username.

Example:

```text
departmentgroupemail
```

Select the appropriate company domain.

Under **Destination**, select:

**Forward to Email Address**

Enter the employee's email address.

Example:

```text
employee@companydomain.com
```

---

### 9. Create the Forwarder

Click **Add Forwarder**.

Wait for the confirmation message.

---

### 10. Add Additional Forwarders

Repeat **Steps 7–9** for every employee who should receive emails from the department group mailbox.

---

### 11. Verify the Configuration

Confirm that:

- The department group mailbox exists.
- All required forwarders have been created.
- Each employee email address appears in the Forwarders list.

---

## Expected Output

- Department group email created successfully.
- Email forwarders configured successfully.
- Emails sent to the department group email are automatically forwarded to the designated employees.

---

## Verification

Verify the following:

- The group email appears in **Email Accounts**.
- The forwarders appear in the **Forwarders** list.
- A test email sent to the group email is successfully received by all configured recipients.

---

## Estimated Duration

Approximately **5–10 minutes** depending on the number of forwarders.

---

## Rollback Procedure

If the configuration is incorrect:

1. Delete the incorrect forwarder.
2. Recreate the forwarder using the correct email address.
3. If necessary, delete and recreate the group mailbox.

---

## Security Considerations

- Verify the request is approved before creating a group email.
- Only add authorized employees as forwarders.
- Use passwords that comply with the company's password policy.
- Review forwarders periodically to remove users who no longer require access.

---

## Dependencies

- cPanel administrator access
- Company email domain
- Active email hosting service
- Approved group email request

---

## Common Issues

- Password does not meet the required strength.
- Group email already exists.
- Incorrect employee email address entered.
- Forwarder not receiving emails.

---

## Troubleshooting

### Group Email Already Exists

Verify whether the mailbox already exists before creating a new one.

---

### Forwarded Emails Not Received

- Verify the employee's email address.
- Confirm the forwarder exists.
- Send a test email to verify delivery.

---

### Incorrect Forwarder

Delete the incorrect forwarder and recreate it using the correct email address.

---

## Lessons Learned

Using department group email addresses with forwarders allows multiple employees to receive the same emails without requiring users to manage separate shared mailbox credentials. It also simplifies onboarding and offboarding by allowing IT to update forwarders rather than changing the department's published email address.

---

## Related Documents

- SOP → Create Employee Email Account in cPanel

---

## References

- cPanel Documentation
- Company Email Management Policy

---

## Notes

When adding or removing employees from a department, update the forwarders instead of changing the published department email address. This maintains a consistent point of contact while ensuring the correct employees receive incoming messages.

---

## Version History

| Version | Date | Changes |
|----------|------|---------|
| 1.0 | 2026-07-03 | Initial documentation |
| 1.1 | 2026-07-03 | Updated title | 
| 1.2 | 2026-07-03 | Improved procedures |