# Overview

## API reference  <!-- {docsify-ignore} -->
Clicknium python sdk provides methods to automation variety applications, such as **Web** browser, **Windows Desktop** application, **Java** application, **Sap** windows Gui app etc. 
The following is a sample code of using clicknium to drive web automation:
```
from clicknium import clicknium as cc, locator, ui

# open new browser window
driver = cc.chrome.open("https://www.bing.com")
driver.find_element(locator.chrome.bing.search_sb_form_q).set_text("automation")
driver.find_element(locator.chrome.bing.svg).click()

# automation on already opened browser
ui(locator.chrome.bing.search_sb_form_q).set_text("automation")
ui(locator.chrome.bing.svg).click()
```

## Project  <!-- {docsify-ignore} -->

Pip: https://python.com/clicknium  
Github: https://github.com/clicknium
