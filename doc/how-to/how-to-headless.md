---
sidebar_position: 5
sidebar_label: Use Headless Browser
---

# How to Use Headless Browser

## Introduction
A headless browser is a web browser without a graphical user interface. Instead of testing a site or performing common actions using familiar graphical elements, use cases are automated and tested in the background.

Headless browsers are commonly used for:
- Website and application testing
- JavaScript library testing
- JavaScript simulation and interactions
- Running one or more automated UI tests in the background.  

Clicknium supports headless mode via Chrome Devtools Protocol (CDP).

## How to use headless mode in Clicknium
### Requirement:
- Chrome or Edge browsers
- Clicknium SDK version >= 0.1.14  

Starting from Version 0.1.12, Clicknium supports CDP for Chrome and Edge, so you do not need to install the Clicknium browser automation extension to run the script. Please note that the browser automation extension is a must-have for the recorder when generating a browser locator.  
Based On CDP, Clicknium starts to support headless mode after 0.1.14. The locators can work in both CDP and non-CDP modes, and the APIs are also the same. The only difference is in the browser class. 
```python
from clicknium import clicknium as cc, locator
# Non-CDP
tab = cc.chrome.open("https://www.clicknium.com/")

# CDP
tab_cdp = cc.chromecdp.open("https://www.clicknium.com/" )

# CDP with Headless
tab_cdp_headless = cc.chromecdp.open("https://www.clicknium.com/", args=["--headless"])

```

Please note that simulating the mouse and keyboard is unavailable in Headless mode since there is no GUI to click and type. Clicknium CDP mode can only manage the browser tab created by its process. It cannot attach existing browser tabs. So you have to use the same tab object that CDP API opens.   


## Sample Code:  
```python
from clicknium import clicknium as cc

tab = cc.chromecdp.open("https://www.clicknium.com/documents/overview", args=["--headless"])
text = tab.find_element_by_xpath("//p[contains(text(),'is a next-generation GUI automation framework for ')]").get_text()
print(text)

```