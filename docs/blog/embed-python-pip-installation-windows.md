---
date: 2024-03-26
categories: programming
---
# 嵌入式 Python Windows 版 pip 安装教程 (python-embed)

本文与嵌入式硬件开发无关

## 下载

- `python-3.xx.xx-embed-amd64.zip` 来自 [python.org](https://www.python.org/)
- `get-pip.py` 来自 [https://bootstrap.pypa.io/get-pip.py](https://bootstrap.pypa.io/get-pip.py)

## 版本选择

- 3.8, 3.9 可能出现 SSL 错误，解决办法：换网络、换节点
- 3.10, 3.11, 3.12 正常

## 安装步骤

1. **为 `PowerShell` 配置 `HTTP` / `Socks` / `Tun` 代理**

2. **运行 get-pip.py**
   ```powershell
   PS C:\python-3.xx.xx-embed-amd64>
   .\python.exe .\any-path\get-pip.py
   ```
   - 自动创建了 `Lib`、`Scripts` 目录

3. **编辑 `python3xx.pth` 或 `python3xx._pth` 文件**
   - 路径：`python-3.xx.xx-embed-amd64` 目录下

4. **找到 `import site` 所在行，去掉前面的 `#`**

## pip 使用方法

1. **使用 Python 模块方式**
   ```powershell
   PS C:\python-3.xx.xx-embed-amd64>
   .\python.exe -m pip
   ```

2. **使用可执行文件方式**
   ```powershell
   PS C:\python-3.xx.xx-embed-amd64>
   .\Scripts\pip.exe
   ```
