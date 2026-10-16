# KB-002: Wi-Fi not connecting

**Category:** Network  
**Applies to:** Windows 10 and Windows 11 (menu names can differ slightly)  
**Support level:** L1 (first-line)

## Symptoms

- Wi-Fi network is not listed
- Wi-Fi is listed but will not connect
- Message such as 'Can't connect to this network'

## Possible causes

- Wi-Fi turned off or Airplane mode on
- Wrong or changed password
- Corrupted network profile or outdated driver
- Router fault

## Steps

1. Check that Airplane mode is off and Wi-Fi is turned on (Settings > Network & internet > Wi-Fi).
2. Check other devices. If they also cannot connect, the router or internet service is the problem. Restart the router and wait 2 minutes.
3. Forget the network and reconnect: Settings > Network & internet > Wi-Fi > Manage known networks > select the network > **Forget**. Reconnect and enter the password again.
4. Renew the connection. Open Command Prompt as administrator and run:
   ```
   ipconfig /release
   ipconfig /renew
   ipconfig /flushdns
   ```
5. Run the troubleshooter: Settings > System > Troubleshoot > Other troubleshooters > Network and Internet (Windows 10: Settings > Update & Security > Troubleshoot).
6. Update or reinstall the Wi-Fi driver: Device Manager > Network adapters > right-click the Wi-Fi adapter > Update driver. If that fails, choose **Uninstall device**, then restart. Windows reinstalls it.
7. As a last step, reset the network settings: Settings > Network & internet > Advanced network settings > Network reset. This removes all saved networks.

## Expected result

The PC connects to the Wi-Fi network, shows signal bars, and a web page loads.

## Escalate to L2 if

No Wi-Fi adapter appears in Device Manager, or the problem affects many users on the same network. Escalate to L2 or the network team.

## Ticket worklog example

> Issue: wi-fi not connecting. Steps taken: see KB-002. Result: ______. Time spent: ____ min. Escalated: Yes / No.
