# KB-001: Windows PC running slow

**Category:** Performance  
**Applies to:** Windows 10 and Windows 11 (menu names can differ slightly)  
**Support level:** L1 (first-line)

## Symptoms

- Slow startup and slow app launch
- Mouse or typing lags
- Fan runs loudly or the PC feels hot

## Possible causes

- Too many startup programs
- Low free disk space or low RAM
- Pending Windows updates
- Malware or background processes

## Steps

1. Restart the PC. A restart clears temporary memory use.
2. Press `Ctrl + Shift + Esc` to open Task Manager. On the **Processes** tab, sort by CPU, Memory and Disk to find the heaviest process. Select it and click **End task** if it is not a system process.
3. Open the **Startup apps** tab in Task Manager and **Disable** programs you do not need at startup.
4. Check free space: Settings > System > Storage. Keep at least 15% of the drive free (see KB-010).
5. Install pending updates: Settings > Windows Update > Check for updates.
6. Run a scan: Windows Security > Virus & threat protection > Scan options > Full scan.
7. Repair system files. Open Command Prompt as administrator and run:
   ```
   sfc /scannow
   ```
8. Set the power plan to Balanced or High performance: Control Panel > Power Options.

## Expected result

Startup time and app launch time improve, and CPU, memory and disk usage in Task Manager settle at normal levels when the PC is idle.

## Escalate to L2 if

Disk usage stays at 100% (KB-008), the drive reports errors, or the PC has less than 4 GB of RAM. Escalate to L2 for a hardware upgrade or reimage.

## Ticket worklog example

> Issue: windows pc running slow. Steps taken: see KB-001. Result: ______. Time spent: ____ min. Escalated: Yes / No.
