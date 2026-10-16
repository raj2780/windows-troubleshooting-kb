# KB-004: Printer offline or not printing

**Category:** Peripherals  
**Applies to:** Windows 10 and Windows 11 (menu names can differ slightly)  
**Support level:** L1 (first-line)

## Symptoms

- Printer shows 'Offline'
- Jobs stay stuck in the queue
- Nothing prints and no error appears

## Possible causes

- Printer off, cable or network problem
- Stuck print job
- Print Spooler service problem
- Wrong default printer or outdated driver

## Steps

1. Check the printer is on, has paper, and shows no error light. Check the USB cable, or confirm a network printer is on the same network.
2. Set the correct default printer: Settings > Bluetooth & devices > Printers & scanners > select the printer > **Set as default**.
3. Open the print queue (select the printer > Open print queue). Cancel all stuck documents.
4. If jobs will not clear, restart the Print Spooler. In Command Prompt as administrator:
   ```
   net stop spooler
   del /Q /F /S "%systemroot%\System32\spool\PRINTERS\*.*"
   net start spooler
   ```
5. In the print queue menu, make sure **Use Printer Offline** is not ticked.
6. Remove the printer and add it again: Printers & scanners > Remove, then **Add device**. Install the latest driver from the manufacturer's website if needed.
7. Print a test page: printer properties > **Print Test Page**.

## Expected result

The test page prints and the print queue empties.

## Escalate to L2 if

The printer fails on every PC (hardware fault), or a shared printer is missing on the print server. Escalate to L2 or the printer vendor.

## Ticket worklog example

> Issue: printer offline or not printing. Steps taken: see KB-004. Result: ______. Time spent: ____ min. Escalated: Yes / No.
