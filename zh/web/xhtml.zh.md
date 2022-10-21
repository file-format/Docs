{
  "date" : "2019-10-11",
  "keywords" :["xhtml", "文件", "扩展名", "文件格式", "文件扩展名", "可扩展的 html"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XHTML - 可扩展的超文本标记语言文件格式",
  "description":"了解什么是 XHTML 文件格式以及可以创建和打开 XHTML 文件的 API。",
  "linktitle" : "XHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是 XHTML 文件？

XHTML 是一种基于文本的文件格式，在 XML 中带有标记，使用 HTML 4.0 的重新表述。这些文件非常适合在 Web 浏览器中打开或查看。 XHTML 被设计成更结构化、更少脚本、更通用；使用 XML 的所有现有设施，并且更加独立于设备。 XHTML 提供了一组通常有价值的元素和属性，以及与样式表相结合的扩展选项。这些属性是从元数据属性集合中使用的。 XHTML 通过将所有 **[HTML](/zh/web/html/)** 表示元素从属于样式表来提供灵活性和可访问性。样式表比这些表示元素更通用。万维网联盟 (W3C) 正在动态开发 HTML 4.01、HTML5 和 XHTML 的规范。

## XHTML 文件格式简史

XHTML 的历史始于 1998 年 12 月万维网联盟发布的一份草稿文档。本文档引用了“Reformulating HTML in XML"，一个称为 XHTML 1.0 的规范。这个新规范使用现有元素或属性在 XML 中重新定义了 HTML。 1999 年 5 月，W3 Consortium 宣布 HTML 4.0 已被重新形成为 XML 应用程序。即XHTML。 2000 年 1 月 26 日，第一个定义 XHTML 1.0 的规范由 W3C 发布。 2001 年 5 月 31 日，W3C 宣布 XHTML 作为一种独立语言，并开始着手开发 HTML 5.0。然而，在 2005 年，一个工作组 (WHATWG) 成立，旨在改进独立于 XHTML 的普通 HTML。 WHATWG 最终开始着手开发与 XHTML 2 并行的 HTML5。

## XHTML 文件格式

XHTML 是一种格式，它是模仿、分类和扩展 HTML 4 的不同文档类型和模块的集合。XHTML 中的文件是基于 XML 的，旨在与基于 XML 的用户代理一起工作。 XHTML 文件符合 XML。标准 XML 工具用于查看、编辑和验证 XHTML 文件。 HTML 文档对象模型或 XML 文档对象模型 [DOM] 依赖的应用程序可以通过 XHTML 文档进行操作。今天选择 XHTML，内容开发人员可以享受 XML 的所有相关好处，而不必担心其内容的向前或向后兼容性。

一组相关的元素在 XHTML 中构建了一个模块。表格或表格模块可以包含可以在网页上显示的各种表格或表格元素。模块化旨在将 HTML 元素隔离为多个链接元素的集合。这样内容开发者就可以利用针对不同类型设备的模块选择。此外，模块允许用户代理选择元素而不会失去与 XHTML 标准的一致性。 XHTML 的解析要求与 XML 相同，而 HTML 自己实践。

### 文档一致性

XHTML2 提供符合 XHTML 1.0 文档的规范，该文档使用 XML 和 XHTML 1.0 中的名称空间元素和属性。文档一致性有两种类型。

严格符合的文档是基于 XML 的，只需要本规范中定义的强制性服务。 XHTML 文件需要满足以下条件：

* 文件必须符合 DTD 和附录 B 中定义的约束。
* 文件的基本元素必须是 html。
* 文件的基本元素必须包含 XHTML 命名空间的声明，并应定义为：

```
http://www.w3.org/1999/xhtml.
```

* 基本元素可以写成：

```
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
```

在基本元素之前，必须声明一个 DOCTYPE，其公共标识符必须引用三个文档类型定义 (DTD) 之一。可以修改系统标识符以符合当前系统约定。

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd">
```

在 XML 文档中，不需要在所有文档中都指定 XML 声明；然而，内容开发人员被诱惑在他们所有的 XHTML 文档中使用 XML 声明。当文档的字符编码不同于 UTF-8 /16 或管理协议未指定编码时，这些声明是强制性的。下面的 XHTML 文档示例定义了 XML 声明

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

符合标准的用户代理必须满足以下规则：

* XHTML 文档的解析和评估由确保其与 XML 1.0 建议一致的用户代理完成。
* 在验证用户代理的情况下，它必须根据 XML 检查其引用的 DTD 的文档有效性。当 XHTML 文件被用户代理处理为通用 XML 时，类型 ID 的特征将被确认为片段标识符。

如果用户代理遇到无法识别的元素，以下是它必须完成的强制性标准

* 处理那个未知元素的内容
* 忽略属性及其值
* 使用默认提供的属性值。

当用户代理遇到一个实体引用声明之前没有被处理时，它应该被处理为字符（以“&"符号开始，以分号结束）。在内容处理期间，可由用户代理预测但不可渲染的字符或字符实体引用可以使用产生相似含义的任何替代渲染。在这种情况下，文档的显示方式必须让用户清楚地知道渲染过程不正常。为了处理空白，用户代理需要从 CSS 字符 [CSS2] 中查找定义。

## XHTML 向后兼容性

如果遵循适当的规则，XHTML 1. 文档的向后兼容性非常熟悉 HTML 4 用户代理。 XHTML 1.1 完全兼容，除了 ruby 注释，尽管它们通常被 HTML 4 浏览器忽略。 XHTML 2.0 的兼容性相对较差，但是通过使用脚本在一定程度上解决了这个问题。

## 参考

* [XHTML 的历史：从 1990 年代到今天](https://www.brighthub.com/internet/web-development/articles/109224.aspx)

