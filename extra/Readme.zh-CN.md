# RitsWiFi
优化立命馆的校内无线网络的体验

***只能在立命馆大学使用***

[English](https://github.com/fang2hou/RitsuWifi) | [日本語](https://github.com/fang2hou/RitsuWifi/blob/master/extra/Readme.ja-JP.md) | [简体中文](https://github.com/fang2hou/RitsuWifi/blob/master/extra/Readme.zh-CN.md)

## 预览
* <img src="https://cdn.rawgit.com/fang2hou/RitsuWiFi/master/extra/example.png" width="250px"/>

## 运行环境
**Python版本**: 2.6+ / 3.3+

RitsuWiFi 在 Python 2.7.0 & 3.7.0 进行编译和测试。

如果你在 macOS 的 Python 3.X 中运行 RitsWiFi，请使用 ```pip3``` 及 ```python3``` 来替换```pip``` 和 ```python```。

**额外库**: ```requests```, ```rumps```

## 如何使用
1. 克隆(Clone)本项目, 或者你也可以通过右上方的下载按钮来获取zip压缩包。
2. 安装包 ```rumps``` 及 ```requests```。对于大多数人来说，推荐通过pip来完成安装。

    ```shell
    pip install rumps
    pip install requests
    ```

3. 修改 ```RitsWiFi.py``` 来添加你的账号和密码
    - __举个例子__
    
    ```python
    # ---------------------------------------
    # Setting Area
    # ---------------------------------------
    wifiName = "Rits-Webauth"
    loginPagePath = "https://webauth.ritsumei.ac.jp"

    myUsername = "is1234rj"
    myPassword = "12345678"
    ```
4. 在**终端**或是其他你喜欢的终端程序中执行 ```python RitsWiFi.py```。

## 编译成独立App
如果你想要一个独立App形式的 RitsuWiFi，这里有一个解决方案。

- 创建 .app 文件时，会采用 logo.icns 来作为图标。
- 请你务必在确认 RitsuWiFi 能够正常工作后再将其编译成独立App。
- 请追加 ```-A``` 编译命令来启用别名模式

1. 安装包 ```py2app```。

    ```shell
    pip install py2app
    ```
2. 在编译之前, 建议执行 ```rm -rf dist build``` 来清理编译文件夹。
3. 在**终端**或是其他你喜欢的终端程序中执行 ```python setup.py py2app -A```。