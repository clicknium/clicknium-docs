# Record<!-- {docsify-ignore-all} -->

- [How to start recorder](#how-to-start-recorder)
- [Record methods](#record-methods)
    - [Select record technology and advanced option](#select-record-technology-and-advanced-option)
    - [Single record](#single-record)
    - [Continuous record](#continuous-record)
    - [Image record](#image-record)
- [Record technology](#record-technology)
- [Record advanced option](#record-advanced-option)

## How to start recorder
- start from Visual Studio Code LOCATORS tab  
![start from vscode local locator](../../img/start_recorder_from_vscode.png)
- strat from Visual Studio Code CLOUD LOCATORS tab  
![start from vscode cloud locator](../../img/start_recorder_from_cloud.png)
- start with pressing hotkey `Ctrl+F10`  

## Record methods

We provide three recording methods: single record, continuous record and image record.

> **Remarks:**
>- The new recorded locator will be added into current selected store.

### Select record technology and advanced option
For each record method we can select record technology and advanced option, please refer to [Record Technology](#record-technology) and [Record Advanced Option](#record-advanced-option).

### Single record

1. Select UI element  
When mouse moving, it will highlight the UI element, and show its position on recorder panel.
![sigle record](../../img/recorder_single.png)
2. Press `Ctrl` + click
3. Press button `Complete`  
![record complete](../../img/recorder_complete.png)

### Continuous record

1. Operation multiple times "Select UI element and Press `Ctrl` + click" to add more locators
2. Press button `Complete` on recorder panel

### Image record

1. Select UI element  
2. Press `Shift` and select one area with the mouse to paint a rectangle for the element
3. Validate image locators are as follows:  
![image locator](../../img/record_image_locator.png)
4. Press button `Complete` on recorder panel

## Record technology

The supporting recorder technologies are as follows `UIA`, `IA`, `Java`, `IE`, `Chrome`, `Firefox`, `Edge` and `Sap`.  
The default technology is `Auto Detect`, which means the recorder will automatically select the technology.  
For web UI element, you can choose `IE`, `Chrome`, `Firefox` or `Edge` recorder technology according to your browser type.  
For SAP application, you can choose `Sap` recorder technology.  
For Java application, you can choose `Java` recorder technology.  
For window UI element, you can choose `UIA` or `IA` recorder technology.  
![select technology](../../img/record_choose_tech.png) 

## Record advanced option

Default advanced option is `None`. When recording web UI element, you can also select `XPath`, which will generate a xpath string.  
![select advance option](../../img/record_choose_advance.png)