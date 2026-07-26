## Ticket #3 — Password Reset

**Date:** 2026-07-26
**Category:** Account Access
**Priority:** Medium
**Reported Issue:** User forgot their password and is unable to log into their workstation.

**Steps Taken:**
1. Verified user identity/account in Active Directory Users and Computers (ADUC)
2. Used the "Reset Password" option on the user's account
3. Set a new temporary password and enabled "User must change password at next logon"
4. Verified the account was not also locked out
5. Logged into CLIENT01 with the temporary password to confirm the forced password change prompt appeared and completed successfully

**Resolution:** Password reset, user regained access, and was required to set a new password on next logon per policy.
**Time to Resolve:** ~5 minutes
