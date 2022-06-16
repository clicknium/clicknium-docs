# navigate

***def navigate(
        self,
        url: str,
        is_wait_complete: bool = True,
        timeout: int = 30
    ) -> None***  

Navigate to another website.

**Parameters:**  
    &emsp;**url[Required]**: str   
        &emsp;&emsp; website string, eg: <https://www.bing.com>  
    &emsp;**is_wait_complete**: bool  
        &emsp;&emsp; is_wait_complete, define whether to wait for the browser to load completely, and the default value is True. 
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