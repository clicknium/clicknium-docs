# attach_by_title_url

***def attach_by_title_url(
        self,
        title: str = '',
        url: str = '',
        is_maximize: bool = True,
        timeout = 30
    ) -> BrowserTab***  

Attach to an opened browser tab with specified title and/or url.

**Parameters:**  
    &emsp;**title**: str   
        &emsp;&emsp; title string, current web page's title, supporting wildcard.  
    &emsp;**url**: str  
        &emsp;&emsp; url string, current web page's url, supporting wildcard.  
    &emsp;**is_maximize**: bool  
        &emsp;&emsp; is_maximize is set to define whether to maximize the browser window, and the default value is True.  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds.

**Returns:**  
    &emsp;[BrowserTab](./doc/api/python/webdriver/browser/browser_tab.md) object, you can execute following operations in the browser tab: find_element, find_elements, close, refresh and so on.

**Example:**
***
```python
    from clicknium import clicknium as cc

    # attach ie browser, by title and url
    ie_tab = cc.ie.attach_by_title_url("bing", "https://cn.bing.com/")

    # attach chrome browser, by title only
    chrome_tab = cc.chrome.attach_by_title_url("bing")

    # attach edge browser, by url only
    edge_tab = cc.edge.attach_by_title_url(url = "https://cn.bing.com/")

    # attach firefox browser, by title with wildcard
    firefox_tab = cc.firefox.attach_by_title_url("bi*", "https://cn.bing.com/")
```