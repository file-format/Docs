{
  "date" : "2019-10-11",
  "keywords" :[ "yaml", ".yaml","什么是 yaml 文件","如何打开 yaml 文件","扩展名","文件","yaml 文件","yaml 文件格式",".yaml 扩展名" , "yaml vs json" ,"YAML 文件示例", "docker yaml 文件示例"],
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "description" :" 了解 YAML 文件格式和可以创建和打开 YAML 文件的 API。",
  "title" :"YAML 文件格式",
  "linktitle" : "YAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-05"
}

## 什么是一 .yaml 文件？ ##

**YAML 文件** 由一种语言 YAML（YAML Ain't Markup Language）组成，它是一种基于 Unicode 的数据序列化语言；用于配置文件、互联网消息传递、对象持久性等。YAML 对其文件使用 .yaml 扩展名。它的语法独立于特定的编程语言。基本上，YAML 是为人类交互而设计的，并且可以很好地与现代编程语言一起使用。对序列化任意原生数据结构的支持增加了 YAML 文件的可读性，但它使解析和文件生成过程稍微复杂了一点。

## 历史简介 ＃＃

YAML 于 2001 年首次提出，由 Clark Evans、Ingy döt Net 和 Oren Ben-Kiki 开发。 YAML 最初的意思是“另一种标记语言"，以表明其作为标记语言的目的。它后来被重新命名为“YAML Aint Markup Language"，以表明其面向数据的目的。


## YAML 文件格式##

YAML 文件由以下数据类型组成

- **标量**：标量是字符串、整数、布尔值等值。
- **序列**：序列是每个项目以连字符 (-) 开头的列表。列表也可以嵌套。
- **Mappings**：映射提供了列出具有值的键的能力。

＃＃＃ 句法 ＃＃＃

- **空白**：空白缩进用于表示嵌套和整体结构。

```yaml
姓名：约翰·史密斯
接触：
家：1012355532
办公室：5002586256
地址：
街道： |
123龙卷风巷
套房 16
城市： 东森特维尔
州：堪萨斯州
```

- **评论**：评论以“#"符号开头。

```yaml
# 这是一个 YAML 注释
```

- **Lists**：连字符 (-) 用于指示列表成员，每个成员位于单独的行中。列表成员也可以用方括号 ([...]) 括起来，成员之间用逗号 (,) 分隔。

```yaml
  - A
  - B
  - C
```

```yaml
[A、B、C]
```

- **关联数组**：关联数组被大括号 ({...}) 包围。键和值用冒号(:) 分隔，每对用逗号(,) 分隔。

```yaml
  {name: John Smith, age: 20}
```

- **字符串**：可以使用或不使用双引号 (") 或单引号 (') 来编写字符串。

```yaml
示例字符串
“示例字符串"
'示例字符串'
```

- **标量块内容**：标量内容可以使用以下块表示法编写：
  - **|**: All live breaks are significant.
  - **>**: Each line break is folded to space. It removes the leading whitespace for each line.

```yaml
数据：|
YAML
（YAML 不是标记语言）
是一种数据序列化语言
```

```yaml
数据： ？
YAML（YAML 不是标记语言）
是一种数据序列化语言
```

- **多个文档**：多个文档在单个流中由三个连字符 (---) 分隔。连字符表示文档的开始。连字符也用于将指令与文档内容分开。文档的结尾用三个点 (...) 表示。

```yaml
  ---
文件 1
  ---
文件 2
...
```

- **Type**：要指定值的类型，使用双感叹号 (!!)。

```yaml
答：!!浮点数 123
乙：!!str 123
```

- **标签**：要为注释分配标签，使用与号 (&) 并引用该节点，使用星号 (*)。

```yaml
姓名：约翰·史密斯
收单方：&id01
街道： |
123龙卷风巷
套房 16
城市： 东森特维尔
州：堪萨斯州

收货方：*id01
```

- **指令**：YAML 文档可以在流中以指令开头。指令以百分号 (%) 开头，后跟名称，然后是由空格分隔的参数。

```yaml
%YAML 1.2
  ---
文件内容
```
## YAML 文件示例
在这里，您可以看到下面的 **docker yaml 文件示例**：

```
topology:
database_node_name: docker_controller
docker_controller_node_name: docker_controller
self_service_portal_node_name: docker_controller
kvm_compute_node_names: kvm_compute1
docker_compute_node_names: docker_compute1
```

## YAML 与 JSON
基本上，JSON 和 YAML 都是为了提供人类可读的数据交换格式而开发的。 YAML 被实现为 JSON 格式的超集。这意味着我们可以使用 YAML 解析器解析 JSON。虽然这个理论的实际实施有点棘手。因此，下面给出 YAML 和 JSON 之间的一些基本区别：

|YAML| JSON|
---|---|
|解析序列化数据的过程复杂耗时 |使用更简单的设计快速轻松地解析JSON序列化数据|
|更少的社区支持|更大的社区支持和人气|
|支持评论|不支持评论|
|使用其他数据对象的引用的能力|不可能用对象引用序列化复杂结构|
|使用双空格字符表示层次结构。 | 不允许使用制表符|对象和数组用大括号和方括号表示。|
|字符串引号是可选的，但它支持单引号和双引号。|字符串必须用双引号。|
|根节点可以是任何有效的数据类型|根节点必须是数组或对象。|


## 参考 ＃＃

- [YAML - 维基百科](https://en.wikipedia.org/wiki/YAML)
- [YAML](https://yaml.org/spec/1.2/spec.html)

