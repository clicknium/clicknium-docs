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