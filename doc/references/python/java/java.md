# Java 

**Java class provides methods to operate Java extension.**

`clicknium.java`: The Java driver instance.

## Property

`extension`: return the Java extension.

### Extension Methods 

- [install](./install.md): install Java extension
- [uninstall](./uninstall.md): uninstall Java extension

### Examples

- You may install Java extension by the following way.
```python
  from clicknium import clicknium as cc
  cc.java.extension.install()
```