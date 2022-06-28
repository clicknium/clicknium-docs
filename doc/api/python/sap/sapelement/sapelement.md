# SapElement <!-- {docsify-ignore-all} -->

- extends: [UiElement](./doc/api/python/uielement/uielement.md) 

**SapElement inherits from UiElement, representing an SAP element with SAP specific automation operations.**  

## Properties

- `parent`: parent element, return SapElement.

- `children`: child elements, return list of SapElement.

- `next_sibling`: next sibling element, return SapElement.

- `previous_sibling`: previous sibling element, return SapElement.

## Methods 

- [select_item](./doc/api/python/sap/sapelement/select_item.md): select the SAP item.
- [call_transaction](./doc/api/python/sap/sapelement/call_transaction.md): call the SAP transaction.
- [get_statusbar](./doc/api/python/sap/sapelement/get_statusbar.md): get information of the SAP status bar.



