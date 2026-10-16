# KB-006: Forgotten Windows password

**Category:** Accounts  
**Applies to:** Windows 10 and Windows 11 (menu names can differ slightly)  
**Support level:** L1 (first-line)

## Symptoms

- User cannot sign in to Windows
- 'The password is incorrect' message
- Caps Lock or wrong keyboard language suspected

## Possible causes

- Forgotten or recently changed password
- Caps Lock or wrong keyboard layout
- Account is locked or expired

## Steps

1. Verify the user's identity first, following company policy, before any reset.
2. Check Caps Lock, Num Lock and the keyboard language shown at the sign-in screen. Click the eye icon to view what is typed.
3. **Microsoft account:** on another device open `account.live.com/password/reset`, verify identity and set a new password. At the sign-in screen, use **I forgot my password**.
4. **Local account with security questions:** click **Reset password** under the password box and answer the questions.
5. **Local account, another administrator available:** sign in as the administrator and open Computer Management > Local Users and Groups > Users (Windows Pro), right-click the user > **Set Password**. On Windows Home, open Command Prompt as administrator and run `net user USERNAME NEWPASSWORD`.
6. **Work or school (domain) account:** use the company self-service password reset, or raise a request with the IT service desk.
7. Ask the user to change the temporary password at the next sign-in and note the reset in the ticket worklog.

## Expected result

The user signs in with the new password.

## Escalate to L2 if

No administrator account exists, the drive is encrypted with BitLocker and the recovery key is missing, or identity cannot be verified. Escalate to L2. Do not bypass the sign-in screen.

## Ticket worklog example

> Issue: forgotten windows password. Steps taken: see KB-006. Result: ______. Time spent: ____ min. Escalated: Yes / No.
