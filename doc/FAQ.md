---
sidebar_position: 6
sidebar_label: FAQ
---

# Frequently Asked Questions

## Login Failure
When you try to login and got error: `Uncaught SecurityError: Failed to read the 'localStorage' property from 'Window': Access is denied for this document.` This exception is thrown when the "Block third-party cookies and site data" checkbox is set in Content Settings.  
To find the setting, open Chrome settings, click `Privacy and security` in navigation bar, click `Cookies and other site data`, and view the third item under General settings.
![pic](./img/block3rdcookies.PNG)  
If this setting is checked, third-party scripts cookies are disallowed and access to localStorage may result in thrown SecurityError exceptions.

## Can not automate browser running instances with different user profiles
If you encountered the subsequent issue when recording:

![multiple user profile error](img/faq_multiple_profile_error.png)

This is due to the possibility that you have started several Chrome browser windows using several user profiles. Every Chrome browser window's user profile is visible in the top-right corner.

![multiple user profile](img/faq_mulitple_profile2.png)

You can fix this issue by first stopping Clicknium Recorder, closing all open browser tabs, opening the browser solely in a single user profile, and then starting a new recording.

## This element is not similar to previous elements, please capture again
If you encountered the subsequent issue when recording similar elements, 

![similar element error](img/faq_similar_elelemt_error.png)

The new recorded locator being different from the old one should be the primary factor. For example:
- They are elements of various types, for example: one with tag "a" and the other with tag "div".
- They are under different iframes.

For more information, please refer to [Capture similar elements](tutorial/recorder/capture_similar_elements.md)

## Browser extension for Chrome is not turned on, do you want to turn on it now?
If you encountered the subsequent issue when recording element on one browser page,

![install extension](img/faq_install_extension_error.png)

The main reason should be Clicknium browser extension is not enabled, you can click 'Yes', browser extension page will be opened, you can enable it: 

![install extension](img/chrome_extension_enable_page.png)

And refresh the web page or re-open the browser window, and record once more.
