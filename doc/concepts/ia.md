---
sidebar_position: 4
sidebar_label: IA Automation 
---
# IA Automation
## Overview

Clicknium IA automation is based on Microsoft Active Accessibility(MSAA) to support the recording function, locators, and all operations on elements.  
As MSAA is now considered a legacy API, we treat IA as a supplement of UIA, on some Electron&CEF applications or legacy applications, IA can be better. Please manually choose IA technology if you want to use IA during recording.

## Locator attributes
 Learn [locator](./locator.md) concept first. For IA automation, the definition of the attributes is listed in the following:

| Name      | equals | contains |startWith |endWith |regex |
| ----------- | ----------- |----------- |----------- |----------- |----------- |
| Name |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| ClassName |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| HelpText |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| AccessKey |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| DefaultAction |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| Description |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| Role |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| IsDirectChild |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| Tag |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| Index |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|

## Locator samples

- github desktop 'open in visual studio code' button
```xml
<Application processName="GitHubDesktop" filePath="GitHubDesktop.exe" version="1.3" />
<IA className="Chrome_WidgetWin_1" isDirectChild="True" name="GitHub Desktop" role="window" />
<IA role="document" />
<IA defaultAction="click" isDirectChild="True" role="group" />
<IA defaultAction="click ancestor" isDirectChild="True" role="group" />
<IA defaultAction="click ancestor" isDirectChild="True" role="group" />
<IA defaultAction="click ancestor" index="2" isDirectChild="True" role="group" />
<IA defaultAction="click ancestor" index="2" isDirectChild="True" role="group" />
<IA defaultAction="click ancestor" isDirectChild="True" role="group" />
<IA className="Chrome_WidgetWin_1" defaultAction="press" name="Open in Visual Studio Code" />
```
- github desktop commit 'description` edit
```xml
<Application processName="GitHubDesktop" filePath="GitHubDesktop.exe" version="1.3" />
<IA className="Chrome_WidgetWin_1" isDirectChild="True" name="GitHub Desktop" role="window" />
<IA role="document" />
<IA defaultAction="click" isDirectChild="True" role="group" />
<IA defaultAction="click ancestor" isDirectChild="True" role="group" />
<IA defaultAction="click ancestor" isDirectChild="True" role="group" />
<IA defaultAction="click ancestor" index="2" isDirectChild="True" role="group" />
<IA defaultAction="click ancestor" index="2" isDirectChild="True" role="group" />
<IA defaultAction="click" isDirectChild="True" role="group" />
<IA defaultAction="click ancestor" isDirectChild="True" role="group" />
<IA defaultAction="click ancestor" isDirectChild="True" name="Create commit" role="group" />
<IA defaultAction="click" isDirectChild="True" role="group" />
<IA defaultAction="click ancestor" isDirectChild="True" role="group" />
<IA className="Chrome_WidgetWin_1" defaultAction="activate" name="Description" role="edit" />
```
- github desktop 'history' tabitem
```xml
<Application processName="GitHubDesktop" filePath="GitHubDesktop.exe" version="1.3" />
<IA className="Chrome_WidgetWin_1" isDirectChild="True" name="GitHub Desktop" role="window" />
<IA role="document" />
<IA defaultAction="click" isDirectChild="True" role="group" />
<IA defaultAction="click ancestor" isDirectChild="True" role="group" />
<IA defaultAction="click ancestor" isDirectChild="True" role="group" />
<IA defaultAction="click ancestor" index="2" isDirectChild="True" role="group" />
<IA defaultAction="click ancestor" index="2" isDirectChild="True" role="group" />
<IA defaultAction="click" isDirectChild="True" role="group" />
<IA defaultAction="click ancestor" isDirectChild="True" role="group" />
<IA defaultAction="click ancestor" isDirectChild="True" role="tab" />
<IA className="Chrome_WidgetWin_1" defaultAction="click" name="History" role="tabItem" />
```

## IA element properties
By [find_element](../references/python/globalfunctions/find_element.md) on one IA locator, you can get one IA element, and you can get properties of the element by [get_property](../references/python/uielement/get_property.md), Clicknium IA supports the following properties:


| Name      | Description |
| ----------- | ----------- |
| Name      |  the name of the user interface      |
| IsEnabled  | whether the element is enabled in the user interface|
| AccessKey   |  a string containing the access key character for the element|
| BoundingRectangle   | the coordinates of the rectangle that completely encloses the element|
| ProcessId   | the process identifier (ID) of the element|
| Description   |  description of the element|
| AcceleratorKey   | a string containing the accelerator key combinations for the element|
| HelpText   |the help text of the element|
| ControlType | the ControlType of the element.|
