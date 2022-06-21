# install

***def install(self) -> None*** 

Install web extension.

>**Remarks:**  
>- Before installing extension, make sure you have already closed the related browsers. 
>- When extension is installed successfully, you should turn on the extension manually.  
>- Refrenece: [Install extensions from vscode](./doc/developtools/extensions/extensions.md).

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