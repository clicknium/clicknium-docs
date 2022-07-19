---
sidebar_position: 1
sidebar_label: install
---
# WebDriver.extension.install

***def install(self) -> None*** 

Install browser extension.

>**Remarks:**  
>- Before installing extension, make sure the related browsers are closed. 
>- When extension is installed successfully, you should turn on the extension manually.  
>- Refrenece: [Install extensions from vscode](./../../../../developtools/vscode//extensions/extensions.md).

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