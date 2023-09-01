{
  "date" : "2020-01-10",
  "keywords" :[ "otg 文件", "otg 文件格式", "什么是 otg 文件", "文件", "otg 示例", "otg 文件扩展名","扩展名", "格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTG - OpenDocument 绘图模板文件格式",
  "description":"了解 OTG 文件格式和可以创建和打开 OTG 文件的 API。",
  "linktitle" : "OTG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## 什么是一 .otg 文件？

OTG 文件是使用遵循 OASIS Office 应用程序 [1.0 规范](https://www.oasis-open.org/committees/download.php/12572/OpenDocument-v1.0-os.pdf) 的 OpenDocument 标准创建的绘图模板。它表示矢量图像的绘图元素的默认组织，可用于进一步增强文件的内容。 OTF 文件与任何其他基于 OpenDocument 格式的文件一样，它们基于 XML 格式来表示文档的内容。可以通过在任何文本或标准 XML 编辑器中打开 OTF 文件来查看它们。

## OTG 文件格式规范 ##

OTG 文件格式基于具有完善架构的 OpenDocument XML 格式。 OpenDocument 格式的每个组件的结构由具有关联属性的元素表示，并且对于所有文档类型（如文本文档、电子表格或绘图文件）都是通用的。 OTG，作为一个绘图模板，广泛利用了图形内容规范，包括：

* 图形应用程序的增强页面功能
* 绘制形状
* 帧
* 3D形状
*自定义形状
* 演示形状
*演示动画
* SMIL 演示动画
* 演示活动
*呈现文本字段
* 演示文稿内容

### 图形应用程序的增强页面功能###
####讲义大师####

讲义主元素是一个模板，用于为支持打印此类页面的应用程序自动生成讲义页面。
可能与 相关联的属性 `<style:handout-master>` 元素是：

|布局|属性|描述
---|---|---|
|演示文稿页面布局|演示文稿：演示文稿页面布局名称|链接到 `<style:presentation-page-layout>`  属性
|页面布局|`style:page-layout-name` |指定包含讲义母版页的大小、边框和方向的页面布局。
|页面样式|`draw:style-name`|通过指定绘图页面样式为讲义母版页指定附加格式属性。|
|标题声明| `presentation:use-header-name`|指定用于在讲义母版页上显示的所有标题字段的标题字段声明的名称。
|页脚声明|演示文稿:use-footer-name|指定用于在讲义母版页上显示的所有页脚字段的页脚字段声明的名称。
|日期和时间声明|use-date-time-name|指定用于在讲义母版页上显示的所有日期时间字段的日期时间字段声明的名称。

### 绘制形状###
OpenDocument 格式支持多种可用于任何类型文档的绘图形状。

|形状|相关属性|元素
---|---|---|
矩形 - `<draw:rect>` |位置、大小、样式、图层、Z-Index、ID、标题 ID、文本锚点、表格背景、绘制结束位置、圆角|标题、详细说明、事件侦听器、胶点、文本
线`<draw:line>` |样式、图层、Z-Index、ID、标题 ID 和转换、文本锚点、表格背景、绘制结束位置、起点、终点|标题、详细描述、事件侦听器、胶点、文本
折线`<draw:polyline> `|位置、大小、视图框、样式、图层、Z-Index、ID、标题 ID 和转换、文本锚点、表格背景、绘制结束位置、点|标题、详细说明、事件侦听器、粘合点、文本
多边形`<draw:polygon> `|位置、大小、视图框、样式、图层、Z-Index、ID、标题 ID 和转换、文本锚点、表格背景、绘制结束位置、点|标题、详细描述、事件侦听器、胶点、文本
|正多边形 `<draw:regular-polygon> `|位置、大小、样式、图层、Z-Index、ID、标题 ID 和转换、文本锚点、表格背景、绘制结束位置、凹面、角点、锐度|标题、详细说明、事件侦听器、胶点、文本
|帕特`<draw:path> `|位置、大小、视图框、样式、图层、Z-Index、ID、标题ID和转换、文本锚点、表格背景、绘制结束位置、路径数据|标题、详细说明、事件侦听器、粘合点、文本

### 帧###
绘图文档中的框架是包含文本框、图像或对象的矩形容器。框架支持附加功能，例如等高线、图像映射和超链接。一个帧可以包含一个对象以及一个图像，因此允许对一个对象进行多个再现。应用程序根据最佳支持呈现相应的元素。

框架可以包含：
* 文本框
* 以 OpenDocument 格式或特定于对象的二进制格式表示的对象
* 图片
* 小程序
* 插件
* 浮动框架

一个框架包含在一个文档中，如下所示。

```
<define name="draw-frame">
<element name="draw:frame">
<ref name="common-draw-shape-with-text-and-styles-attlist"/>
<ref name="common-draw-position-attlist"/>
<ref name="common-draw-rel-size-attlist"/>
<ref name="common-draw-caption-id-attlist"/>
<ref name="presentation-shape-attlist"/>
<ref name="draw-frame-attlist"/>
<zeroOrMore>
<choice>
<ref name="draw-text-box"/>
<ref name="draw-image"/>
<ref name="draw-object"/>
<ref name="draw-object-ole"/>
<ref name="draw-applet"/>
<ref name="draw-floating-frame"/><ref name="draw-plugin"/>
</choice>
</zeroOrMore>
<optional>
<ref name="office-event-listeners"/>
</optional>
<zeroOrMore>
<ref name="draw-glue-point"/>
</zeroOrMore>
<optional>
<ref name="draw-image-map"/>
</optional>
<optional>
<ref name="svg-title"/>
</optional>
<optional>
<ref name="svg-desc"/>
</optional>
<optional>
<choice>
<ref name="draw-contour-polygon"/><ref name="draw-contour-path"/>
</choice>
</optional>
</element>
</define>
```

## 参考 ＃＃
* [OASIS 办公应用开放文档格式](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [OpenDocument 格式 - 维基百科](https://en.wikipedia.org/wiki/OpenDocument)

