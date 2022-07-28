---
sidebar_position: 2
sidebar_label: UIA Automation 
---
# UIA Automation 
## Overview

Clicknium UIA automation is based on Microsoft UI Automation, supply recording function, generate locator and all operations on one element.  
During recording, if you choose the windows application, such as notepad, calculator, some ERP client applications, clicknium will use UIA automation to record the element.

## Locator attributes
You can get [locator](locator.md) concept first, for UIA automation, the attributes defined are as the following:

| Name      | equals | contains |startWith |endWith |
| ----------- | ----------- |----------- |----------- |----------- |
| Name |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| AutomationId |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| ClassName |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| HelpText |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| Role |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| IsDirectChild |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| AccessKey |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| IsPassword |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| AcceleratorKey |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| ItemType |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| ItemStatus |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| Orientation |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| Index |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|

## Locator samples

- notepad 'format' menuitem
```xml
<Application processName="notepad" filePath="notepad.exe" version="1.3" />
<Uia className="Notepad" isDirectChild="True" name="Untitled - Notepad" role="window" />
<Uia accessKey="Alt" automationId="MenuBar" isDirectChild="True" role="menuBar" />
<Uia accessKey="Alt+o" isDirectChild="True" name="Format" role="menuItem" />
```
- notepad 'document' area
```xml
<Application processName="notepad" filePath="notepad.exe" version="1.3" />
<Uia className="Notepad" isDirectChild="True" name="Untitled - Notepad" role="window" />
<Uia automationId="15" className="Edit" isDirectChild="True" role="document" />
```
- calculator button '5'
```xml
<Application processName="ApplicationFrameHost" filePath="Calculator.exe" version="1.3" />
<Uia className="ApplicationFrameWindow" isDirectChild="True" name="计算器" role="window" />
<Uia className="Windows.UI.Core.CoreWindow" isDirectChild="True" name="计算器" role="window" />
<Uia className="LandmarkTarget" isDirectChild="True" role="group" />
<Uia automationId="NumberPad" className="NamedContainerAutomationPeer" isDirectChild="True" role="group" />
<Uia automationId="num5Button" className="Button" isDirectChild="True" />
```

## UIA element properties
By [find_element](../references/python/globalfunctions/find_element.md) on one UIA locator, you can get one UIA element, you can get properties of the element.   by [get_property](../references/python/uielement/get_property.md), Clicknium UIA support the following properties:

| Name      | Description |
| ----------- | ----------- |
| Name      |  the name of the user interface      |
| IsEnabled  | whether the element is enabled in the user interface|
| AccessKey   |  a string containing the access key character for the element|
| AutomationId |a string containing the UI Automation identifier (ID) for the element|
| BoundingRectangle   | the coordinates of the rectangle that completely encloses the element|
| ProcessId   | the process identifier (ID) of the element|
| ItemType   | the description of the item type |
| IsPassword   |  whether the UI Automation element contains protected content|
| IsOffscreen   |  whether the UI Automation element is visible on the screen(true when the control is not visible; otherwise false)|
| AcceleratorKey   | a string containing the accelerator key combinations for the element|
| HelpText   |the help text of the element|
| IsKeyboardFocusable   |whether the UI Automation element can accept keyboard focus|
| IsContentElement   | whether the element is a content element|
| IsControlElement   | whether the element is viewed as a control|
| HasKeyboardFocus   | whether the element has keyboard focus|
| FrameworkId   | the name of the UI framework, such as "Win32", "WinForm", or "DirectUI". The default value is an empty string.|
| ControlType | the ControlType of the element.|
