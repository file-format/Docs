
{
  "date" : "2021-12-14",
  "keywords": [ ".abc file", "extension", "format","ActionScript Byte Code File", "how to open .abc file","abc file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABC - ActionScript 字节码文件",
  "description":"通过示例和可以创建和打开 ABC 文件的 API 了解什么是 ABC 文件格式。",
  "linktitle" : "ABC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-14"
}

## 什么是一 .abc 文件？

扩展名为 .abc 的文件是 Flash 编译器在编译 ActionScript 脚本文件后创建的 ActionScript 字节代码文件。 ABC 文件中包含的字节码由 ActionScript 虚拟机（AVM 和 AVM2）执行。字节码由常量数据、来自 AVM2 指令集的指令和各种元数据组成。当 ABC 文件加载到 AVM 或 AVM2 中时，它会进行验证。如果它不符合 AVM2 概述，则会被拒绝。 ABC 文件可以在很久以前停产的 Adobe Flash Player 中打开。

## ABC 文件格式 - 更多信息

ABC 文件以 AVM 或 AVM2 虚拟机可读的二进制文件格式保存到磁盘。它的内部文件结构表示可执行代码块及其所有常量数据、类型描述符、代码和元数据。

## ABC 文件结构

ABC 文件结构如下图所示。

```
abcFile  
{
           u16        minor_version                
           u16        major_version                
           cpool_info        constant_pool                
           u30        method_count                
           method_info        method[method_count]                
           u30        metadata_count                
           metadata_info        metadata[metadata_count]                
           u30        class_count                
           instance_info        instance[class_count]                
           class_info        class[class_count]                
           u30        script_count                
           script_info        script[script_count]               
           u30        method_body_count                
           method_body_info        method_body[method_body_count]        
}
```

### ABC 文件字段

|字段名称|描述|
---|---|
|minor_version,major_version|major_version 和minor_version 的值是abcFile 格式的主要和次要版本号。|
|constant_pool|constant_pool 是一个可变长度结构，由整数、双精度、字符串、命名空间、命名空间集和多名称组成。|
|method_count, method|method_count 的值是方法数组中的条目数。方法数组中的每个条目都是一个可变长度的 method_info 结构。|
|metadata_count, metadata|metadata_count 的值是元数据数组中的条目数。每个元数据条目都是一个 metadata_info 结构，它将名称映射到一组字符串值。 |
|class_count, instance, class|class_count 的值是实例和类数组中的条目数。 |
|script_count, script|script_count 的值是脚本数组中的条目数。每个脚本条目都是一个 script_info 结构，它定义了该文件中单个脚本的特征。 |
|method_body_count, method_body|method_body_count 的值是method_body 数组中的条目数。每个 method_bodyentry 都由一个可变长度的 method_body_info 结构组成，该结构包含单个方法或函数的指令。

## 参考

* [Robust ABC (ActionScript Bytecode) [Dis-]Assembler - Github](https://github.com/CyberShadow/RABCDAsm)

