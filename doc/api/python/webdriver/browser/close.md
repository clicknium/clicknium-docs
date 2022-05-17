# close

***def close(self) -> None***  

Close browser.

**Parameters:**  
    &emsp;None

**Returns:**  
    &emsp;None

**Example:**
***
```python
    from clicknium import clicknium as cc

    # open chrome browser
    chrome_browser = cc.chrome.open("https://www.bing.com")

    # close the browser
    chrome_browser.close()
```