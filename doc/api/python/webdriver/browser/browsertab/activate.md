# activate

***def activate(
        self,
        is_topmost: bool = True
    ) -> None***  

Activate the current tab.

**Parameters:**  
    &emsp;**is_topmost**: bool    
        &emsp;&emsp; it defines whether to set the window on topmost

**Returns:**  
    &emsp;None

**Example:**
***
```python
    from clicknium import clicknium as cc

    # open chrome browser
    chrome_tab = cc.chrome.open("https://www.bing.com")

    # activate the tab
    chrome_tab.activate()

```