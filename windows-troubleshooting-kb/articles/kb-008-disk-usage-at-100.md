# KB-008: Disk usage at 100%

**Category:** Performance  
**Applies to:** Windows 10 and Windows 11 (menu names can differ slightly)  
**Support level:** L1 (first-line)

## Symptoms

- Task Manager shows Disk at 100%
- PC freezes for several seconds at a time
- Programs open very slowly

## Possible causes

- A background process or update using the disk
- Failing hard drive
- Malware
- Low free space

## Steps

1. Open Task Manager (`Ctrl + Shift + Esc`) and sort the **Disk** column to identify the process.
2. Wait for any running Windows Update or antivirus scan to finish, then restart.
3. Close or uninstall the heavy application if it is not needed.
4. Run a full scan in Windows Security to rule out malware.
5. Check the disk for errors: `chkdsk C: /f` in Command Prompt as administrator, then restart.
6. Check disk health in PowerShell:
   ```
   Get-PhysicalDisk | Select FriendlyName, HealthStatus
   ```
7. Free up space (see KB-010).

## Expected result

Disk usage falls to a normal level when the PC is idle and the system responds smoothly.

## Escalate to L2 if

HealthStatus is not Healthy, `chkdsk` reports bad sectors, or the PC has a hard drive (HDD) that stays at 100%. Escalate to L2 to replace the drive, ideally with an SSD, after backing up data.

## Ticket worklog example

> Issue: disk usage at 100%. Steps taken: see KB-008. Result: ______. Time spent: ____ min. Escalated: Yes / No.
