{
  "date" : "2021-07-13",
  "keywords" :["CFM","扩展名","文件","格式","系统","冷融合标记语言","语言","CFM 网页","CFML 引擎","CFML"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFM - 冷融合标记",
  "description":"了解 CFM 文件格式和可创建和打开 CFM 文件的 API。",
  "linktitle" : "CFM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## 什么是一 .cfm 文件？ ##

**Cold Fusion Markup Language** 中使用的网页和文件包含 CFM 的扩展名，被命名为 CFM 网页。这种 Web 开发脚本语言在 Google App Engine、.NET 框架和 JVM 上运行。它可以包含一种编程语言或该语言的代码。当用户访问它的任何页面时，ColdFusion 的网络服务器会执行它。 CFScript（即接近 JavaScript）或标签可用于编写 CFML。 CFML 可用于生成除 [HTML](/zh/web/html/) 之外的其他语言，例如 [CSS](/zh/web/css/)、[JavaScript](/zh/web/js/)、[XML](/zh/web/ xml/) 等。

这种语言和它支持的标签的使用主要是在开发动态Web应用程序中，如果在离线使用应用程序开发平台时出现任何错误，可以直接在浏览器中在线运行文件。
 

CFML 的工作方式是为 CFML 引擎提供特定的服务器文件扩展名（.cfc、.cfm）以进行处理。如果引擎基于 Java，则使用 Java servlet 实现。 CFML 引擎只处理函数和标签，它会将 CFML 标签之外的函数和文本原封不动地返回给 Web 服务器。


## 历史简介 ＃＃

1995 年，它首先由一家名为 Allaire 的公司创建。 2005 年 Adobe 收购了它，现在它仍然为开发 ColdFusion 提供服务。多年来，它得到了许多人和公司的开发和升级。 2012 年，一个名为 OpenCFML 的基金会成立。后来，在 2015 年，前 Railo 提供了他的服务来提高 CFM 的性能并减少资源以获得更好的功能。它的最新更新于 2020 年推出，并宣布将持续到 2028 年。

## CFM 文件格式 ##

CFM 文件和网页的代码主要包含 HTML 等标签，但略有不同。这些文件负责执行 ColdFusion 脚本允许运行的各种操作。
* 这些文件可以使用任何操作系统的浏览器在 Windows 和 macOS 上直接访问和运行。
* Adobe ColdFusion 提供在PC 上开发网页和动态应用程序的平台。
* 任何文本编辑器（如记事本）或操作系统中的任何其他文本编辑器都可用于打开这些文件，因为这些文件是基于文本的。
* 当任何 CFM 文件在文本编辑器中打开时，它会显示由标签和脚本组成的代码，除非他是 Web 开发人员，否则无法理解。

## CFM 使用示例 ##

下面显示了一个简单的使用示例 CFM 文件。

### CFM 文档###

```html
<!--- temperature.cfc --->
<cfcomponent>
  <cffunction name="FtoC" access="public" returntype="numeric">
    <cfargument name="fahrenheit" required="yes" type="numeric" />
    <cfset answer= (fahrenheit - 32)*100/180 />
    <cfreturn answer />
  </cffunction>
</cfcomponent>
<!--- test.cfm --->
<cfset fDegrees = 212 />
<cfinvoke component="temperature" method="FtoC" returnvariable="result">
  <cfinvokeargument name="fahrenheit" value="#fDegrees#" />
</cfinvoke>
<cfoutput>#fDegrees#&deg;F = #result#&deg;C</cfoutput> <br />
```

## 参考 ＃＃

- [CFM - 维基百科](https://en.wikipedia.org/wiki/ColdFusion_Markup_Language)

