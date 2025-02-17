# [Linux] Bash chage Usage equivalent: Manage user password expiration settings

## Overview
The `chage` command in Linux is used to change user password expiry information. It allows administrators to set and modify the parameters related to password aging, ensuring that users update their passwords regularly for security purposes.

## Usage
The basic syntax of the `chage` command is as follows:

```bash
chage [options] [username]
```

## Common Options
- `-l` : List the current password aging settings for the specified user.
- `-m` : Set the minimum number of days between password changes.
- `-M` : Set the maximum number of days a password is valid.
- `-I` : Set the number of days of inactivity allowed after a password expires.
- `-E` : Set the expiration date of the user account.
- `-d` : Set the last password change date.

## Common Examples

1. **List current password aging settings:**
   ```bash
   chage -l username
   ```

2. **Set the minimum password age to 7 days:**
   ```bash
   chage -m 7 username
   ```

3. **Set the maximum password age to 90 days:**
   ```bash
   chage -M 90 username
   ```

4. **Set the account to expire on a specific date (e.g., January 1, 2024):**
   ```bash
   chage -E 2024-01-01 username
   ```

5. **Set the last password change date to today:**
   ```bash
   chage -d 0 username
   ```

## Tips
- Always review the current settings with `chage -l username` before making changes.
- Consider setting a reminder for users when their password is nearing expiration.
- Use the `-I` option to enforce a grace period for users to change their passwords after expiration.
- Regularly audit user accounts to ensure compliance with your organization's password policies.