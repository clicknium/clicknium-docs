# Code IntelliSense<!-- {docsify-ignore-all} -->

  - [Code Complete](#code-complete)
  - [Locator Error Hint](#locator-error-hint)
  - [Locator Hover](#locator-hover)
  - [Auto Fill](#auto-fill)


## Code Complete
使用clicknium库下的locator。在locator后输入字符"."后，会自动提示项目中引用的Store，Store后输入"."后会提示Store下的folder和locator。
![code complete](../../img/vscode-code-complete.png)

## Locator Error Hint
### 类型错误
- ui或find_element函数参数必须是locator，如果是store或folder会提示错误信息
![type error](../../img/vscode-type-error.png)
### locator不存在
- 输入的locator在引用的store中不存在，会提示错误信息
![not exist](../../img/vscode-locator-not-exist.png)
- 选择Quick Fix打开录制器，录制元素后会已当前不存在的locator命名生成locator
  
## Locator Hover
- 鼠标滑到代码中的locator上，会提示locator的内容，便于识别。
![locator hover](../../img/vscode-code-hover.png)
- Open:打开对应的locator，方便编辑
- Validate:验证locator
- Recapture:打开录制器，重新录制locator，录制后的locator跟编辑窗口中的不同，会直接保存。

## Auto Fill
1. 代码中按快捷键ctrl+f10或右键菜单中点击Capture,会打开录制器录制。
2. 录制好后，录制器中选择希望填充的locator。
3. 点击OK后，locator会自动填充到代码中。