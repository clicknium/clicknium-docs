# open

***def open(
        self,
        url: str,
        is_maximize: bool = True,
        is_wait_complete: bool = True,
        userdata_folder_mode: Literal["automatic", "defaultfolder", "customfolder"] = WebUserDataMode.Automatic,
        userdata_folder_path: str = "",
        timeout: int = 30
    ) -> BrowserTab***  

Open browser with specified url to get a browser tab.

>**Remarks:**  
>- When you open and run the python script with "Start Debugging (F5)" or "Run Without Debugging (Ctrl+F5)" in Visual Studio Code , the opened browser may be closed finally.

**Parameters:**  
    &emsp;**url[Required]**: str   
        &emsp;&emsp; url string, ex: <https://www.bing.com>  
    &emsp;**is_maximize**: bool  
        &emsp;&emsp; is_maximize, define whether to maximize the browser window, and the default value is True. 
    &emsp;**is_wait_complete**: bool  
        &emsp;&emsp; is_wait_complete is set to define whether to wait for the broswser to load completely, and the default value is True. 
    &emsp;**userdata_folder_mode**: WebUserDataMode  
        &emsp;&emsp; userdata_folder_mode defines whether using customized user data folder when opening the browser.  
        &emsp;&emsp; **Automatic**：use user data folder automatically  
        &emsp;&emsp; **DefaultFolder**：use default user data folder  
        &emsp;&emsp; **CustomFolder**：use the folder specified with parameter 'userdata_folder_path'  
    &emsp;**userdata_folder_path**: str  
        &emsp;&emsp; user data's folder path.  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second,and the default value is 30 seconds. 

**Returns:**  
    &emsp;[BrowserTab](./doc/api/python/webdriver/browser/browser_tab.md) object, you can execute the following operations in the browser tab such as, find_element, find_elements, close, refresh and so on.

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