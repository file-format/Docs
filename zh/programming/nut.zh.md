{
  "date" : "2021-09-23", 
  "keywords" :["NUT","文件","扩展名","文件格式","NUT 程序语言","编程指南","NUT 示例","NUT 文件格式","松鼠语言",".nut 扩展名文件", "NUT 文件" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NUT - 松鼠语言文件",
  "description":"了解 NUT 文件格式和可以创建和打开 NUT 文件的 API。",
  "linktitle" : "NUT",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-23"
}

## 什么是一 .NUT 文件？

NUT 指的是 NUT Open Container Format 文件。这种 NUT 文件格式属于被称为 Squirrel 的编程语言。它是一种面向对象的高级命令式编程语言，主要用于嵌入式系统和视频游戏。

松鼠语言被认为是一种轻量级的脚本语言，可以根据大小和带宽轻松调整。它涉及自动引用计数和内存中垃圾管理的优势。

squirrel 语言的语法因为类似于 C 并且涉及脚本语言的特性而吸引了开发人员。但是，与其他更流行的编程语言相比，它的优势要少得多。



## 历史简介 ＃＃

它是由 Alberto Demichelis 于 2003 年设计的。然而，该语言的稳定版本于 2016 年发布。它是在 zlib/libpng 的许可下设计的。 2010 年，许可证更改并转移到麻省理工学院。这种语言被认为是 [LUA](/zh/programming/lua/)（编程语言）的灵感版本。 Alberto 设计的网站上有一个关于前一种语言的建议列表，以使其更有利。


## 技术规格##

松鼠语言的特点和规格是多方面的。它提供了动态类型、委托属性、类和接口的多种用途的便利。这种语言的语法与 C 语言的语法有相似之处。 Enduro/X（集群应用服务器）等应用程序使用这种语言。由于 Squirrel 也用于视频游戏，其中一些是 OpenTTD、GTA IV 等。

该语言的稳定版本是 3.0.7。一个名为 MirthKit 的工具包使用 Squirrel 编程语言为二维游戏提供开源和跨平台。这种语言的本质是动态的，大部分特性类似于[Python](/zh/programming/py/)、LUA等。它还涉及基于寄存器的VM的实现。与 LUA 相比，Squirrel 的性能要慢一些。

还有另一种“.nut"扩展文件类型，这就是为什么您应该查看文件大小以找出您拥有哪个 NUT 文件的原因。 Squirrel script NUT 文件大多小于 1 MB，而视频 NUT 文件通常大于 1 MB。


## NUT 文件格式示例 ##

```
function factorial(x)
  {
    if (x == 0) {
      return 1;
}
    else {
      return x * factorial(x-1);
}
  }
```

```

class BaseVector {
    constructor(...)
    {
      if(vargv.len() >= 3) {
        x = vargv[0];
        y = vargv[1];
        z = vargv[2];
  }
}
    x = 0;
    y = 0;
    z = 0;
  }

  class Vector3 extends BaseVector {
    function _add(other)
    {
      if(other instanceof ::Vector3)
        return ::Vector3(x+other.x,y+other.y,z+other.z);
      else
        throw "wrong parameter";
}
    function Print()
    {
      ::print(x+","+y+","+z+"\n");
}
  }

  local v0 = Vector3(1,2,3)
  local v1 = Vector3(11,12,13)
  local v2 = v0 + v1;
  v2.Print();

```

## 参考 ＃＃

* [NUT - 维基百科提供](https://en.wikipedia.org/wiki/Squirrel_(programming_language))



