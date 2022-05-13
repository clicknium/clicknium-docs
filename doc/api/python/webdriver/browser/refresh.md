# refresh

***def refresh(
        self,
        is_wait_complete: bool = False,
        timeout: int = 30
    ) -> None***  

Refresh the current browser.

**Parameters:**  
    &emsp;**is_wait_complete**: bool  
        &emsp;&emsp; is_wait_complete is set to define whether to wait for a broswser to load completely. Default is False  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, unit is second, default value is 30 seconds 

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