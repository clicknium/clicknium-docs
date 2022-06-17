# Code IntelliSense<!-- {docsify-ignore-all} -->

  - [Code Complete](#edit-store)
  - [Locator Error Hint](#edit-folder)
  - [Locator Hover](#edit-locator)
  - [Auto Fill](#edit-locator)


## Code Complete
使用clicknium库下的locator。在locator后输入字符"."后，会自动提示项目中引用的Store，Store后输入"."后会提示Store下的folder和locator。
![code complete](../../img/vscode-code-complete.png)

## Locator Error Hint
### 类型错误
ui或find_element函数参数必须是locator，如果是store或folder会提示错误信息
![type error](../../img/vscode-type-error.png)
### locator不存在
输入的locator在引用的store中不存在，会提示错误信息
