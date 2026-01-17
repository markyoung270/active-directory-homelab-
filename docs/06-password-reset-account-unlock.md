The purpose of this scenario was to simulate a common help desk workflow in which a user is locked out of their domain account and requires a password reset and account unlock.
This task provided hands-on experience with routine Active Directory user management operations.

I began by intentionally attempting to lock a domain user account through repeated failed login attempts.
After observing that the account did not lock out by default, I identified that the domain account lockout policy was not configured.
I then updated the lockout policy on the domain controller to lock accounts after three invalid login attempts and successfully triggered an account lockout.

After confirming the lockout, I opened Active Directory Users and Computers to review the user’s account properties and verified that the account was marked as locked.
I then reset the user’s password, unlocked the account, and configured the account to require a password change at the next login.

Finally, I logged into the client workstation as the affected user, completed the required password change, and verified successful authentication.
This confirmed that the account access issue was resolved and that the user was able to log in normally following the reset and unlock process.
