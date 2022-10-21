{
  "date" : "2022-02-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WSDL 文件格式 - Web 服务描述语言文件",
  "description":"了解什么是 WSDL 文件以及可以创建和打开 WSDL 文件的 API。",
  "linktitle" : "WSDL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-02-03"
}

## 什么是 .WSDL 文件？

WSDL 文件是用 XML 语言编写的用于描述 Web 服务的 Web 服务描述语言文件。它包含有关以普遍接受的格式连接到外部世界的端点或接口的信息。 [WSDL 文件格式规范](https://www.w3.org/TR/2007/REC-wsdl20-20070626/)（由 W3C.org 维护）定义了发布数据馈送以交换数据的术语，以便拥有通过端口和端点进行远程应用程序访问。

## WSDL 文件格式 - 更多信息

WSDL 文件保存为人类可读的 XML 文件，可以在任何文本编辑器中打开以查看内容。

## WSDL 服务描述

WSDL 2.0 文件格式规范将 WSDL 服务描述为包括两个阶段：

- 抽象阶段
- 混凝土舞台

描述和独立关注点设计的可重用性由 Web 服务管理。这是使用几种不同类型的元素来实现的，包括类型（数据类型定义）、消息（通信的数据）、操作（动作）和服务使用的协议。这些都在抽象级别进行管理。传输和有线格式详细信息的绑定由绑定指定，它将端点组合在一起以实现公共接口。

### 哪些技术可用于与 WSDL 服务交互？

有几种不同的技术可用于连接 WSDL 服务，包括 ASP.NET、C/C++ 和 Java 应用程序。

## WSDL 示例

```
<message name="getTermRequest">
  <part name="term" type="xs:string"/>
</message>

<message name="getTermResponse">
  <part name="value" type="xs:string"/>
</message>

<portType name="glossaryTerms">
  <operation name="getTerm">
    <input message="getTermRequest"/>
    <output message="getTermResponse"/>
  </operation>
</portType>
```

在本例中，portType“glossaryTerms"定义了一种称为“setTerm"的单向操作。

## 参考

* [WSDL XML](https://www.w3schools.com/xml/xml_wsdl.asp)
* [WSDL 文件格式规范](https://www.w3.org/TR/2007/REC-wsdl20-20070626/)

