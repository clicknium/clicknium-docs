# Parametric Locator
Parametric locator uses parameter in locator string as value or partial value of the attribute in locator. User can use the parametric locator in automation project, and replace the parameters in locator with the varaible or data in project. This allows the locator to stand for a series of elements, not only one target element.
- dynamic value: {{varaible}}, the variable in locator
  
format as the following:  
`<Web ancestorId="{{id}}" tag="A" />`
or set partial value as parameter:  
`<Web ancestorId="video-{{id}}" tag="A" />`

- Use parametric locator in project  
```python
    from clicknium import clicknium as cc, locator, ui

    #will replace varaible 'name' in parametric locator during runtime
    variables = {"name":"test"}
    ui(locator.chrome.bing.search_sb_form_q, variables)
```

# Examples
To illustrate parametric locator functionality, we use the following two samples, one is for web page, the other is for windows applciation.  
## Web Example  
![sample1](img/parametric_locator_sample1.png)  
to locator the item in list, after record, the locator string as the following:  
![sample1](img/parametric_locator_sample1_2.png)  
To iterate access each item, we can add parameter as the following:  
![sample1](img/parametric_locator_sample1_3.png)  

```python
    from clicknium import clicknium as cc, locator, ui

    index = 1
    driver = cc.chrome.open("https://getbootstrap.com/docs/5.1/forms/input-group/")
    while True:
        variables = {"index":index}
        if driver.is_exist(locator.chrome.getbootstrap.li_anitem, variables):
            text = driver.find_element(locator.chrome.getbootstrap.li_anitem, variables).get_text()
            print(text)
            index += 1
        else:
            break
```

## Windows application Example  
![sample1](img/parametric_locator_sample2.png)  
to locator the menu item, after record, the locator string as the following:  
![sample1](img/parametric_locator_sample2_2.png)  
To iterate access each menu item, we can add parameter as the following:  
![sample1](img/parametric_locator_sample2_3.png)  

```python
    from clicknium import clicknium as cc, locator, ui

    titles = {'File', 'Edit', 'Format', 'View', 'Help'}

    for title in titles:
        variables = {"title":title}
        text = ui(locator.chrome.getbootstrap.li_anitem, variables).get_text()
        print(text)
```