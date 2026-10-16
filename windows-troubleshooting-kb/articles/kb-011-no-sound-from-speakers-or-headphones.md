# KB-011: No sound from speakers or headphones

**Category:** Peripherals  
**Applies to:** Windows 10 and Windows 11 (menu names can differ slightly)  
**Support level:** L1 (first-line)

## Symptoms

- No audio from speakers or headphones
- Red X on the speaker icon
- Sound works in some apps only

## Possible causes

- Muted or low volume
- Wrong output device selected
- Audio service stopped or driver issue

## Steps

1. Check the volume and mute in the taskbar and on the speakers or headphones. Test with different headphones or speakers.
2. Select the right output: click the speaker icon in the taskbar and choose the correct device.
3. Run the audio troubleshooter: Settings > System > Troubleshoot > Other troubleshooters > Audio.
4. Restart the audio service: press `Win + R`, type `services.msc`, right-click **Windows Audio** > **Restart**.
5. Update or reinstall the audio driver: Device Manager > Sound, video and game controllers > right-click the device > **Update driver**, or **Uninstall device** and restart.
6. Check the app's own volume in the volume mixer.

## Expected result

Sound plays from the selected device at a normal level.

## Escalate to L2 if

No audio device appears in Device Manager, or sound fails on a known good device. Escalate to L2 for a hardware check.

## Ticket worklog example

> Issue: no sound from speakers or headphones. Steps taken: see KB-011. Result: ______. Time spent: ____ min. Escalated: Yes / No.
