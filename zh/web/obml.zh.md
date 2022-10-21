{
  "date" : "2022-05-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OBML 文件格式 - Opera Mini 保存的网页文件",
  "description" :"了解什么是 OBML 文件以及可以创建和打开 OBML 文件的 API。",
  "linktitle" : "OBML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-05-19"
}

## 什么是一 .obml 文件？

OBML（Opera 二进制标记语言）文件是由 Opera Mini 移动网络浏览器保存的网页的离线版本。它是 [HTML](/zh/web/html/) 文件的独立、紧凑版本，其中包含页面的所有元素，可在离线时在特定设备上显示。 OBML 文件格式已升级到多个版本，并且广泛使用 OBML15 和 OBML16。需要注意的重要一点是，每个 Opera Mini 版本仅兼容一种 OBML 格式。因此，升级 Opera Mini 将使之前保存的页面保持可读性。 OBML 文件可以转换为 HTML 和 [PDF](/zh/pdf/)。

## OBML 文件格式

OBML 文件格式以 Opera 的专有文件格式保存，其文件格式规范不公开。然而，[OMBL 格式](https://github.com/grawity/obml-parser/blob/master/obml.md) 被逆向工程以解码其结构如下。

### OBML 数据类型

根据逆向工程结果，OBML 使用以下原始类型：

* `byte` – 无符号整数（1 字节）
* `short` – 有符号整数（2 字节，大端）
* `medium` – 有符号整数（3 字节，大端）
 * `blob` – { length: short, data: byte[length] }
* `char` – 一个包含 ASCII 字符的字节
* `string` – 一个包含 UTF-8 编码文本的 blob

### OBML 标头

```
header := {
	(if version >= 15) {
		fake_file_size: medium = 0x02d355
		fake_version: byte     = 16
	}
	file_size: medium
	version: byte
	page_size: coords
	(if version == 16) {
		unknown: byte[3]      // always S\x00\x00
	}
	unknown: short                // always -1
	page_title: string
	unknown: blob
	page_url_base: string
	page_url: url
	(if version >= 15) {
		unknown: byte[6]
	}
	(if 6 < version <= 13) {
		unknown: byte[5]
	}
	(if version == 6) {
		unknown: byte[1]
	}
	metadata: chunk[]
	content: chunk[]
}
```
## 参考

* [OMBL 格式](https://github.com/grawity/obml-parser/blob/master/obml.md)

