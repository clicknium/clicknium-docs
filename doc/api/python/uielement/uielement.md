# UiElement <!-- {docsify-ignore-all} -->
**UiElement class provides common operations for web, desktop's uielement.**  

## property

- `parent`   
    the element's parent element, return UiElement

- `children`  
    the element's children elements, return list of UiElement

- `next_sibling`  
    the element's next sibling element

- `previous_sibling`  
    the element's previous sibling element

## methods
- [child](/doc/api/python/uielement/child.md)：get child element with index
- [click](/doc/api/python/uielement/click.md)：click the element
- [double_click](/doc/api/python/uielement/double_click.md)：double click the element
- [drag_drop](/doc/api/python/uielement/drag_drop.md): holds down the left mouse button on the element, then moves to the target offset
- [get_position](/doc/api/python/uielement/get_position.md): get the element's position
- [get_property](/doc/api/python/uielement/get_property.md): get property value of the element
- [get_size](/doc/api/python/uielement/get_size.md): get the element's size
- [set_text](/doc/api/python/uielement/set_text.md): set the element's text
- [get_text](/doc/api/python/uielement/get_text.md): get the element's text
- [clear_text](/doc/api/python/uielement/clear_text.md): clear the element's text
- [highlight](/doc/api/python/uielement/highlight.md): highlight the element with specified color
- [hover](/doc/api/python/uielement/hover.md): hover on the element, the mouse will move upon the element for a while
- [save_to_image](/doc/api/python/uielement/save_to_image.md): save the element's screenshot to file with specified size and offset
- [select_item](/doc/api/python/uielement/select_item.md): select one option for the element
- [select_items](/doc/api/python/uielement/select_items.md): select multiple options for the element
- [send_hotkey](/doc/api/python/uielement/send_hotkey.md): send hot key based on the element
- [set_checkbox](/doc/api/python/uielement/set_checkbox.md): do check operation on the element
- [set_focus](/doc/api/python/uielement/set_focus.md): set focus for the the element

