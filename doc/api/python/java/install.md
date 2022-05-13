# install

***def install(self, java_install_path: str = '') -> None*** 

Install java extension.

**Parameters:**  
    &emsp;**java_install_path**: str  
        &emsp;&emsp; java install path string, you can provide java install path like `"C:\\Program Files\\Java\\jdk-17.0.2\\bin"`. If you don't give that path, it will scan java install path under "Program Files && Program Files (x86)"

**Returns:**  
    &emsp;None

**TODO----steps+update link in popup window**

**Remark:**  
    &emsp;1. Make sure you have installed java or jre.

**Example:**
***
```python
    from clicknium import clicknium as cc

    # get java driver
    java_driver = cc.java

    # install java extension with default java install path "Program Files && Program Files (x86)"
    java_driver.install()

    # install java extension with specified java install path
    java_driver.install(java_install_path = "C:\\Program Files\\Java\\jdk-17.0.2\\bin")

```