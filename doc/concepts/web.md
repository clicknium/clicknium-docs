---
sidebar_position: 3
sidebar_label: Web Automation 
---
# Web Automation 
## Overview

Clicknium web automation support the following popular web browsers: Chrome, Microsoft Edge, IE, Firefox.
You need install extension for [Chrome](./../tutorial/extensions/chromeextension.md), [Edge](./../tutorial/extensions/edgeextension.md) or [Firefox](./../tutorial/extensions/firefoxextension.md) before recording.  
During recording, if you choose the web browser page, clicknium will use specified web automation to record the element.

## Locator attributes
You can get [locator](locator.md) concept first, for web automation, the attributes defined are as the following:

## Tab
| Name      | equals | contains |startWith |endWith |
| ----------- | ----------- |----------- |----------- |----------- |
| Name |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| Title |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| URL |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| ClassName |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| Role |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| Index |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|

## Web
| Name      | equals | contains |startWith |endWith |
| ----------- | ----------- |----------- |----------- |----------- |
| Name |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| Id |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| Type |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| AncestorId |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| AncestorName |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| CssSelector |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| XPath |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| SInfo |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| TabIndex |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| Href |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| Src |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| Title |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| Tag |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| TableRow |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| TableCol |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| IsLeaf |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| Index |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|

## Locator samples

-  azure devops 'A' element
```xml
<Application processName="chrome" filePath="chrome.exe" version="1.3" />
<Tab className="Chrome_WidgetWin_1" role="window" title="sprint query - Boards" />
<Web ancestorId="row_vss_4_4" tag="A" />
```
- bing search input
```xml
<Application processName="msedge" filePath="msedge.exe" version="1.3" />
<Tab className="Chrome_WidgetWin_1" role="window" url="https://*bing.com/" />
<Web id="sb_form_q" name="q" tag="INPUT" />
```
- bing search icon
```xml
<Application processName="msedge" filePath="msedge.exe" version="1.3" />
<Tab className="Chrome_WidgetWin_1" role="window" url="https://*bing.com/" />
<Web ancestorId="search_icon" tag="svg" />
```
- bing search result item
```xml
<Application processName="msedge" filePath="msedge.exe" version="1.3" />
<Tab className="Chrome_WidgetWin_1" role="window" url="https://*bing.com/search?*" />
<Web ancestorId="b_results" cssSelector="body>div>main>ol>li h2>a" tag="A" />
```

## Web element properties
By [find_element](../references/python/globalfunctions/find_element.md) on one web locator, you can get one web element, you can get properties of the element by [get_property](../references/python/uielement/get_property.md), Clicknium web element support the following properties:

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
