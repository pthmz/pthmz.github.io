---
layout: post
title:  "嵌入式 Python Windows 版 pip安装教程 (python-embed)"
date:   2024-03-26 16:00:00 +0800
categories: programming
---
本文与嵌入式硬件开发无关

**下载**

`python-3.xx.xx-embed-amd64.zip` 来自 [python.org](https://www.python.org/)

`get-pip.py` 来自 [https://bootstrap.pypa.io/get-pip.py](https://bootstrap.pypa.io/get-pip.py)

**版本选择**
* 3.8, 3.9 可能出现SSL错误，解决办法：换网络、换节点
* 3.10, 3.11, 3.12 正常

**步骤**
1. 为 `PowerShell` 配置 `HTTP` / `Socks` / `Tun` 代理
2. 
`PS C:\python-3.xx.xx-embed-amd64> `
`.\python.exe .\any-path\get-pip.py`
* 自动创建了 `Lib`、`Scripts` 目录
3. 编辑 `python-3.xx.xx-embed-amd64` 目录下的 `python3xx.pth` 或 `python3xx._pth`
4. 找到内容 `import site` 所在行，去掉前面的 `#`

* pip使用方法
  * 
    `PS C:\python-3.xx.xx-embed-amd64> `
    `.\python.exe -m pip`
  * 
    `PS C:\python-3.xx.xx-embed-amd64> `
    `.\Scripts\pip.exe`