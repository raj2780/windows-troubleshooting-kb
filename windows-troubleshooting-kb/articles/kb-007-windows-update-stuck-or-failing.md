# KB-007: Windows Update stuck or failing

**Category:** System  
**Applies to:** Windows 10 and Windows 11 (menu names can differ slightly)  
**Support level:** L1 (first-line)

## Symptoms

- Update stays at a percentage for hours
- Error codes such as `0x80070002` or `0x800f0922`
- Updates fail and roll back at restart

## Possible causes

- Low disk space
- Corrupted update cache
- Damaged system files
- Connection interrupted during download

## Steps

1. Confirm at least 10 GB of free space and a stable internet connection.
2. Restart the PC and run Windows Update again.
3. Run the troubleshooter: Settings > System > Troubleshoot > Other troubleshooters > Windows Update.
4. Clear the update cache. In Command Prompt as administrator:
   ```
   net stop wuauserv
   net stop bits
   ren C:\Windows\SoftwareDistribution SoftwareDistribution.old
   net start wuauserv
   net start bits
   ```
5. Repair system files:
   ```
   sfc /scannow
   DISM /Online /Cleanup-Image /RestoreHealth
   ```
6. Run Windows Update again and restart when prompted.

## Expected result

Windows Update shows 'You're up to date' and the failing update appears in Update history as successful.

## Escalate to L2 if

The same error code returns after all steps. Escalate to L2 with the error code and the KB number of the failing update.

## Ticket worklog example

> Issue: windows update stuck or failing. Steps taken: see KB-007. Result: ______. Time spent: ____ min. Escalated: Yes / No.
