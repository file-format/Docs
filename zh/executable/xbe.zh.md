{
  "date" : "2021-08-31",
  "keywords" :["xbe 文件","xbe 文件格式","什么是 xbe 文件","文件","xbe 示例","xbe 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 XBE 文件格式和可以创建和打开 XBE 文件的 API。",
  "title" :"XBE - iOS 应用程序包文件",
  "linktitle" : "XBE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-31"
}

## 什么是一 .xbe 文件？
具有 .xbe 扩展名的文件是来自 Xbox 视频游戏光盘的可执行应用程序。 XBE 文件是在 Xbox 系统中执行的主要文件，通常不应在计算机上打开，但可以使用 Xbox 仿真程序在 PC 上打开。这些文件通常由游戏开发者创建，然后由 Microsoft 签名。文件结构类似于 Windows PE 文件，但根据 XBox 设置应用了一些重要更改，使其可在 XBox 上运行。

## XBE 文件格式
XBE 文件由图像头、节头集合、证书、线程本地存储数据、库版本集合、Microsoft 位图以及包含代码和资源的节组成。

### 图片标题
映像头包含解释可执行文件的其他组件在文件中的位置的信息，以及应如何处理和加载可运行文件。

### TLS 表
TLS 表包含 XBE 正确设置线程本地存储所需的所有信息。它基本上是 PE32 文件中的 TLS 目录唯一的，可以直接从那里复制。如果 XBE 文件不使用任何线程本地存储，并且图像头中的相应字段设置为零，则可以省略此表。

|偏移 |尺寸 |姓名 |说明 |
--------|--------|--------|------------|
| 0x0000 | 0x0004 |原始数据开始 |程序映像中 TLS 变量数据的绝对（即不是 RVA）起始地址。 |
| 0x0004 | 0x0004 |原始数据结束 |程序映像中 TLS 变量数据结束的绝对（即不是 RVA）地址。 |
| 0x0008 | 0x0004 |索引地址 | TLS 索引变量的绝对（即不是 RVA）地址。 |
| 0x000C | 0x0004 |回调地址 |空终止的 TLS 回调函数表的绝对（即不是 RVA）地址。 |
| 0x0010 | 0x0004 |零填充的大小 |在内存中应设置为零的原始数据之后的字节数。 |
| 0x0014 | 0x0004 |特点 |描述对齐。 |

＃＃＃ 证书

每个包含标题信息的 Xbox 可执行文件都必须有一个证书：
 


- 创建证书的时间和日期
- 标题 ID
- 标题名称
- 替代标题 ID
- 允许运行可执行文件的媒体类型（HD、DVD、CD 等）
- 游戏区域
- 游戏评分
- 磁盘编号
- 版本
- 用于系统链接的 LAN 密钥原始数据
- 签名密钥原始数据（用于签署存档游戏）
- 备用签名密钥
- 证书原件尺寸
- 在线服务名称（不存在于早期的可执行文件中）
- 运行时安全标志（早期的可执行文件中不存在）
 


### 允许的媒体类型
可执行文件允许从中运行的媒体类型。以下值是已知的：
|媒体类型 |价值 |
---------------------|------------|
|硬盘 | 0x00000001 |
| DVD_X2 | 0x00000002 |
| DVD_CD | 0x00000004 |
|光盘 | 0x00000008 |
| DVD_5_RO | 0x00000010 |
| DVD_9_RO | 0x00000020 |
| DVD_5_RW | 0x00000040 |
| DVD_9_RW | 0x00000080 |
|加密狗 | 0x00000100 |
|媒体板 | 0x00000200 |
| NONSECURE_HARD_DISK | 0x40000000 |
|非安全模式 | 0x80000000 |
|媒体掩码 | 0x00FFFFFF |

### 部分
节由节标题表示。部分标题在证书之后开始，并包含文件中实际部分所在位置的信息。 Xbox 可执行文件中始终至少存在两个部分：


- 。文本


- .rdata


## 参考



* [Xbe - XBox 可执行文件](https://xboxdevwiki.net/Xbe)

