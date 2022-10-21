{
  "date" : "2019-10-11",
  "keywords" :["dicom 文件","dicom 文件格式","什么是 dicom 文件","文件","dicom 示例","dicom 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DICOM - 数字成像和通信文件格式",
  "description":"了解可创建和打开 DICOM 文件的 DICOM 文件格式和 API。",
  "linktitle" : "DICOM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .dicom 文件？

DICOM 是 Digital Imaging and Communications in Medicine 的首字母缩写词，属于医学信息学领域。 DICOM 用于集成来自不同供应商的打印机、服务器、扫描仪等医疗成像设备，还包含每个患者的唯一识别数据。如果 DICOM 文件能够接收 DICOM 格式的图像数据，则它们可以在两方之间共享。 DICOM的通信部分是应用层协议，实体之间使用TCP/IP进行通信。 Web 服务支持的版本是 1.0、1.1、2 或更高版本。

## 历史 ＃＃

DICOM 由美国放射学会 (ACR) 和美国国家电气制造商协会 (NEMA) 联合开发，用于交换和查看 MRI、CT 扫描和超声图像等医学图像。最初，很难解码机器生成的图像。因此，ACR 和 NEMA 于 1983 年共同组建了一个团队，于 1985 年发布了其第一个标准 ACR/NEMA 300。第二个版本于 1988 年发布，更受厂商欢迎，但很快意识到第二个版本也需要改进。该标准的第 3 版于 1993 年作为“DICOM"发布。 3.0 仍然是最新版本，但自 1993 年以来一直在不断更新。

## DICOM 文件格式##

DICOM 是文件格式定义和网络通信协议的结合。 DICOM 使用 .DCM 扩展名。 .DCM 以两种不同的格式存在，即格式 1.x 和格式 2.x。 DCM Format 1.x 还提供两个普通版本和扩展版本。 HTTP 和 HTTPS 协议用于 DICOM 的 Web 服务。

### 文件头###

文件头包含 128 字节的文件前导码和 4 字节的 DICOM 前缀。

**Preamble #128 Bytes**|**Prefix #4 Bytes “D, I, C, M**

**Preamble** 用于访问 DICOM 文件中的图像和其他数据，提供与常用图像文件格式的兼容性。

**前缀**包含字符串“DICM"作为大写字符。

### 数据集###

每个文件必须包含一个表示 SOP 实例和具有相关 IOD 的 SOP 类的数据集。数据集是现实世界信息的表示。数据集包含数据元素，数据元素包含该对象的属性值。属性的结构在 IOD 中指定。一个 DICOM 数据对象由许多属性组成，包括名称、ID 等项目，以及一个包含图像像素数据的特殊属性。

### 数据元素###

数据元素由数据元素标签、值长度和数据元素的值组成。有 5 种类型的数据元素，即类型 1 必需数据元素、类型 1C 条件数据元素、类型 2 必需数据元素、类型 2C 条件数据元素和类型 3 可选数据元素。基本 三种类型的数据元素结构如下。

**具有显式 VR 的数据元素**

|组号|元素号|值表示|保留|值长度|值字段
---|---|---|---|---|---|
|2 字节|2 字节|2 字节|2 字节 # 0x00, 0x00|4 字节|“值长度字节"

**具有显式 VR 的数据元素**

|组号|元素号|值表示|值长度|值字段
---|---|---|---|---|
|2 字节|2 字节|2 字节|2 字节|"值长度字节"

**具有隐式 VR 的数据元素**


|组号|元素号|值长度|值字段
---|---|---|---|
|2 字节|2 字节|4 字节|"值长度字节"

1. **Data Element Tag**：一个有序整数，代表组号和元素号
1. **Value Representation VR**：VR是一个字符串，代表数据元素的VR。
1. **Value Length**：是无符号整数，表示值字段的显式长度。
1. **Value Field**：描述数据元素的值。

## 传输语法##

转移语法是一组编码规则，以明确表示更抽象的语法。在传输语法的帮助下，通信实体就它们支持的通用编码技术进行协商。

## 标准操作程序##

IOD 和 DIMSE 的联合定义了一个 SOP 类。 SOP 类定义包含可能限制使用 DIMSE 服务组中的服务或 IOD 属性的规则和语义。服务元素的示例是存储、获取、查找、移动等。对象的示例是 CT 图像、MR 图像，但还包括日程表、打印队列等。

## 服务 ＃＃

DICOM 提供各种服务，主要与数据通信有关。每一个都简要描述如下：


**存储：** DICOM 存储服务将图像或其他对象发送到图片存档和通信系统 (PACS) 或服务器。


**存储承诺：** 存储承诺服务用于确认图像已永久存储在任何类型的媒体上的设备上。


**查询/检索：** 此服务使工作站能够查找图像或其他对象的列表，然后从 PACS 中检索它们。


**模态工作清单：** 模态工作清单服务提供了已安排由图像采集设备执行的成像程序列表。


**打印：** 此服务将图像发送到打印机。

## IP上的端口号##

DICOM 使用以下 TCP 和 UDP 端口：

1. 104
1. 2761
1. 2762
1. 11112

## 参考 ＃＃

* [https://en.wikipedia.org/wiki/DICOM](https://en.wikipedia.org/wiki/DICOM)
* [https://www.leadtools.com/sdk/medical/dicom-spec](https://www.leadtools.com/sdk/medical/dicom-spec)
* [https://www.dicomstandard.org/concepts/](https://www.dicomstandard.org/concepts/)
* [https://www.dicomlibrary.com/dicom/](https://www.dicomlibrary.com/dicom/)

