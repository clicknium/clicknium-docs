# get_tab

***def get_tab(self, title = '', url = '') -> BrowserTab***  

Get tab by specified title and/or url.

**Parameters:**  
    &emsp;**title**: str   
        &emsp;&emsp; title string, current web page's title, supporting wildcard.  
    &emsp;**url**: str  
        &emsp;&emsp; url string, current web page's url, supporting wildcard. 

**Returns:**  
    &emsp;[BrowserTab](./doc/api/python/webdriver/browser/browser_tab.md) object, you can execute following operations in the browser tab: find_element, find_elements, close, refresh and so on.

**Example:**
***
```python
    from clicknium import clicknium as cc

    browser = cc.chrome.browsers[0]
    # by tile and url
    browser.get_tab("bing", "https://cn.bing.com/")

    # by title only
    browser.get_tab("bing")

    # by url only
    browser.get_tab(url = "https://cn.bing.com/")

    # by title with wildcard
    browser.get_tab("bi*", "https://cn.bing.com/")
```