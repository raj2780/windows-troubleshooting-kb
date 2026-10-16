# KB-009: Application not responding or crashing

**Category:** Applications  
**Applies to:** Windows 10 and Windows 11 (menu names can differ slightly)  
**Support level:** L1 (first-line)

## Symptoms

- Window shows '(Not Responding)'
- Program closes without a message
- Program freezes on opening

## Possible causes

- Corrupted app files or settings
- Outdated app or Windows
- Conflict with another program
- Low memory

## Steps

1. Wait one minute. A busy program may recover.
2. Open Task Manager, select the app and click **End task**. Reopen the app.
3. Restart the PC to free memory.
4. Update the app and Windows.
5. Repair or reset the app: Settings > Apps > Installed apps > select the app > **Advanced options** > **Repair**, then **Reset** if needed. Reset removes app data.
6. If the app is not a Store app, use Control Panel > Programs > Uninstall a program > select the app > **Repair**, or uninstall and reinstall it.
7. Check the cause in Reliability Monitor or Event Viewer > Windows Logs > Application, and note the error.

## Expected result

The app opens and runs normally without freezing.

## Escalate to L2 if

The same crash returns after a reinstall. Escalate to L2 or the application owner with the app version and error details.

## Ticket worklog example

> Issue: application not responding or crashing. Steps taken: see KB-009. Result: ______. Time spent: ____ min. Escalated: Yes / No.
