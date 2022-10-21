{
  "date" : "2021-12-09",
  "keywords" :["asa",".asa","文件格式","文件类型","什么是 .asa 文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASA - ASP 配置文件",
  "description" :"了解什么是 ASA 文件以及可以创建和打开 ASA 文件的 API。",
  "linktitle" : "ASA",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## 什么是一 .asa 文件？

ASA 文件是为 [ASP](/zh/web/asp/)/ASP.NET 项目创建的配置文件。它包含在应用程序的全局级别上可访问的变量、包含和函数的声明。项目中的所有页面都可以访问这些变量和函数，从而避免了重写这些的需求。一个这样的例子是 Global.asa 页面，它存储在根目录中，可供其他 ASP 网站页面访问。 Global.asa 文件是可选的，但如果使用，每个应用程序只能有一个 Global.asa 文件。

## ASA 文件格式 - 更多信息

ASA 文件是具有以下信息的纯文本文件。

* 应用事件
* 会话事件
* \<object>声明
* 类型库声明
* #include 指令

## ASA 文件示例

Global.asa 文件可能看起来像这样。

```
<script language="vbscript" runat="server">

sub Application_OnStart
'some code
end sub

sub Application_OnEnd
'some code
end sub

sub Session_OnStart
'some code
end sub

sub Session_OnEnd
'some code
end sub

</script>
```

## 参考

* [ASP Global.asa 文件 - w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)

