SAP WinGUI Automation
SAP WinGUI is commonly used to access SAP functionality in SAP applications.
Clicknium automation stack supports automation for SAP WinGUI， need enable SAP WinGUI API scripting.

The following version of SAP WinGUI are supported.
- 7.4
- 7.5
- 7.6
  
the following functions specified for SAP are supported:
- [login](/doc/api/python/sap/login.md)
- [select_item](/doc/api/python/sap/select_item.md)
- [call_transaction](/doc/api/python/sap/call_transaction.md)
- [get_statusbar](/doc/api/python/sap/get_statusbar.md)  

Besides the about functions, the other general functions are also supported for SAP WinGUI element, such as click, set_text, get_text etc.

## Enabling SAP WinGUI API scripting
### Server Side Configuration
1. Launch `saplogon`, log in to SAP server
2. Run transaction code `RZ11`  
![sap](img/sap1.png)  
3. Input the parameter name `sapgui/user_scripting`, click `Display` button
![sap](img/sap2.png)  
4. In the `Display Profile Parameter Attributes` dialog, click `Change Value` button, Set ***Current Value*** to `TRUE`, then save the changes.
![sap](img/sap3.png)  
5. Repeat step 4, set the following parameters's value to `FALSE`
- sapgui/user_scripting_disable_recording
- sapgui/user_scripting_force_notification
- sapgui/user_scripting_per_user
- sapgui/user_scripting_set_readonly
  
Note: All changes to parameters in transaction `RZ11` are applied with immediate effect and are lost when the system restarts. For changes to be permanent, please contact your SAP System Administrator.

### Client Side Configuration
1. Select  `Options` menu
2. Go to Accessibility & Scripting and click on Scripting.
3. Check the Enable scripting option.  
![sap](img/sap4.png)  
4. Clear the checkboxes for the following options:
- Notify when a script attaches to SAP GUI
- Notify when a script opens a connection
5. Save the changes by clicking OK. The SAP WinGUI scripting is now enabled.

### Enabling Modal Dialog Boxes
1. From the SAP Easy Access window, click Settings under the Help menu. The Personal Settings for User window is displayed.  
![sap](img/sap5.png)  
2. Access the F1 Help tab and select the in Modal Dialog Box option from the Display section.  
![sap](img/sap6.png)  
3. If need use date selection, access the F4 Help tab, and select Control (amodal) option from the Display section.  
![sap](img/sap7.png)  
4. Click the Apply button to save changes and close the Personal Settings for User window.