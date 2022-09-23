# WebElement

- extends: [UiElement](./../../../../../python/uielement/uielement.md) 

**WebElement class inherits from UiElement, representing the web UI element with web specific operations.**  

## Properties

- `parent`: parent element, return WebElement.  

- `children`: child elements, return list of WebElement.  

- `next_sibling`: next sibling element, return WebElement.

- `previous_sibling`: previous sibling element, return WebElement.

## Methods
- [child](./child.md)：get child element by given index.
- [set_property](./set_property.md): set the property value of the web element.  
- [execute_js](./execute_js.md): execute Javascript code for the target element.  
- [execute_js_file](./execute_js_file.md): execute Javascript file for the target element.  
- [find_element](./find_element.md)：find element by the given locator.
- [find_element_by_xpath](./find_element_by_xpath.md)：find element by the given xpath.  
- [find_element_by_css_selector](./find_element_by_css_selector.md)：find element by the given css selector.
- [find_elements](./find_elements.md)：find elements by the given locator.
- [find_elements_by_xpath](./find_elements_by_xpath.md)：find elements by the given xpath.
- [find_elements_by_css_selector](./find_elements_by_css_selector.md)：find elements by the given css selector.


