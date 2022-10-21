{
  "date" : "2019-10-11",
  "keywords" :[ "class", ".class","什么是类文件","如何打开类文件", "扩展名", "文件", "类文件","类文件格式", ".class扩展名", "java 中的类文件" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"类 - Java 类文件格式",
  "description":"了解 Class 文件格式和可以创建和打开 Class 文件的 API。",
  "linktitle" : "CLASS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## 什么是类文件？

**Java 中的类文件** 是由 Java 虚拟机 (JVM) 实际执行的 [.java](/zh/programming/java/) 类的编译输出。类文件可以单独执行，也可以作为 [JAR](/zh/programming/jar/) 文件的一部分与其他包文件一起作为捆绑包执行。这些可以使用命令行界面中的 **`javac`** 命令创建。一些 Java IDE，如 [Eclipse](https://www.eclipse.org/downloads/packages/release/2020-06/r/eclipse-ide-java-developers) 和 NetBeans 提供从项目的 Java 创建 .class 输出文件文件。

## 类文件格式

Java 类文件由字节码组成，字节码是 JVM 运行的中间代码。类文件由 8 位字节流组成，多字节数据项始终以大端顺序存储。

### 类文件结构

类文件结构如下图所示。
```
ClassFile {
    u4             magic;
    u2             minor_version;
    u2             major_version;
    u2             constant_pool_count;
    cp_info        constant_pool[constant_pool_count-1];
    u2             access_flags;
    u2             this_class;
    u2             super_class;
    u2             interfaces_count;
    u2             interfaces[interfaces_count];
    u2             fields_count;
    field_info     fields[fields_count];
    u2             methods_count;
    method_info    methods[methods_count];
    u2             attributes_count;
    attribute_info attributes[attributes_count];
}
```
在哪里：

* u1 = 无符号单字节数量
* u2 = 无符号的两字节数量
* u4 = 无符号四字节数量

.class 文件结构的详细信息以及 Oracle [类文件格式](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html) 中的说明，可以参考供开发者参考。这些字段的摘要如下。

* `magic` - 魔法项提供标识类文件格式的幻数；它的值是 0xCAFEBABE。
* `minor_version`, `major_version` - 次要版本和主要版本项的值是这个类文件的次要和主要版本号。
* `constant_pool_count` - constant_pool_count 项的值等于 constant_pool 表中的条目数加一。如果 constant_pool 索引大于零且小于 constant_pool_count，则认为它是有效的，long 和 double 类型的常量除外。
* `constant_pool[]` - constant_pool 是一个结构表（第 4.4 节），表示在 ClassFile 结构及其子结构中引用的各种字符串常量、类和接口名称、字段名称和其他常量。每个 constant_pool 表条目的格式由其第一个“标记"字节指示。
* `access_flags` - access_flags 项的值是标志的掩码，用于表示对此类或接口的访问权限和属性。
* `this_class` - this_class 项的值必须是 constant_pool 表的有效索引。
* `super_class` - 对于一个类，super_class 项的值要么必须为零，要么必须是 constant_pool 表的有效索引。
* `interfaces_count` - interfaces_count 项的值给出了此类或接口类型的直接超接口的数量。
* `interfaces[]` - interfaces 数组中的每个值都必须是 constant_pool 表的有效索引。
* `fields_count` - fields_count 项的值给出了字段表中 field_info 结构的数量。
* `fields[]` - 字段表中的每个值都必须是一个 field_info 结构，给出此类或接口中字段的完整描述。
* `methods_count` - methods_count 项的值给出了方法表中 method_info 结构的数量。
* `methods[]` - 方法表中的每个值都必须是一个 method_info 结构，提供此类或接口中方法的完整描述。如果在 method_info 结构的 access_flags 项中没有设置 ACC_NATIVE 和 ACC_ABSTRACT 标志，则还提供实现该方法的 Java 虚拟机指令。
* `attributes_count` - attributes_count 项的值给出了此类的属性表中的属性数（第 4.7 节）。
* `attributes[]` - 属性表的每个值都必须是一个 attribute_info 结构。




## 参考

* [类文件格式](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html)

