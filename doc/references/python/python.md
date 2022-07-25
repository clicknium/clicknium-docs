# Overview  

[Clicknium Python package](https://pypi.org/project/clicknium/) supports automating various types of applications, such as **Web** browser, **Windows** application, **Java** application and **SAP** Windows GUI App, etc.

## Install Clicknium Python pacakge

### System Requirements​
- Python 3.7 or above
- Windows 7 SP1 or above

### Install
```
# python version is 3.8 or below
pip install clicknium

# python version is 3.9 or above
pip install --pre pythonnet
pip install clicknium
```

## API reference   
- [Global Functions](./globalfunctions/globalfunctions.md)：the root level APIs for UI element.  
- [UiElement](./uielement/uielement.md): the UI element operations.  
- [WebDriver](./webdriver/webdriver.md): the web automation related objects and APIs.  
- [Window](./window/window.md): the window specific automation APIs.  
- [Sap](./sap/sap.md): the SAP specific automation APIs.   
- [Java](./java/java.md): the java extension APIs.  
- [Configuration](./config/config.md): the configuration setting APIs.
- [Exceptions](./exceptions/exceptions.md): the errors defined in clicknium.  

## Example
A sample code for web automation with clicknium is as follows.

```python
from clicknium import clicknium as cc, locator, ui

# open new browser window
chrome_tab = cc.chrome.open("https://www.bing.com")
chrome_tab.find_element(locator.chrome.bing.search_sb_form_q).set_text("clicknium")
chrome_tab.find_element(locator.chrome.bing.svg).click()

# automation on already opened browser
chrome_tab = cc.chrome.attach_by_title_url(url="https://www.bing.com")
chrome_tab.find_element(locator.chrome.bing.search_sb_form_q).set_text("clicknium")
chrome_tab.find_element(locator.chrome.bing.svg).click()

# you can also use the following api directly, clicknium will automatically attach to the browser
ui(locator.chrome.bing.search_sb_form_q).set_text("clicknium")

# for windows application
ui(locator.notepad.document_15).set_text("clicknium")

```
