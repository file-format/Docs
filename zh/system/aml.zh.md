{
  "date" : "2022-04-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AML 文件 - ACPI 机器语言文件",
  "description":"了解 ACPI AML 文件格式和可以创建和打开 AML 文件的 API。",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier" : "system-aml",
      "parent" : "system"
}
},
  "lastmod" : "2022-04-12"
}

## 什么是一 .AML 文件？

AML 文件是使用高级配置和电源接口 (ACPI) 语言创建的系统文件，用于配置硬件属性。它包含与机器无关的字节码，用于配置硬件，即使是简单的操作，例如关闭计算机。 AML 文件可能包含说明，具体取决于将其安装在机器上的目的。 ACPI 标准的实施使您可以增强电源管理功能和用于配置主板设备（如 P55 主板）的强大接口。

## ACPI AML 文件格式

AML 文件以二进制文件的形式保存到磁盘，内容以字节码编写。 ACPI 标准的文件格式规范可在 [uefi](https://uefi.org/) 上找到。该语言旨在提供稳定性和向后兼容性，需要更少的重写或重新构建应用程序堆栈。

## AML 文件格式规范

一个 AML 文件由 DSDT 和 SSDT 表组成。从每个表的开头读取和解析 AML 字节码。这提供了有关 ACPI 命名空间中设备和对象定义的信息。使用此信息，AML 解释器可以生成系统中所有可用设备的列表，以及它们支持的属性和功能。

### DSDT 的示例 ASL 代码

DSDT 的 ASL 代码示例如下。

```
DefinitionBlock ("test.aml", "DSDT", 1, "OEMID ", "TABLEID  ", 0x00000000)
{
    Scope (_SB)
    {
        Device (PCI0)
        {
            Name (_HID, EisaId ("PNP0A03"))
    }
}
}
```

## 参考

* [ACPI AML](https://wiki.osdev.org/AML)
* [DSDT](https://wiki.osdev.org/DSDT)
* [SSDT](https://wiki.osdev.org/SSDT)

