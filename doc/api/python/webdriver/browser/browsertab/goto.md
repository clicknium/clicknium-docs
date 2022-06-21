# goto

***def goto(
        self,
        url: str
    ) -> None***  

Redirect current tab to the given url.

**Parameters:**  
    &emsp;**url[Required]**: str   
        &emsp;&emsp; website string, eg: <https://www.bing.com>  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;None

**Example:**
***
```python
    from clicknium import clicknium as cc

    # open chrome browser
    chrome_tab = cc.chrome.open("https://www.bing.com")

    # naviage to another website
    chrome_tab.goto("https://google.com")

```