# KB-003: Connected to Wi-Fi but no internet

**Category:** Network  
**Applies to:** Windows 10 and Windows 11 (menu names can differ slightly)  
**Support level:** L1 (first-line)

## Symptoms

- Wi-Fi icon shows 'No internet' or a yellow warning
- Some sites load while others do not
- Browser shows DNS errors

## Possible causes

- DNS problem
- Wrong IP configuration
- Proxy or VPN setting
- Internet service outage

## Steps

1. Test another device on the same network to see if the internet is down for everyone.
2. Open Command Prompt and test the connection:
   ```
   ping 8.8.8.8
   ping google.com
   ```
   If the first works and the second fails, the problem is DNS.
3. Flush DNS and renew the address:
   ```
   ipconfig /flushdns
   ipconfig /release
   ipconfig /renew
   ```
4. Change DNS: Settings > Network & internet > Wi-Fi > Hardware properties > DNS server assignment > Edit > Manual. Enter `8.8.8.8` and `8.8.4.4`.
5. Turn off any proxy or VPN: Settings > Network & internet > Proxy > turn off **Use a proxy server**.
6. Reset the network stack. In Command Prompt as administrator:
   ```
   netsh winsock reset
   netsh int ip reset
   ```
   Then restart the PC.

## Expected result

`ping google.com` replies, and web pages open normally.

## Escalate to L2 if

`ping 8.8.8.8` also fails on every device (internet outage), or the issue returns after a restart. Escalate to the network team or internet provider.

## Ticket worklog example

> Issue: connected to wi-fi but no internet. Steps taken: see KB-003. Result: ______. Time spent: ____ min. Escalated: Yes / No.
