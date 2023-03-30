---
sidebar_position: 6
sidebar_label: JAVA Automation 
---
# JAVA Automation
## Overview

Clicknium JAVA automation is based on JAVA Access Bridge to support recording function, locator and all operations on UI elements.   
During recording, if you are recording a JAVA application, for example some ERP JAVA client, Clicknium will use JAVA automation to record the element.
You need install [JAVA extension](./../tutorial/extensions/javaextension.md) first.
Currently, the JAVA extension is compatible with JAVA 1.6 and above but below **JAVA 14**. Please follow the [configration steps for JAVA 9+ environment](../tutorial/extensions/javaextension.md#configration-steps-for-java-9-environment).

## Locator attributes
You can learn [locator](./locator.md#advanced-locator) concept first. For JAVA automation, the attributes defination is in the following table:

| Name      | equals | contains |startWith |endWith |regex |
| ----------- | ----------- |----------- |----------- |----------- |----------- |
| Name |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| ClassName |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| IsDirectChild |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| AccessKey |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| Index |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|

## Locator samples
We use one JAVA Swing sample application to show locator samples
-  awt component
```xml
<Application processName="javaw" filePath="javaw.exe" version="1.3" />
<Java className="frame" isDirectChild="True" name="SwingSet2" />
<Java className="root pane" isDirectChild="True" />
<Java className="layered pane" isDirectChild="True" />
<Java className="panel" isDirectChild="True" />
<Java className="panel" isDirectChild="True" />
<Java className="page tab list" isDirectChild="True" />
<Java className="page tab" isDirectChild="True" name="Internal Frames Demo" />
<Java className="panel" isDirectChild="True" />
<Java className="panel" isDirectChild="True" />
<Java className="desktop pane" isDirectChild="True" />
<Java className="internal frame" isDirectChild="True" name="Frame 4  " />
<Java className="AWT component" isDirectChild="True" />
```
- menu `Themes`
```xml
<Application processName="javaw" filePath="javaw.exe" version="1.3" />
<Java className="frame" isDirectChild="True" name="SwingSet2" />
<Java className="root pane" isDirectChild="True" />
<Java className="layered pane" isDirectChild="True" />
<Java className="menu bar" isDirectChild="True" name="Swing demo menu bar" />
<Java className="menu" isDirectChild="True" name="Themes" />
```
- toggle button
```xml
<Application processName="javaw" filePath="javaw.exe" version="1.3" />
<Java className="frame" isDirectChild="True" name="SwingSet2" />
<Java className="root pane" isDirectChild="True" />
<Java className="layered pane" isDirectChild="True" />
<Java className="panel" isDirectChild="True" />
<Java className="panel" isDirectChild="True" />
<Java className="panel" isDirectChild="True" />
<Java className="panel" isDirectChild="True" />
<Java className="tool bar" isDirectChild="True" />
<Java className="toggle button" index="3" isDirectChild="True" />
```
- text input
```xml
<Application processName="javaw" filePath="javaw.exe" version="1.3" />
<Java className="frame" isDirectChild="True" name="SwingSet2" />
<Java className="root pane" isDirectChild="True" />
<Java className="layered pane" isDirectChild="True" />
<Java className="panel" isDirectChild="True" />
<Java className="panel" isDirectChild="True" />
<Java className="page tab list" isDirectChild="True" />
<Java className="page tab" isDirectChild="True" name="Internal Frames Demo" />
<Java className="panel" isDirectChild="True" />
<Java className="panel" isDirectChild="True" />
<Java className="desktop pane" isDirectChild="True" />
<Java className="internal frame" isDirectChild="True" name="Internal Frame Generator" />
<Java className="root pane" isDirectChild="True" />
<Java className="layered pane" isDirectChild="True" />
<Java className="panel" isDirectChild="True" />
<Java className="panel" index="3" isDirectChild="True" />
<Java className="text" isDirectChild="True" />
```

## JAVA element properties
By [find_element](./../references/python/globalfunctions/find_element.md) on one JAVA locator, you can get one JAVA element, you can get properties of the element by [get_property](./../references/python/uielement/get_property.md), Clicknium JAVA support the following properties:

| Name      | Description |
| ----------- | ----------- |
| Name      |name of the user interface |
| BoundingRectangle   |the coordinates of the rectangle that completely encloses the element|
| States    |  states of elements such as enabled, visible, showing, focusable       |
| IndexInParent   | the index of current UI element in parent element |
| IsKeyboardFocusable   |  whether the UI element can accept keyboard focus |
| IsEditable   |  whether the UI element is editable or not |
| IsOffscreen   | whether the UI element is visible on the screen(true when the control is not visible; otherwise false)|
| ProcessId   |the process identifier (ID) of this element|
