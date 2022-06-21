# refresh

***def refresh(self) -> None -> None***  

Refresh the page of the current tab.

**Returns:**  
    &emsp;None

**Example:**
***
```python
    from clicknium import clicknium as cc

    # open chrome browser
    chrome_tab = cc.chrome.open("https://www.bing.com")

    # refresh browser tab
    chrome_tab.refresh()

```