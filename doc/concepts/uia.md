---
sidebar_position: 3
sidebar_label: UIA Automation 
---
# UIA Automation 
## Overview

Clicknium UIA automation is based on Microsoft UI Automation to support the recording function, generating locator, and all operations on UI elements.  
During recording, for the Windows applications, such as notepad, calculator, and ERP client applications, Clicknium will use UIA automation to record the element.

## Locator attributes
You can learn [locator](locator.md) concept first. For UIA automation, the attributes are defined below:

| Name      | equals | contains |startWith |endWith | regex
| ----------- | ----------- |----------- |----------- |----------- |----------- |
| Name |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| AutomationId |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| ClassName |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| HelpText |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| Role |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| IsDirectChild |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| AccessKey |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| IsPassword |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| AcceleratorKey |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| ItemType |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| ItemStatus |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| Orientation |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| Index |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|

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
By [find_element](../references/python/globalfunctions/find_element.md) on one UIA locator, you can get one UIA element, and properties of the element by [get_property](../references/python/uielement/get_property.md).  
Clicknium UIA supports the following properties:  

| Name      | Description |
| ----------- | ----------- |
| Name      |  The name of the user interface. |
| IsEnabled  | Whether the element is enabled in the user interface. |
| AccessKey   | A string containing the access key character for the element. |
| AutomationId | A string containing the UI Automation identifier (ID) for the element. |
| BoundingRectangle   | The coordinates of the rectangle that completely encloses the element. |
| ProcessId   | The process identifier (ID) of the element. |
| ItemType   | The description of the item type. |
| IsPassword   |  Whether the UI Automation element contains protected content. |
| IsOffscreen   |  Whether the UI Automation element is visible on the screen(true when the control is not visible; otherwise false). |
| AcceleratorKey   | A string containing the accelerator key combinations for the element. |
| HelpText   | The help text of the element. |
| IsKeyboardFocusable   | Whether the UI Automation element can accept keyboard focus. |
| IsContentElement   | Whether the element is a content element. |
| IsControlElement   | Whether the element is viewed as a control. |
| HasKeyboardFocus   | Whether the element has keyboard focus. |
| FrameworkId   | The name of the UI framework, such as "Win32", "WinForm", or "DirectUI". The default value is an empty string. |
| ControlType | The ControlType of the element. |
