{
  "date" : "2022-06-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WHL 文件格式 - Python Wheel 包文件",
  "description":"了解 WHL 文件格式和可以创建和打开 WHL 文件的 API。",
  "linktitle" : "WHL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-29"
}

## 什么是一 .whl 文件？

WHL (Wheel) 文件是以 Python 的轮子格式保存的分发包文件。它是 Python 发行版的标准格式安装，包含安装所需的所有文件和元数据。 WHL 文件还包含有关此 wheel 文件支持的 Python 版本和平台的信息。与 [MSI](/zh/executable/msi/) 安装文件类似，WHL 文件格式是一种即装即用格式，允许在不构建源代码分发的情况下运行安装包。

## WHL 文件格式

WHL 文件格式是 [ZIP](/zh/compression/zip/) (.zip) 存档，其中包含安装程序安装软件包所需的所有安装文件和元数据。这些 WHL 文件可以使用解压缩选项或标准解压缩软件应用程序（如 WinZIP 和 WinRAR）解压缩。

### WHL 文件名约定

WHL 文件按照以下约定命名。

```
{dist}-{version}(-{build})?-{python}-{abi}-{platform}.whl
```

WHL 文件名的示例如下。

```
cryptography-2.9.2-cp35-abi3-macosx_10_9_x86_64.whl
```

* `cryptography` 是包名。
* `2.9.2` 是密码学的软件包版本。版本是符合 PEP 440 的字符串，例如 2.9.2、3.4 或 3.9.0.a3。
* `cp35` 是 Python 标记，表示轮子需要的 Python 实现和版本。
* `abi3` 是 ABI 标签。 ABI 代表应用程序二进制接口。
* `macosx_10_9_x86_64` 是平台标签，正好是个拗口。

## 参考

* [什么是 Python Wheels，为什么要关心？](https://realpython.com/python-wheels/)
* [Python Wheel](https://pypi.org/project/wheel/)

