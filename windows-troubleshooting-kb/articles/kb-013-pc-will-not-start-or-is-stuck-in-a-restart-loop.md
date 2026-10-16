# KB-013: PC will not start or is stuck in a restart loop

**Category:** System  
**Applies to:** Windows 10 and Windows 11 (menu names can differ slightly)  
**Support level:** L1 (first-line)

## Symptoms

- Black screen or logo that never reaches sign-in
- 'Preparing Automatic Repair' loop
- Error 'Your PC did not start correctly'

## Possible causes

- Corrupted startup files
- Failed update or driver
- Disk error or a loose drive

## Steps

1. Unplug external USB devices and restart.
2. If the recovery screen appears, choose Troubleshoot > Advanced options > **Startup Repair**.
3. If it fails, open Advanced options > **Startup Settings** > Restart > **Safe Mode**. Uninstall the latest update or driver there.
4. Try **System Restore** from Advanced options to return to an earlier restore point.
5. From Advanced options > **Command Prompt**, run:
   ```
   bootrec /fixmbr
   bootrec /fixboot
   bootrec /rebuildbcd
   ```
6. If no recovery screen appears, force-shut down the PC three times in a row during startup to open Windows Recovery.

## Expected result

Windows reaches the sign-in screen and starts normally.

## Escalate to L2 if

The drive is missing in BIOS or every repair option fails. Escalate to L2 and do not reset or reinstall Windows without confirming that the user's data is backed up.

## Ticket worklog example

> Issue: pc will not start or is stuck in a restart loop. Steps taken: see KB-013. Result: ______. Time spent: ____ min. Escalated: Yes / No.
