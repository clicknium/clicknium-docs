# Overview

API refence for clicknium python sdk

**Project**  

Python sdk: https://python.com/clicknium  
Vscode extension: https://microsoft.com/clicknium  
Github: https://github.com/clicknium  

**Sample code** 

```python
    from clicknium import clicknium as cc, selectorstore

    #操作一个已经打开的浏览器
    cc.find_element(selectorstore.chrome.baidu.text_kw).set_text("rpa")
    cc.find_element(selectorstore.chrome.baidu.submit_su).click()

    #打开一个浏览器操作
    driver = cc.chrome.open("www.baidu.com")
    driver.find_element(selectorstore.chrome.baidu.text_kw).set_text("rpa")
    driver.find_element(selectorstore.chrome.baidu.submit_su).click()
    driver.close()
```