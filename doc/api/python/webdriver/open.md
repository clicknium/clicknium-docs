# open

***def open(
        self,
        url: str,
        is_maximize: bool = True,
        is_wait_complete: bool = True,
        userdata_folder_mode: Literal["automatic", "defaultfolder", "customfolder"] = WebUserDataMode.Automatic,
        userdata_folder_path: str = "",
        timeout: int = 30
    ) -> Browser***  

Open browser with specified website to get a browser object

>**Remarks:**  
>- When you use the function open and run the python script with VSCode's "Start Debugging (F5)" or "Run Without Debugging (Ctrl+F5)", the open browser will be closed.

**Parameters:**  
    &emsp;**url[Required]**: str   
        &emsp;&emsp; website string, ex: <https://www.bing.com>  
    &emsp;**is_maximize**: bool  
        &emsp;&emsp; is_maximize is set to define whether to maximize the browser window. Default is True. 
    &emsp;**is_wait_complete**: bool  
        &emsp;&emsp; is_wait_complete is set to define whether to wait for the broswser to load completely. Default is True. 
    &emsp;**userdata_folder_mode**: WebUserDataMode  
        &emsp;&emsp; userdata_folder_mode defines whether using customized user data folder when opening the browser.  
        &emsp;&emsp; **Automatic**：use user data folder automatically  
        &emsp;&emsp; **DefaultFolder**：use default user data folder  
        &emsp;&emsp; **CustomFolder**：use the folder specified with parameter 'userdata_folder_path'  
    &emsp;**userdata_folder_path**: str  
        &emsp;&emsp; user data's folder path  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, Unit is second,and default value is 30 seconds. 

**Returns:**  
    &emsp;[Browser](./doc/api/python/webdriver/browser/browser.md) object, you can execute the following operation in the browser, such as: find_element, close_tab, refresh and so on.

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