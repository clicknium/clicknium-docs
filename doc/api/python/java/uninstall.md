# uninstall

***def uninstall(self, java_install_path: str = '') -> None*** 

Uninstall java extension.

**Parameters:**  
    &emsp;**java_install_path**: str  
        &emsp;&emsp; For java install path string, you can provide java install path as `"C:\\Program Files\\Java\\jdk-17.0.2\\bin"`. If you don't give that path, it will scan java install path under "Program Files && Program Files (x86)"

**Returns:**  
    &emsp;None

**Example:**
***
```python
    from clicknium import clicknium as cc

    # get java driver
    java_driver = cc.java

    # uninstall java extension with default java install path "Program Files && Program Files (x86)"
    java_driver.extension.uninstall()

    # uninstall java extension with specified java install path
    java_driver.extension.uninstall(java_install_path = "C:\\Program Files\\Java\\jdk-17.0.2\\bin")

```