# SOP - Reset Employee Email Password in cPanel

---

## Overview

This Standard Operating Procedure (SOP) outlines the process for resetting an employee's email account password using cPanel.

---

## Purpose

To ensure employee email passwords are reset securely, consistently, and in accordance with company security policies.

---

## Scope

This procedure applies to:

- Employee email password reset requests
- Company email accounts managed through cPanel
- IT administrators responsible for email account management

---

## Roles & Responsibility

- **IT/Admin:** Resets the employee's email password and communicates the temporary credentials.
- **HR / Supervisor:** May request or approve the password reset, if required.
- **Employee:** Logs in using the temporary password and changes it immediately after the first successful login.

---

## Inputs / Preconditions

Before starting, ensure the following are available:

- Approved password reset request
- Employee email address
- cPanel administrator credentials
- Company default password

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

### 3. Locate the Employee Email Account

Use the search box to locate the employee's email account.

Verify that the correct email account has been selected before proceeding.

---

### 4. Open Email Account Management

Click **Manage** on the right side of the employee's email account.

---

### 5. Reset the Password

Enter the **company default password**.

Ensure the password complies with the company's password policy.

---

### 6. Save the Changes

Click **Update Email Settings**.

Wait for the confirmation message indicating that the password has been successfully updated.

---

### 7. Verify Password Reset

Confirm that:

- No errors occurred during the password reset.
- The password update was completed successfully.

---

### 8. Communicate Temporary Credentials

Provide the employee with:

- Email address
- Temporary (default) password

Use only approved communication methods when sharing credentials.

---

### 9. Instruct the Employee to Change the Password

Advise the employee to:

- Sign in using the temporary password.
- Change the password immediately after the first successful login.

---

## Expected Output

- Employee password successfully reset.
- Employee receives the temporary password.
- Employee can access the mailbox.
- Employee changes the password after logging in.

---

## Verification

Verify the following:

- Password update completed successfully.
- Employee has received the temporary password.
- No errors occurred during the password reset process.

---

## Estimated Duration

Approximately **2–3 minutes** per password reset.

---

## Rollback Procedure

If the password reset fails:

1. Verify the employee's email address.
2. Repeat the password reset process.
3. Confirm the password was updated successfully.
4. If the issue persists, investigate mailbox status or escalate as necessary.

---

## Security Considerations

- Verify the identity of the requester before resetting a password.
- Use only the approved company default password.
- Never disclose passwords to unauthorized individuals.
- Use secure communication channels when sending credentials.
- Instruct employees to change the temporary password immediately after logging in.

---

## Dependencies

- cPanel administrator access
- Active email hosting service
- Employee email account
- Company password policy

---

## Common Issues

- Employee email account not found.
- Password update failed.
- Employee unable to log in after reset.
- Incorrect email address provided.

---

## Troubleshooting

### Email Account Not Found

Verify that the correct email address was provided.

---

### Password Update Failed

Retry the password reset and ensure the password meets the required policy.

---

### Employee Unable to Log In

Verify:

- The correct email address is being used.
- The temporary password was entered correctly.
- The employee is accessing the correct webmail or email client.

---

## Lessons Learned

Using a standardized default password and requiring employees to change it immediately after logging in improves account security while simplifying password reset requests.

---

## Related Documents

- SOP → Create Employee Email Account in cPanel

---

## References

- cPanel Documentation
- Company Password Policy

---

## Notes

Password resets should only be performed after verifying the identity of the employee or confirming an authorized request. Temporary passwords should never be reused beyond the initial login.

---

## Version History

| Version | Date | Changes |
|----------|------|---------|
| 1.0 | 2026-07-03 | Initial documentation |