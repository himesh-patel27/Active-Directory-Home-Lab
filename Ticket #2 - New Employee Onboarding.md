## Ticket #2 — New Employee Onboarding

**Date:** 2026-07-26
**Category:** Account Provisioning
**Priority:** Medium
**Reported Issue:** New employee starting on the IT team needs a domain account, workstation access, and appropriate group membership set up before their start date.

**Steps Taken:**
1. Created a new user object in Active Directory Users and Computers (ADUC) under the IT OU
2. Set a temporary password and enabled "User must change password at next logon"
3. Added the user to the appropriate security group (IT Staff)
4. Verified account properties (name, logon name, OU placement, group membership)
5. Logged into CLIENT01 with the new account to confirm successful first login and forced password change prompt

**Resolution:** New user account created, added to IT Staff security group, and verified working login on domain-joined workstation. User was prompted to set a new password on first logon as expected.
**Time to Resolve:** ~10 minutes
