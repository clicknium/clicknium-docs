# Clicknium VSCode Extension<!-- {docsify-ignore-all} -->

  - [Overview](#overview)
  - [Create Project](#create-project)
  - [Extension Installation](#extension-installation)
  - [Record UI Locators](#record-ui-locators)
  - [Edit and Validate Locator](#edit-and-validate-locator)
  - [Writing code](#writing-code)
  - [Run/Debug Project](#rundebug-project)
  - [For Existing Project](#for-existing-project)

## Overview
For python developer, if you use Visual Studio Code, Clickcorp provides clicknium extension that include all RPA features. 
With our extension for Visual Studio Code, you can create python automation project; capture ui elements in web browsers 
and variety desktop applications, easy to edit ui locator, validate or recapture; run/debug the automation project, and 
centeral locator store managerment on cloud. Besides these features, we also improve writing code experience, 
can do IntelliSense, error hint etc.

***Installation​***: Install through VS marketplace `Clicknium VS Code extension` or search clicknium in Visual Studio Code.  
***Remarks***: Clicknium extension is completely free, developer can use all features in Visual Studio Code.

## Create Project

## Extension Installation
[Automation Extensions](./doc/developtools/extensions/extensions.md)

## Record UI Locators
In Visual Studio Code, press `CTRL+F10` can invoke clicknium recorder and minimize current Visual Studio Code window,  
![clicknium recorder](../img/recorder_main.png)  
Capture Technology: indicate which automation technology current using to capture ui element, we support several automation tech:
- UIA： Leverage Microsoft UI Automation, it is used for most windows application such as win32, winform, WPF application and so on
- IA: based on MSAA (Microsoft Active Accessibility)
- Java: automation for java application, support JRE version about 1.6
- IE: automation for Internet Explorer, support version above 5.5 
- Chrome: automation for chrome, need install chrome extension first, support version above 60
- Edge: automation for edge, need install msedge extension first
- Firefox: automation for firefox, need install firefox extension first, support version above 56
- Sap: automation for sap wingui, need enable SAP GUI Scripting setting first 
  
Default is ***Auto Detect*** which means clicknium recorder automatically select rechnology:  
if mouse moves on windows applicaiton, it will use UIA technology to locate element;   
if mouse moves on java applicaiton, it will use Java technology to locate element;   
if mouse moves on Internet explorer, it will use IE technology to locate element;   
if mouse moves on Chrome, it will use Chrome technology to locate element;   
if mouse moves on Microsoft Edge, it will use Edge technology to locate element;   
if mouse moves on Firefox, it will use Firefox technology to locate element;   
if mouse moves on Sap windows GUI, it will use Sap technology to locate element

Advanced Option: default is None, you can choose `XPath`, it will take affect on web automation technology(IE, Chrome, Edge, Firefox), 
when capture element, will generate locator in XPath style.

Cursor Position(X,Y): indicate current mouse postion in screen

After invoke Clicknium Recorder, you can move mouse on the target applicaiton, it will highlight the element recognized, 
if you want to capture the element, press `Ctrl` and click, the element locator will be added.

![clicknium recorder](../img/record1.gif) 

## Edit and Validate Locator
After record the locators, you can open and edit the locator  
![clicknium vscode](../img/main.png) 

- locator store: file to store locator data. the locators of the same application are stored in one locator store defaultly, user can manage the locator store from Visual Studio Code or Clicnium Recorder.
- locator: Ui element locator, locator is string(XML fragment) that used to find the element, it includes application info, includes all necessary parent nodes of the element in the user interface, and using several attributes to identify each node include element itself.
- Screenshot: during record the element, we will store the screenshot together with the locator
- Attributes: user can select/deselect or edit the value of each attribute

More about locator, please refer to [clicknium locator](./doc/automation/locator.md)

After edit locator, you can press `Validate` button to verify, it will minimize Visual Studio Code and highlight the found element, if not found, will show detail error.
![validate error](../img/validate_err.png)

## Writing code
- Auto Code Complete
when you write code, need pass locator as parameter, for example, `cc.find_element(`, you can press `Ctrl`+F10, invoke clicknium recorder, and capture element, return back to Visual Studio Code, the captured element will be auto filled like `cc.find_element(locator.chrome.bing.search_sb_form_q)`

- IntelliSense
You can select one locator already in locator store, clicknium code extension can help you to show locator store list and locator list  
![intellisense](../img/intelliSense.png)

## Run/Debug Project

## For Existing Project