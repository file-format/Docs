{
  "date" : "2022-02-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MP 文件 - LaTeX MetaPost 文件",
  "description":"了解 MP 文件格式和可以创建和打开 MP 文件的 API。",
  "linktitle" : "MP",
  "menu" : {
    "docs" : {
      "identifier":"image-mp",
      "parent" : "image"
}
},
  "lastmod" : "2022-02-23"
}

## 什么是 .mp 文件？

MP 文件是由 MetaPost 编程语言生成的用于创建图片的矢量图像文件。使用 MP 文件格式创建的矢量图像保存为 [EPS](/zh/image/eps/)（封装 PostScript）文件。此外，MetaPost 与 TeX 和 Metafont 框架一起分发，并且可以从这些应用程序使用的 TEX 和 LTX 文件中生成 MP 文件。 MP 文件包含用于渲染输出 EPS 文件的绘图语句和数学算法绘图。 PDFTex 引擎可以使用创建的 EPS 直接生成 [PDF](/zh/pdf/) 文件。

## MP 文件格式

MP 文件作为二进制文件保存到光盘，并在导出为输出矢量图像文件格式时生成 EPS 输出。使用 MetaPost 创建的绘图以格式化的形式包含在使用 LaTex 创建的技术文档和期刊出版物中。

### MetaPost MP 文件示例

以下是引用自 [Berkeley Educational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost) 的示例，其中包含一个箭头和位于中间上方的字母“A"箭。

```
outputtemplate:="%j%c.mps";
beginfig(1);

z1=(0,0);
z2=(10mm,10mm);

drawarrow(z1--z2);
label.ulft(btex $A$ etex, .5[z1,z2]);

endfig;

bye
```
## 参考 ＃＃

* [维基百科的 MetaPost](https://en.wikipedia.org/wiki/MetaPost)
* [伯克利教育维基的乳胶样本 Metapost](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost)

