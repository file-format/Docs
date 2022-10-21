{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAR - 可扩展存档文件格式",
  "description":"了解 XAR 文件格式和可以创建和打开 XAR 文件的 API。",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
      "identifier": "compression-xar",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## 什么是一 .xar 文件？

具有 .xar（可扩展存档格式）扩展名的文件是一个 UNIX 存档，可以是压缩或非压缩格式。它还用于 Mac OS 上的软件包安装。 XAR 是开源的，是 Mac OS X 10.5 的一部分，可与 Safari 浏览器一起使用。

## XAR 文件格式

[XAR](https://github.com/mackyle/xar/wiki/xarformat) 文件具有三个主要区域。

* 标题
* 目录
* 堆

### XAR 标头

XAR 标头的结构如下。

|字段|数据类型|字节大小|
---|---|---|
|魔术|无符号整数 32|4|
|大小|无符号整数 16|2|
|版本|无符号整数 16|2|
|TOC 长度压缩|无符号整数 64|8|
|TOC 长度未压缩|无符号整数 64|8|
|校验和|无符号整数 32|4|
|消息摘要名称 |空终止||

XAR头的C结构可以定义如下。
```
struct xar_header {
    uint32_t magic;
    uint16_t size;
    uint16_t version;
    uint64_t toc_length_compressed;
    uint64_t toc_length_uncompressed;
    uint32_t cksum_alg;
    /* A nul-terminated, zero-padded to multiple of 4, message digest name
     * appears here if cksum_alg is 3 which must not be empty ("") or "none".
     */
};
```
请注意，标头的所有字段（magic、大小、版本、toc_length_compressed、toc_length_uncompressed、cksum_alg）始终以网络字节（又名大端）顺序存储在 XAR 文件中。

### XAR 目录 (TOC)

目录是一个 XML 文档，它（并且必须）被编码为 UTF-8。它存储在文件的开头，便于扫描存档以提取单个文件。 XAR 存档允许您使用不同的压缩方案独立压缩/编码存档中的各个文件，例如 [GZIP](/zh/compression/gz/)、[BZIP2](/zh/compression/bz2) 和其他类似方案。

```
<?xml version="1.0"?>

<xar>
  <toc>
    <checksum style="sha1">
      <size>20</size>
      <offset>0</offset>
    </checksum>
    <file id="1">
      <name>xar</name>
      <type>file</type>
      <mode>0755</mode>
      <uid>0</uid>
      <gid>0</gid>
      <user>root</user>
      <group>wheel</group>
      <size>81180</size>
      <data>
        <offset>0</offset>
        <size>74108</size>
        <length>23083</length>
        <extracted-checksum style="md5">d852c77ac3c8e83f312c12b4c3198e6d</checksum>
        <archived-checksum style="md5">ceaf793ccb1990ecbadb20112d5f9e5d</checksum>
        <encoding style="application/x-gzip"/>
      </data>
      <ea>
        <name>com.apple.ResourceFork</name>
        <offset>0</offset>
        <size>7072</size>
        <length>3942</length>
        <extracted-checksum style="md5">0f7061dca2d7411352377db0e53792db</checksum>
        <archived-checksum style="md5">c72de8ac25abe462a930254d82958534</checksum>
        <encoding style="application/x-gzip"/>
      </ea>
    </file>
  </toc>
</xar>
```

### 堆

压缩后的 toc 立即开始堆。它是 TOC 引用的非结构化数据堆。 TOC 中列出的偏移值从堆的开头开始。 toc 中的长度值是指存储在堆中的实际字节数（压缩与否），而大小值是指提取的项目大小（必要时解压缩后）。

## 参考

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)
* [XAR - 维基百科](https://en.wikipedia.org/wiki/Xar_(archiver))

