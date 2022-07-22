# Locator
A locator is a way to identify elements on a web page or desktop app.   

# Overview 
Identification of the correct GUI element on a web page is pre-requisite for creating any successful automation script. It is where locators come into the picture. Locators are one of the essential components of Clicknium infrastructure, which help Clicknium scripts in uniquely identifying the UI elements(such as text box, button, etc.). 
The way to get a locator for a specific UI element is the key experience for automation framwork. Before Clicknium, you have to learn some web essential knowledge, such as XPath. Clicknium provides Clicknum Recorder to help you get a locator by just clicking the elements. 

# How to use
So, how do we get the values of these locators? And how to use the same in the automation framework? 

## Get a locator 
Clicknium provides Clicknium Recorder to get UI locators.  
- Make sure that Clicknium Python package, VS code extention, Chrome extension installed. 
- Open a Python file via VS code. 
- Use Recorder to capture locators.  

![show locator](./../img/showlocator.gif)  

## Use locator in Python Code
Clicknium provides intellgent auto-complete experience. You can find the exsiting locators captured by Clicknium Recorder in VS Code. Use the `locator` class under the Clicknium package. You can reference Locator by `Locator.{localorStoreName}.{folderName}.{LocatorName}`  Operate locators via Python code, run and waiting for a miracle to happen. 

![use locator](./../img/uselocator.gif)

# Locator Type








## Locator Error Hint
### Error Type
- ui or find_element function argument must be locator. If it is store or folder, an error message will be displayed.
![type error](../../doc/img/vscode-type-error.png)
### Locator Does Not Exsit
- If the entered locator does not exist in the referenced store, an error message is displayed.
![not exist](../../doc/img/vscode-locator-not-exist.png)
- Select `Quick Fix` to start the recorder. After recording elements, a locator that does not exist will be named to generate a locator.
  
## Locator Hover
- If you hover the mouse to the locator in the code, the locator content is displayed for easy identification.
![locator hover](../../doc/img/vscode-code-hover.png)
- `Open`: Open the corresponding locator to edit
- `Validate`: Validate the locator
- `Recapture`: Start the recorder to capture the locator again. If the recorded locator is different from the one in the editing window, it will be saved directly. 


## Auto Fill
1. Press the shortcut key CTRL+F10 or click  `Capture` in the right menu to start the recorder.
2. After recording, select a locator that is required to fill in the recorder.
3. After clicking `OK`, the locator will be automatically filled into the code.


