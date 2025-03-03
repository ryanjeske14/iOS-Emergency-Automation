# Emergency Alert Automation for iOS

## Overview
This guide explains how to set up automation on an iPhone to send emergency text messages and, optionally, call a designated contact. Additionally, it includes a separate automation to ensure that incoming emergency messages from designated contacts are noticed by disabling "Do Not Disturb" and "Silent" modes and setting the ringtone volume to maximum.

## Features
1. **Send an Emergency Alert:**
   - Uses the Shortcuts app to:
       - Send an emergency text message containing "EMERGENCY" to a designated contact.
       - Send the address of your current location to a designated contact.
       - Prompt the user to call a designated contact.

2. **Receive an Emergency Alert:**
   - Uses the Automation feature of the Shortcuts app to:
       - Detect incoming messages containing "EMERGENCY".
       - Disable "Do Not Disturb" mode.
       - Disable "Silent" mode.
       - Set the ringtone volume to 100%.


## Prerequisites
- iPhone running iOS with the Shortcuts app installed.

## Setup Instructions

### 1. Create the Emergency Shortcut (repeat these steps for each emergency contact that you want to be able to contact)
1. Open this [link](https://www.icloud.com/shortcuts/71512416fbcf402ca111de6a7c0d6b91) on your iPhone.
2. Tap **+ Add Shortcut**.
3. This should take you to Shortcuts app. Find the newly-added shortcut named "Emergency - \<NAME>" and tap the three dots to edit the shortcut.
4. On the edit screen, tap the dropdown next to the shortcut name and choose **Rename**. Replace `<NAME>` with the name of your emergency contact (e.g., `Emergency - Ryan`). 
5. On the step **Send "EMERGENCY" to Recipients**, tap **Recipients** and select your emergency contact from your Contacts list.
6. On the step **Send "Current Location" to Recipients**, tap **Recipients** and select your emergency contact from your Contacts list.
7. On the step **Choose from menu with...**, tap the step and replace `<NAME>` with the name of your emergency contact (e.g., `Do you want to call Ryan?`).
8. On the **Call Contact** step under the **Yes** option, tap **Contact** and select your emergency contact from your Contacts list.
9. OPTIONAL - tap the dropdown next to the shortcut name and choose **Add to Home Screen**. Tap the name under the icon to edit it and set it to the name of your emergency contact (e.g., `Ryan`). Now, you can run the shortcut by clicking the associated shortcut icon from your home screen (i.e., apps view). 
10. OPTIONAL - if you set up multiple emergency contact shortcuts and add them to your homescreen, combine them into one folder and name the folder `Emergency`.  
11. Tap **Done** on the top right corner of the screen.

### 2. Create the Emergency Automation
1. Open the **Shortcuts** app and go to the **Automation** tab at the bottom of the screen.
2. Tap **+** to create a new automation.
4. Scroll down and choose **Message** as the trigger.
5. In the **Sender** field, select one or more contacts from whom you want to be able to receive emergency messages and calls (e.g, Bob, Alice, Mom, Dad).
6. In the **Message Contains** field, enter `EMERGENCY`.
7. Select the option for **Run Immediately**.
8. Tap **Next**.
9. Tap **New Blank Automation**
10. Search for and select **Set Focus** and ensure the it is set to **Turn Do Not Disturb Off**.
11. Tap **Seach Actions** again to add another action.
12. Search for and select **Set Silent Mode** and ensure that it is set to **Turn Silent Mode Off**.
13. Tap **Seach Actions** again to add another action.
14. Search for and select **Set Volume**. Tap the volume type (e.g., **Media**) and select **Ringtone**. Then, set the volume level to 100%.
15. Tap **Done** to save the automation.

## Testing the Setup
- You can test the setup by adding yourself as a contact in your Contacts app. Then, go through the steps under **1. Create the Emergency Shortcut** using yourself as the contact. Then, on step 5 under **2. Create the Emergency Automation**, add yourself to the Sender list.
- Enable "Silent" mode, enable "Do Not Disturb" mode, and set your ringtone volume to any value less than 100%.
- Manually run the shortcut (the one you created for yourself for testing).
- Expected Results:
    - Message `EMERGENCY` sent to yourself.
    - Message containing the address of your location sent to yourself.
    - A promt asking if you want to call yourself. You can test both options if you'd like to confirm the functionality.
    - "Do Not Disturb" mode disabled.
    - "Silent" mode disabled.
    - Ringtone volume set to 100%.

## Notes
- Ensure the designated contact is saved in your contacts.
- Use this setup responsibly, as it could trigger false alarms.

## Disclaimer
Use this setup at your own discretion. It is designed to assist in emergencies but does not guarantee functionality or immediate assistance.
