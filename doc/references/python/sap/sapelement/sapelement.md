# SapElement 

- extends: [UiElement](../../uielement/uielement.md) 

**SapElement inherits from UiElement, representing an SAP element with SAP specific automation operations.**  

## Properties

- `parent`: parent element, return SapElement.

- `children`: child elements, return list of SapElement.

- `next_sibling`: next sibling element, return SapElement.

- `previous_sibling`: previous sibling element, return SapElement.

## Methods 
- [child](./child.md)：get child element by given index.
- [select_item](./select_item.md): select the SAP item.
- [call_transaction](./call_transaction.md): call the SAP transaction.
- [get_statusbar](./get_statusbar.md): get information of the SAP status bar.



