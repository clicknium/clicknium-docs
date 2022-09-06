---
sidebar_position: 1
sidebar_label: open
---
# WebDriver.open

***def open(
        self,
        url: str,
        is_maximize: bool = True,
        is_wait_complete: bool = True,
        userdata_folder_mode: Literal["automatic", "default", "custom"] = WebUserDataMode.Automatic,
        userdata_folder_path: str = "",
        timeout: int = 30
    ) -> BrowserTab***  

Open browser with specified url to get a browser tab.

>**Remarks:**  
>- When you open and run the Python script with "Start Debugging (F5)" or "Run Without Debugging (Ctrl+F5)" in Visual Studio Code , the opened browser may be closed when exiting the debugging or running state.

**Parameters:**  
    &emsp;**url[Required]**: str   
        &emsp;&emsp; Url string, the target site url, eg.: <https://www.bing.com>.     
    &emsp;**is_maximize**: bool  
        &emsp;&emsp; is_maximize, whether to maximize the browser window, the default value is True.  
    &emsp;**is_wait_complete**: bool  
        &emsp;&emsp; is_wait_complete, whether to wait for the broswser to complete loading, the default value is True.  
    &emsp;**userdata_folder_mode**: WebUserDataMode  
        &emsp;&emsp; userdata_folder_mode defines whether using customized user data folder when opening the browser.  
        &emsp;&emsp; `automatic`：use user data folder automatically.  
        &emsp;&emsp; `default`：use default folder of the user data.  
        &emsp;&emsp; `custom`：use the folder specified by parameter 'userdata_folder_path'.  
    &emsp;**userdata_folder_path**: str  
        &emsp;&emsp; User data's folder path.  
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;[BrowserTab](./browser/browsertab/browsertab.md) object, you can execute the following operations in the browser tab such as: find_element, find_elements, close, refresh and so on.

**Example:**
***
```python
from clicknium import clicknium as cc

# open ie browser
ie_tab = cc.ie.open("https://www.bing.com")

# open chrome browser
chrome_tab = cc.chrome.open("https://www.bing.com")

# open edge browser
edge_tab = cc.edge.open("https://www.bing.com", is_wait_complete = True)

# open firefox browser
firefox_tab = cc.firefox.open("https://www.bing.com", timeout = 10)
```