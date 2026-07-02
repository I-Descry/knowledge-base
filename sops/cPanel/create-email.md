# SOP - Create Employee Email Account in cPanel

---

## Overview

This Standard Operating Procedure (SOP) outlines the process for creating a new employee email account in cPanel.

---

## Purpose

To ensure employee email accounts are created consistently, securely, and in accordance with company standards.

---

## Scope

This procedure applies to:

- New employee email accounts
- Company email domains managed through cPanel
- IT administrators responsible for email account management

---

## Roles & Responsibility

- **IT/Admin:** Creates the employee email account and communicates the credentials.
- **HR / Supervisor:** Provides the approved email account request.
- **Employee:** Uses the provided credentials and changes the password after the first login.

---

## Inputs / Preconditions

Before starting, ensure the following are available:

- Approved request from HR or Supervisor
- Employee name
- Desired email username
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

### 3. Create a New Email Account

Click **Create** to open the email account creation page.

---

### 4. Enter Email Account Information

Provide the following details:

- **Username:** Enter the employee's email username.
- **Password:** Enter a temporary password that complies with the company's password policy.

> **Note:** cPanel requires a password strength of **65** or higher. If the password strength is below the required minimum, create a stronger password before proceeding.

---

### 5. Create the Email Account

Review the entered information.

Click **Create**.

Wait for the confirmation message indicating that the email account has been successfully created.

---

### 6. Verify Account Creation

Confirm that:

- The new email account appears in the **Email Accounts** list.
- No errors occurred during account creation.

---

### 7. Communicate Credentials

Provide the employee or authorized requester with:

- Email address
- Temporary password
- Login instructions (if applicable)

Only share credentials through approved communication channels.

---

### 8. Advise Password Change

Instruct the employee to change the temporary password after the first successful login.

---

## Expected Output

- Employee email account created successfully.
- Mailbox appears in the Email Accounts list.
- Employee receives login credentials.
- Employee is able to access the mailbox.

---

## Verification

Verify the following:

- The email account exists in the **Email Accounts** list.
- The email address is correct.
- No errors were displayed during creation.
- Credentials have been communicated to the employee or authorized requester.

---

## Estimated Duration

Approximately **2–5 minutes** per email account.

---

## Rollback Procedure

If the email account was created incorrectly:

1. Navigate to **Tools → Email Accounts**.
2. Locate the incorrect email account.
3. Delete the account if it should not exist.
4. Recreate the email account using the correct information.

---

## Security Considerations

- Verify that the request is approved before creating an email account.
- Use passwords that comply with the company's password policy.
- Never share credentials with unauthorized individuals.
- Encourage employees to change their password after the first login.
- Follow company policies for handling user credentials.

---

## Dependencies

- cPanel administrator access
- Active email hosting service
- Company email domain
- Approved email account request

---

## Common Issues

- Password does not meet the required strength.
- Email username already exists.
- Incorrect email domain selected.
- Unable to create the mailbox.

---

## Troubleshooting

### Password Strength Too Low

Create a stronger password until the password strength reaches the required minimum of **65**.

---

### Username Already Exists

Choose an alternative username or verify whether the account already exists.

---

### Unable to Create the Mailbox

- Verify administrator permissions.
- Confirm the email hosting service is active.
- Ensure the email domain is correct.

---

## Lessons Learned

Using a standardized naming convention for email usernames and enforcing a strong temporary password helps reduce account creation errors and improves consistency across the organization.

---

## Related Documents

-
-
-

---

## References

- cPanel Documentation
- Company Password Policy

---

## Notes

Email accounts should only be created after receiving an authorized request. Always verify the employee's information before creating the mailbox to prevent duplicate or incorrect accounts.

---

## Version History

| Version | Date | Changes |
|----------|------|---------|
| 1.0 | 2026-07-02 | Initial documentation |