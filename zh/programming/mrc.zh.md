{
  "date" : "2021-09-14", 
  "keywords" :["mrc","文件","扩展","文件格式","mrc 实现","编程指南","mrc 示例","mIRC","mIRC 脚本语言","INI 文件"," mSL 脚本语言","mIRC 语言","mIRC 脚本","脚本语言"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MRC - mIRC 脚本语言文件",
  "description":"了解 MRC 文件格式和可以创建和打开 MRC 文件的 API。",
  "linktitle" : "MRC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-14"
}

## 什么是一 .mrc 文件？

mIRC 是一种脚本语言，作为 IRC 客户端（Internet 中继聊天）嵌入在 Windows 操作系统中。它为个人和频道使用提供了防止垃圾邮件的功能。为了提供更好的用户兼容性体验，这种 mIRC 脚本语言允许创建对话窗口。包含脚本的文件，主要是纯文本格式，以 MRC 的扩展名或 [INI](/zh/system/ini/) 的文件存储。这种语言的函数称为命令和标识符（当它们返回值时）。

mIRC 语言提供一次加载多个脚本文件。另一方面，一个文件在同时加载时可能会导致另一个文件不再使用。命令被保存，它们可以自动存在于 IRC 中。此语言中使用的命令和别名不包含任何字符的优先级。

mIRC 被广泛用于使机器人自动管理频道，但它也可以通过 mSL 脚本语言进行修改。它可以引入许多新功能，如宏、音乐播放能力、小宏和功能、基础游戏或操作小应用程序。


## 历史简介 ＃＃

这种脚本语言由 Khaled Adam Bey 于 1995 年首次开发。脚本语言的设计也是由 Khalid 创建的。这种语言的目标是事件驱动编程。最初，用于这种编程语言文件的文件扩展名是 .mrc 和 .ini。此外，它是在专有软件的许可下开发的。

## 技术规格##

一些函数是通过这种 mIRC 语言编写的自定义脚本，称为别名。当这些别名返回值时，它们被称为自定义标识符。此 mIRC 语言中包含的所有变量都是动态类型的。 Sigils 由 mIRC 脚本使用。这种脚本语言的另一个特点是弹出窗口。用户只需选择它们即可调用弹出窗口。遥控器被指定给某些事件。当相关事件发生时调用遥控器。

空格分隔的标记用于打破该语言的每一行代码。还有一些其他流行的扩展用于 mIRC 文件，例如 MDX（mIRC 对话扩展）和 DCX（对话控制扩展）。这两者都是对话扩展，并且相对更受欢迎。语言结构由该脚本语言的命名法引用。 mIRC 语言涉及脚本语言的不同方面，例如局部和全局变量、二进制变量、哈希表和文件处理。


## MRC 文件格式示例 ##

```

;Defines the alias 'hello' in the remote script

;Note: if this is placed in an alias script,
;the 'alias' part must be removed (result: hello {)
;Usage: /hello

alias hello {

  ;Displays(/zh/echo) 'Hello World!' into the active window(-a)
  echo -a Hello World!

}

```

```
;Placed in a remote script

;When a user types Hello! in a channel,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:#:{ msg $chan Hello, $nick $+ ! }

;When a user types Hello! in a private message,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:?: { msg $nick Hello, $nick $+ ! }

;Here is a script which automatically gives voice to a user
;who joins a particular channel (The Bot or user should have HOP)

on *:JOIN:#?: { mode $chan +v $nick }

;A bad word script

on *:Text:die*:#: { .mode $chan +b $nick | kick $chan $nick Dont say that again }

```

## 参考 ＃＃

* [MIRC - 维基百科](https://en.wikipedia.org/wiki/MIRC_scripting_language)



