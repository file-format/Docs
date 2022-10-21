{
  "date" : "2020-03-16",
  "keywords" :["PAT 文件","格式","CAD"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 PAT 文件格式和可以创建和打开 PAT 文件的 API。",
  "title" :"PAT 文件格式",
  "linktitle" : "PAT",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-10-25"
}

## 什么是一 .pat 文件？

扩展名为 .pat 的文件是 AutoCAD 软件使用的 CAD 文件。可以打开 PAT 文件的应用程序使用存储在这些文件中的填充图案获取有关区域纹理/填充的信息。包含的图案为绘制的对象提供了有关材料外观的信息。 PAT 文件可以在 Autodesk AutoCAD、CorelDRAW Graphics Suite 和 Ketron Software 等应用程序中打开。 PAT 文件可以转换为不同的图像格式，例如 JPG、PNG、BMP 等。

## PAT 文件格式

PAT 文件以纯文本格式编写，可以在任何文本编辑器中打开。这些文件中的填充图案是基于矢量的，并遵循 AutoCAD 文档中概述的语法。

所有图案都从点 0,0 开始，计算出图案以覆盖阴影边界。

### 模式定义

所有模式定义都包含以下字段：
* 前导 '\*'
* 名称 - 名称不能有空格、标点符号、括号或斜线。
* 说明

填充图案的标准格式是 `<\*><name> <，描述>`。名称和描述以逗号分隔，描述不能超过八十个字符的行长。填充图案是在此信息之后定义的。

### 填充图案示例
以下是方形图案的示例
```
* square, a square pattern
0,     0,0,   0,1,   1,-1
90,   0,1,   0,1,   1,-1
```
显示平行四边形图案的另一个示例如下。

```
*pgram, parallelogram pattern
0,     0,0,    1,1,                     1,-1
45,   0,0,    0,1.4142,   1.4142,-1.4142
45,   0,1,    0,1.4142,   1.4142,-1.4142
```
## 参考 ＃＃

* [Autodesk 的哈希模式](https://knowledge.autodesk.com/support/autocad-lt/learn-explore/caas/CloudHelp/cloudhelp/2018/ENU/AutoCAD-LT/files/GUID-A6F2E6FF-1717- 44B6-A476-0CA817ADD77E-htm.html)

