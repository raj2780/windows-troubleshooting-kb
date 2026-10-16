# KB-010: Low disk space

**Category:** Storage  
**Applies to:** Windows 10 and Windows 11 (menu names can differ slightly)  
**Support level:** L1 (first-line)

## Symptoms

- 'Low disk space' warning
- Updates fail to install
- Cannot save files

## Possible causes

- Large downloads or temporary files
- Old Windows update files
- Unused programs
- Full Recycle Bin

## Steps

1. Open Settings > System > Storage and check what uses the most space.
2. Turn on **Storage Sense** to clear temporary files automatically.
3. Open **Temporary files** in that screen and remove Downloads, Recycle Bin and temporary files you do not need. Check each box before deleting.
4. Run Disk Cleanup: press `Win + R`, type `cleanmgr`, choose the drive and click **Clean up system files**.
5. Uninstall unused programs: Settings > Apps > Installed apps.
6. Move large personal files (videos, photos) to an external drive or cloud storage.

## Expected result

The drive has at least 15% free space and updates install without a space error.

## Escalate to L2 if

The drive is still nearly full after cleanup and the user needs the data. Escalate to L2 for a larger drive or cloud storage.

## Ticket worklog example

> Issue: low disk space. Steps taken: see KB-010. Result: ______. Time spent: ____ min. Escalated: Yes / No.
