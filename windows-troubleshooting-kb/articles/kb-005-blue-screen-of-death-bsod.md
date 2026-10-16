# KB-005: Blue Screen of Death (BSOD)

**Category:** System  
**Applies to:** Windows 10 and Windows 11 (menu names can differ slightly)  
**Support level:** L1 (first-line)

## Symptoms

- Blue screen with a sad face and a stop code
- PC restarts on its own
- Stop codes such as `CRITICAL_PROCESS_DIED` or `IRQL_NOT_LESS_OR_EQUAL`

## Possible causes

- Faulty or incompatible driver
- Failing RAM or disk
- Corrupted system files
- Recent update or new hardware

## Steps

1. Write down the **stop code** shown on the blue screen (or take a photo).
2. Restart the PC. If it does not happen again, monitor it. If it repeats, continue.
3. Remove recently connected hardware (USB devices, new drives).
4. If the PC will not start normally, start Safe Mode: interrupt startup three times to open the recovery screen, then Troubleshoot > Advanced options > Startup Settings > Restart > **4 / F4 Safe Mode**.
5. Uninstall the latest update or driver: Settings > Windows Update > Update history > Uninstall updates. For drivers, use Device Manager > Properties > Driver > **Roll Back Driver**.
6. Repair system files. In Command Prompt as administrator:
   ```
   sfc /scannow
   DISM /Online /Cleanup-Image /RestoreHealth
   ```
7. Check memory: press `Win + R`, type `mdsched.exe`, choose **Restart now and check for problems**.
8. Check the disk: run `chkdsk C: /f` as administrator and restart when asked.
9. Review the crash details in Reliability Monitor (search for it in the Start menu) to see which app or driver was involved.

## Expected result

The PC runs without blue screens, and Reliability Monitor shows no new critical events.

## Escalate to L2 if

Blue screens continue after steps 5 to 8 or memory or disk tests fail. Escalate to L2 with the stop code, the time of each crash and the steps tried.

## Ticket worklog example

> Issue: blue screen of death (bsod). Steps taken: see KB-005. Result: ______. Time spent: ____ min. Escalated: Yes / No.
