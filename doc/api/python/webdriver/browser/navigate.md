# navigate

***def navigate(
        self,
        url: str,
        is_wait_complete: bool = True,
        timeout: int = 30
    ) -> None***  

In current open browser, navigate to other website.

**Parameters:**  
    &emsp;**url[Required]**: str   
        &emsp;&emsp; website string, eg: <https://www.bing.com>  
    &emsp;**is_wait_complete**: bool  
        &emsp;&emsp; is_wait_complete is set to define whether to wait for the broswser to load completely. Default is True. 
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, Unit is second, and default value is 30 seconds. 

**Returns:**  
    &emsp;None

**Example:**
***
```python
    from clicknium import clicknium as cc

    # open chrome browser
    chrome_browser = cc.chrome.open("https://www.bing.com")

    # naviage to another website
    chrome_browser.navigate("https://google.com")

```