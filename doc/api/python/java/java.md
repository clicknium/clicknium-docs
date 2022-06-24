# Java <!-- {docsify-ignore-all} -->

**Java class provides methods to operate java extension.**

`clicknium.java`: The java driver instance.

## Property

`extension`: return the java extension.

### Extension Methods 

- [install](./doc/api/python/java/install.md): install java extension
- [uninstall](./doc/api/python/java/uninstall.md): uninstall java extension

### Examples

- You may install java extension by the following way.
```python
  from clicknium import clicknium as cc
  cc.java.extension.install()
```