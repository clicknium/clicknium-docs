# open

***def open(
        self,
        url: str,
        is_maximize: bool = True,
        is_wait_complete: bool = False,
        userdata_folder_mode: Literal["automatic", "defaultfolder", "customfolder"] = WebUserDataMode.Automatic,
        userdata_folder_path: str = "",
        timeout: int = 30
    ) -> Browser***  

Open browser with specified website and get a browser object.

**Parameters:**  
    &emsp;**url[Required]**: str   
        &emsp;&emsp; website string, ex: <https://www.bing.com>  
    &emsp;**is_maximize**: bool  
        &emsp;&emsp; is_maximize is set to define whether to maximize the browser window. Default is True  
    &emsp;**is_wait_complete**: bool  
        &emsp;&emsp; is_wait_complete is set to define whether to wait for a broswser to load completely. Default is False  
    &emsp;**userdata_folder_mode**: WebUserDataMode  
        &emsp;&emsp; userdata_folder_mode define whether to use custom user data folder when opening browser  
        &emsp;&emsp; **Automatic**：it means use user data folder automatically  
        &emsp;&emsp; **DefaultFolder**：it means use default user data folder  
        &emsp;&emsp; **CustomFolder**： it means we will use the folder you specified with parameter 'userdata_folder_path'  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, unit is second, default value is 30 seconds 

**Returns:**  
    &emsp;[Browser](./doc/api/python/webdriver/browser/browser.md) object, you can use the browser to do the following operation: find_element, close_tab, refresh and so on

**Remark:**  
    &emsp;When you use the open function and run the python script with VSCode's "Start Debugging (F5)" or "Run Without Debugging (Ctrl+F5)", the opened browser will be closed after the run is finished. 

**Example:**
***
```python
    from clicknium import clicknium as cc

    # open ie browser
    ie_browser = cc.ie.open("https://www.bing.com")

    # open chrome browser
    chrome_browser = cc.chrome.open("https://www.bing.com")

    # open edge browser
    edge_browser = cc.edge.open("https://www.bing.com", is_wait_complete = True)

    # open firefox browser
    firefox_browser = cc.firefox.open("https://www.bing.com", timeout = 10)
```