# Automation Concepts

## Overview
In this section, we will illustrate the technology information about Clicknium automation, including how to leverage Clicknium automation technology to make RPA/automation project robust and easily edited, writed and maintained.  
Clicknium automation integrate mulitple automation technologies in backgroup, Clicknium Recorder default use `Auto Detect` mode, it means Clicknium will automatically detect the application type, and choose appropriate background technology.  
Clicknium defined unified [locator](./locator.md) schema to identify UI element, a locator stores the attributes of a UI element and its parents, for example, button on Windows application, input on web page or combobox on Java application can be stored as one locator.

The following technologies are freqeuntly used:
- [Clicknium UIA](./uia.md): automation on most Windows/desktop application，based on Microsoft UI Automation.
- [Clicknium Chrome/Edge/IE/Firefox](./web.md)：automation on many popular web browsers.
- [Clicknium Java](./java.md): automation on Java application, support Java 1.6 or above.
- [Clicknium SAP](./sap.md): automation on SAP WinGUI, it requires the SAP WinGUI API scripting enabled.
- [Clicknium IA](./ia.md): automation on Windows/desktop application, it can be supplement for UIA, on some electron&CEF applications or some legacy application, IA can be better.
- [Clicknium Image Automation](./image.md): image automation can be used combied with above technologies.


## Articles
- [Locator](./locator.md)
- [UIA automation](./uia.md)
- [Web automation](./web.md)
- [Java automation](./java.md)
- [SAP Automation](./sap.md)
- [IA Automation](./ia.md)
- [Image Automation](./image.md)

