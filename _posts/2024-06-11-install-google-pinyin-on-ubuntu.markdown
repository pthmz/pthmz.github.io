---
layout: post
title:  "在Ubuntu衍生版上安装Google拼音"
date:   2024-06-11 22:00:00 +0800
categories: os
---
在 Lubuntu 24.04 和 Ubuntu Studio 24.04 上测试成功
- 安装`Fcitx`和`Google拼音`
```bash
sudo apt install fcitx fcitx-googlepinyin
```
- Logout
- 重新登录
- 进入Fcitx Configuration
	- 点击`+`
	- 取消勾选`Only Show Current Language`
	- 搜索Google Pinyin（不区分大小写）
	- 选中，点击OK
- 在任意输入框使用`Ctrl`+`Space`与英文输入法切换

`fcitx` 似乎已经不更新，过时。`fcitx5`似乎是一个更好的替代品？
