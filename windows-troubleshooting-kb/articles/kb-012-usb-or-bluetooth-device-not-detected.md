# KB-012: USB or Bluetooth device not detected

**Category:** Peripherals  
**Applies to:** Windows 10 and Windows 11 (menu names can differ slightly)  
**Support level:** L1 (first-line)

## Symptoms

- New device is not recognized
- 'USB device not recognized' message
- Bluetooth device will not pair

## Possible causes

- Faulty port, cable or device
- Missing or damaged driver
- Bluetooth turned off or device not in pairing mode

## Steps

1. Try a different USB port and cable. Test the device on another PC to separate a device fault from a PC fault.
2. Restart the PC.
3. Open Device Manager and look for a device with a yellow warning mark. Right-click it > **Uninstall device**, then **Action > Scan for hardware changes**.
4. Install driver updates: Settings > Windows Update > Advanced options > Optional updates.
5. **Bluetooth:** turn Bluetooth on in Settings > Bluetooth & devices, put the device in pairing mode, remove the old pairing, and pair again.
6. Run the troubleshooter: Settings > System > Troubleshoot > Other troubleshooters > Bluetooth.

## Expected result

The device appears in Device Manager or Bluetooth settings and works normally.

## Escalate to L2 if

The device fails on other PCs too, or a port does not work with any device. Escalate to L2 for hardware replacement.

## Ticket worklog example

> Issue: usb or bluetooth device not detected. Steps taken: see KB-012. Result: ______. Time spent: ____ min. Escalated: Yes / No.
