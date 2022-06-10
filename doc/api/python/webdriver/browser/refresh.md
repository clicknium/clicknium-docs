# refresh

***def refresh(
        self,
        is_wait_complete: bool = True,
        timeout: int = 30
    ) -> None***  

Refresh the current browser

**Parameters:**  
    &emsp;**is_wait_complete**: bool  
        &emsp;&emsp; is_wait_complete is set to define whether to wait for the broswser to fully load. Default is True.  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, Unit is second, ana default value is 30 seconds. 

**Returns:**  
    &emsp;None

**Example:**
***
```python
    from clicknium import clicknium as cc

    # open chrome browser
    chrome_browser = cc.chrome.open("https://www.bing.com")

    # refresh browser
    chrome_browser.refresh()

```