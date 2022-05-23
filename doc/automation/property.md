# UiElement Property<!-- {docsify-ignore-all} -->

- [Web Element Property](#web-element-property)
- [UIA Element Property](#uia-element-property)
- [Java Element Property](#java-element-property)

## Overview
Different ui elements may support different property list, based on automation technology, the following tables list the properties supported.

## Web Element Property

| Name      | Description |
| ----------- | ----------- |
| pagetitle      |title of current HTML page|
| readystate      |the loading state of the document, return 1 if Document.readyState equals "complete" or return 0|
| Id      |a unique id for an HTML element|
| url      |url of current page|
| htmlwindowname      |`window.name` in javascript|
| title      |the title of an element|
| cookie      |the cookies value, format is cookiename=value, multiple cookies split by ;|
| innertext      |the inner text of an element|
| innertextshort      |at most 512 char of innertext|
| outertext      |the outer text of an element|
| outertextshort      |at most 512 char of outertext|
| innerhtml      |the HTML content (inner HTML) of an element|
| innerhtmlshort      |at most 512 char of innerhtml|
| outerhtml      |the HTML element, including attributes, start tag, and end tag|
| outerhtmlshort      |at most 512 char of outerhtml|
| tag      |the tag name of an element|
| ancestorid |clicknium custom property, from current element search up through the DOM tree, the first ancestor node with Id attribute, return the Id of that ancestor node|
| ancestorname      |clicknium custom property, from current element search up through the DOM tree, the first ancestor node with Name attribute, return the Name of that ancestor node|
| ancestorcss      |from current element search up through the DOM tree, the first ancestor node with class attribute, return the class of that ancestor node|
| tablerow      |if element is in one table, return the row of the element in that table|
| tablecol      |if element is in one table, return the column of the element in that table|
| rowname      |row header name|
| colname      |column header name|
| columncount      |column count|
| rowcount      |row count|
| ischecked      |whether the element(checkbox, radio) is checked|
| sinfo      |clicknium custom property, the text displayed|
| sinfoshort      |at most 512 char of sinfo|
| css_selector      |css selector|
| selecteditem      |the selected option's text|
| selecteditems      |all option text|
| isleaf      |clicknium custom property, whether the node is leaf in DOM|
| tabindex      |the value of the tabindex attribute of an element|
| href      |value of element's href attribute |
| XPath      |xpath value|
| Type      |value of element's type attribute|
| Src      |value of element's src attribute|
| Role      |value of element's role attribute|
| Name      |value of element's name attribute|

## UIA Element Property

| Name      | Description |
| ----------- | ----------- |
| Name      |  name of the user interface      |
| IsEnabled  |indicating whether this element is enabled in the user interface|
| AccessKey   |  a string containing the access key character for the element|
| AutomationId |a string containing the UI Automation identifier (ID) for the element|
| BoundingRectangle   | the coordinates of the rectangle that completely encloses the element|
| ProcessId   | the process identifier (ID) of this element|
| ItemType   | a description of the type of an item |
| IsPassword   | indicates whether the UI Automation element contains protected content|
| IsOffscreen   |  indicates whether the UI Automation element is visible on the screen(true if the control is not visible; otherwise false)|
| AcceleratorKey   | a string containing the accelerator key combinations for the element|
| HelpText   |the help text associated with the element|
| IsKeyboardFocusable   |indicates whether the UI Automation element can accept keyboard focus|
| IsContentElement   |specifies whether the element is a content element|
| IsControlElement   |indicates whether the element is viewed as a control|
| HasKeyboardFocus   | indicates whether the element has keyboard focus|
| FrameworkId   | the name of the underlying UI framework. The name of the UI framework, such as "Win32", "WinForm", or "DirectUI". The default value is an empty string.|
| ControlType | the ControlType of the element.|

## Java Element Property

| Name      | Description |
| ----------- | ----------- |
| Name      |name of the user interface |
|Role| |
| BoundingRectangle   |the coordinates of the rectangle that completely encloses the element|
| States    |         |
| Actions   |         |
| Selection   |         |
| Hypertext   |         |
| Text   |         |
| Value   |         |
| Table   |         |
| IndexInParent   |         |
| IsKeyboardFocusable   |         |
| IsEditable   |         |
| IsOffscreen   | indicates whether the UI Automation element is visible on the screen(true if the control is not visible; otherwise false)|
| ProcessId   |the process identifier (ID) of this element|