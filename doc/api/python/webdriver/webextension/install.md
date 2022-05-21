# install

***def install(self) -> None*** 

Install web extension.

**Remarks:**  
    &emsp;1. Before installing extension, you should make sure you have already closed edge, firefox and chrome browser.  
    &emsp;2. When extension is installed successfully, then you should turn on the extension manually.  

**Example:**
***
```python
    from clicknium import clicknium as cc

    # install chrome extension
    cc.chrome.extension.install()

    # install edge extension
    cc.edge.extension.install()

    # install firefox extension
    cc.firefox.extension.install()
```