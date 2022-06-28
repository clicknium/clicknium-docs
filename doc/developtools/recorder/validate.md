# Validate<!-- {docsify-ignore-all} -->

Validate can be used to judge the validity of the locator. 

- [Start validate](#start-validate)
- [Locator validation](#locator-validation)
    - [Single locator](#single-locator)
    - [Single locator with variables](#single-locator-with-variables)
    - [Single locator with mutiple windows](#single-locator-with-mutiple-windows)
    - [Mutiple similar locators](#mutiple-similar-locators)
- [Validation result](#validation-result)

## Start validate
You can validate from locator viewer tab in Visual Studio Code. 
    ![vscode validate](../../img/recorder_validate_vscode.png)

## Locator validation
### Single locator

Press the button `Validate`, and get validation result refer to [Validation result](#validation-result).

### Single locator with variables

1. Record a locator, and modify the locator with variables, for more about variables, please refer to [Parametric Locator](./doc/automation/parametric_locator.md).
![locator variables](../../img/locator_variables.png)
2. Press the button `Validate`, popup window as follows:  
![validate variable window](../../img/validate_variable_window.png)
3. Input varible value, then press the button `Continue`
4. Get validation result refer to [Validation result](#validation-result)

### Single locator with mutiple windows
1. If your locator can be found in mutiple windows, press the button `Validate`, popup window will as follows:  
![validate muti windows](../../img/validate_muti_window.png)
2. Select the index of window to get correct window, then press the button `Continue`
3. Get validation result refer to [Validation result](#validation-result)

### Mutiple similar locators
1. Record a locator, and modify the locator with wildword as follows:
![locator wildword](../../img/locator_wildword.png)
2. Select the index of the element, then Press `OK`  
![validate muti locators](../../img/validate_muti_locators.png)
3. Get validation result refer to [Validation result](#validation-result)


## Validation result
- When validating the locator successfully, the UI element will be highlighted, and locator viewer tab in Visual Studio Code as follows:
![validate success](../../img/validate_success.png)

- When validating the locator failed, the locator viewer tab in Visual Studio Code as follows:
![validate fail](../../img/validate_err.png)



