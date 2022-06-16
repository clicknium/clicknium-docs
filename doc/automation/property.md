# UiElement Property<!-- {docsify-ignore-all} -->

- [UiElement Property](#uielement-property)
  - [Overview](#overview)
  - [Web Element Property](#web-element-property)
  - [UIA Element Property](#uia-element-property)
  - [Java Element Property](#java-element-property)

## Overview
Different UI elements support different property lists based on automation technology. The following tables list the properties supported.

## Web Element Property

| Name      | Description |
| ----------- | ----------- |
| pagetitle      |the title of the current HTML page|
| readystate      |the loading state of the document, return 1 if Document.readyState equals "complete" or return 0|
| ID     |the unique ID for an HTML element|
| URL      |URL of current page|
| htmlwindowname      |`window.name` in javascript|
| title      |the title of an element|
| cookie      |the cookies value, format is cookiename=value, multiple cookies split by ;|
| innertext      |the inner text of an element|
| innertextshort      |at most 512 char of innertext|
| outertext      |the outer text of an element|
| outertextshort      |at most 512 char of outertext|
| innerhtml      |the HTML content (inner HTML) of an element|
| innerhtmlshort      |at most 512 char of innerhtml|
| outerhtml      |the HTML elements, including attributes, start tag, and end tag|
| outerhtmlshort      |at most 512 char of outerhtml|
| tag      |the tag name of an element|
| ancestorid |a Clicknium custom property, the ID of first ancestor node with ID attribute in the DOM tree |
| ancestorname      |a Clicknium custom property,  the name of the first ancestor node with Name attribute in the DOM tree|
| ancestorcss      |a Clicknium custom property,  the class of the first ancestor node with Class attribute in the DOM tree|
| tablerow      |if the element is in one table, return the row of the element|
| tablecol      |if the element is in one table, return the column of the element|
| rowname      |row header name|
| colname      |column header name|
| columncount      |column count|
| rowcount      |row count|
| ischecked      |whether the element(checkbox, radio) is checked|
| sinfo      |a clicknium custom property, the text displayed|
| sinfoshort      |at most 512 char of sinfo|
| css_selector      |css selector|
| selecteditem      |the text of selected option|
| selecteditems      |the text of all options|
| isleaf      |a clicknium custom property, whether the node is leaf in DOM|
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

## Java Element Property

| Name      | Description |
| ----------- | ----------- |
| Name      |name of the user interface |
| BoundingRectangle   |the coordinates of the rectangle that completely encloses the element|
| States    |         |
| Actions   |         |
| Selection   |         |
| Hypertext   |         |
| Text   |         |
| Value   |         |
| Table   |         |
| IndexInParent   | the index of current UI element in parent element |
| IsKeyboardFocusable   |  whether the UI element can accept keyboard focus |
| IsEditable   |  whether the UI element is editable or not |
| IsOffscreen   | whether the UI element is visible on the screen(true when the control is not visible; otherwise false)|
| ProcessId   |the process identifier (ID) of this element|