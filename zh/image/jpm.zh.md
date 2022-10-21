{
  "date" : "2019-11-25",
  "keywords" :["jpm 文件","jpm 文件格式","什么是 jpm 文件","文件","jpm 示例","jpm 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPM - JPEG 2000 复合文件格式",
  "description":"了解 JPM 文件格式和可以创建和打开 JPM 文件的 API。",
  "linktitle" : "JPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-08"
}

## 什么是一 .jpm 文件？

JPM 是指用于文档成像的 JPEG 2000 图像编码系统第 6 部分。它基于混合光栅内容标准 (ISO/IEC 16485)，包含使用 JPEG 2000 和其他编码的分层静止图像。除了自己的规范之外，JPM 文件格式还继承了其父文件格式的特征，即 [jp2](/zh/image/jp2/) 文件格式。

## JPM 文件格式

JPM 文件格式由 [ISO/IEC 15444-6:2003](http://www.iso.org/iso/home/store/catalogue_ics/catalogue_detail_ics.htm?csnumber=61124) 定义——JPEG 2000 图像编码系统——第 6 部分：复合图像文件格式。复合图像可能包含扫描图像、合成图像或两者兼有，需要混合使用连续色调和双级压缩方法。 JPM 文件格式定义了一个合成模型，该模型描述了使用 ITU-T T.44 | 中定义的多层混合光栅内容 (MRC) 成像模型组合多个图像以生成复合图像的方法。 ISO/IEC 16485。

### JPM 规范
JPM 文件格式标准将其指定为二进制容器来表示复合图像，通过该复合图像可以将多个图像组合成单个图像。它设置了在布局对象、页面和页面集合的层次结构中对多个图像进行分组的机制，以存储 JPEG 2000 和其他压缩图像数据格式。该格式包括合并元数据的机制（在数字图书馆项目中通常称为结构元数据）。

## 参考

* [ITU-T 建议书。 T.805](http://www.itu.int/rec/T-REC-T.805/en)
* [ISO/IEC 15444-6:2013](http://www.iso.org/iso/home/store/catalogue_ics/catalogue_detail_ics.htm?csnumber=61124)
* [维基百科：JPEG 2000](http://en.wikipedia.org/wiki/JPEG_2000)

