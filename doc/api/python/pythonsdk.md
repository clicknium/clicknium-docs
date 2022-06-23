# Overview  <!-- {docsify-ignore-all} -->

## Install Clicknium Python SDK

### System Requirements​
- Python 3.7 or above  

Install Clicknium automation sdk through [pip](https://pypi.org/project/clicknium/)  

```
# python version is 3.8 or below
pip install clicknium

# python version is 3.9 or above
pip install --pre pythonnet
pip install clicknium
```

## API reference  
Clicknium python sdk provides ways to automate various applications, such as **Web** browser, **Windows Desktop** application, **Java** application, **SAP** windows Gui app, etc. 
A sample code to drive web automation with clicknium is as follows.
```
from clicknium import clicknium as cc, locator, ui

# open new browser window
chrome_tab = cc.chrome.open("https://www.bing.com")
chrome_tab.find_element(locator.chrome.bing.search_sb_form_q).set_text("automation")
chrome_tab.find_element(locator.chrome.bing.svg).click()

# automation on already opened browser
chrome_tab = cc.chrome.attach_by_title_url(url="https://www.bing.com")
chrome_tab.find_element(locator.chrome.bing.search_sb_form_q).set_text("automation")
chrome_tab.find_element(locator.chrome.bing.svg).click()

# you can also use the following api directly, we will do attach browser automatically
ui(locator.chrome.bing.search_sb_form_q).set_text("automation")

$ for windows application
ui(locator.notepad.document_15).set_text("clicknium")

```
