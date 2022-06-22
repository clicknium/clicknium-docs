## Overview

Locator Store Management
Locator manangement
Edit locator, recapture, validate (include case multiple window, multiple elements)
Edit locator/store, rename, delete, move locator/folde

## Store Management

- Create store: 创建一个新的 store
  1. 点击 `...`
  2. 点击 `Create Store` 菜单
  3. 输入 store 名字
  4. 按 `Enter` 或 `Tab` 保存
- Rename store: 重命名 store，新名字不可和其它 store 名字重复。
  - 通过快捷键
    1. 选择一个 store 按 `F2`
    2. 输入新的名字
    3. 按 `Enter` 或 `Tab` 保存
  - 通过菜单按钮
    1. 选择一个 store 右键鼠标
    2. 点击 `Rename`
    3. 输入新的名字
    4. 按 `Enter` 或 `Tab` 保存
- Remove Reference:移除对 Store 的引用，该 store 未保存的改动将会丢失。
  - 通过快捷键
    1. 选择一个 store 按 `Delete`
    2. 点击 `Yes` 确认移除
  - 通过菜单按钮
    1. 选择一个 store 右键鼠标
    2. 点击 `Remove Reference`
    3. 点击 `Yes` 确认移除

## Folder Management

- Add Folder:在 store 或者 folder 下创建 folder
  1. 选择 store 或者 folder 右键鼠标
  2. 点击 `Add Folder`
  3. 输入 folder 名字
  4. 按 `Enter` 或 `Tab` 保存
- Rename folder: 重命名 folder，新名字不可和其它 folder 或 locator 名字重复。
  - 通过快捷键
    1. 选择一个 folder 按 `F2`
    2. 输入新的名字
    3. 按 `Enter` 或 `Tab` 保存
  - 通过菜单按钮
    1. 选择一个 folder 右键鼠标
    2. 点击 `Rename`菜单
    3. 输入新的名字
    4. 按 `Enter` 或 `Tab` 保存
- Delete folder:删除 Folder，若其中包含 folder 和 locator 也一并删除。
  - 通过快捷键
    1. 选择一个 folder 按 `Delete`
    2. 点击 `Yes` 确认移除
  - 通过菜单按钮
    1. 选择一个 folder 右键鼠标
    2. 点击 `Delete`
    3. 点击 `Yes` 确认移除
- Move folder:通过拖拽，将 folder 移动至其它 store 或 folder

## Locator Management

- Recapture locator:可以重新弄捕获并覆盖之前的 locator
  1. 选择一个 locator 右键鼠标
  2. 点击 `Recapture`
  3. 捕获一个新元素
- Rename locator: 重命名 locator，新名字不可和其它 folder 或 locator 名字重复。
  - 通过快捷键
    1. 选择一个 locator 按 `F2`
    2. 输入新的名字
    3. 按 `Enter` 或 `Tab` 保存
  - 通过菜单按钮
    1. 选择一个 locator 右键鼠标
    2. 点击 `Rename`菜单
    3. 输入新的名字
    4. 按 `Enter` 或 `Tab` 保存
- Delete locator:删除 locator。
  - 通过快捷键
    1. 选择一个 locator 按 `Delete`
    2. 点击 `Yes` 确认移除
  - 通过菜单按钮
    1. 选择一个 locator 右键鼠标
    2. 点击 `Delete`
    3. 点击 `Yes` 确认移除
- Move locator:通过拖拽，将 locator 移动至其它 store 或 folder

## Validate

- 元素验证成功：
  高亮元素，并通知 VS Code 已经验证成功。
- 元素验证失败：
  通知 VS Code 验证失败，并给出失败原因。
- 多窗体验证：当打开了多个符合条件的窗体时，验证过程中可选择窗体，也可以取消本次验证。
- 多元素验证：当匹配到多个满足条件的元素时，可切换并高亮对应的元素，勾选`Single target`后，点击`OK`，当前的元素的 index 会写入 locator 中。
