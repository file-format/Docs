{
  "date" : "2022-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Torrent 文件格式 - BitTorrent 文件",
  "description":"了解可以创建和打开 TORRENT 文件的 TORRENT 文件和 API。",
  "linktitle" : "TORRENT",
  "menu" : {
    "docs" : {
"标识符":"misc-torrent",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## 什么是 .torrent 文件？

TORRENT 文件是由 BitTorrent 和其他 P2P（点对点）程序用于下载和交换内容的文本文件。可下载的内容可以包括互联网上可用的文档、视频、游戏、电影和其他媒体。它包括有关要下载的媒体的内容和位置的元数据信息。 BitTorrent 等软件使用此文件中的信息（例如名称、文件大小和文件夹结构）来下载数据。 Torrent文件可以在线转换为其他文件格式，例如[PDF](/zh/pdf/)。

## 什么是洪流？用于数据交换的 TORRENT 文件格式

Torrenting 是使用 BitTorrent 网络交换（下载和上传）数据文件的概念。与上传数据供其他人访问和下载的传统服务器不同，torrent 文件是使用 torrent 网络检索和发送的。当用户在 BitTorrent 等应用程序中打开 .torrent 文件时，软件会开始按位下载文件的内容。如果多个用户拥有相同的文件，BitTorrent 会在所有用户之间拆分下载以加快下载过程。同时，正在下载该文件的用户的计算机也成为将其发送给同样下载相同文件的其他用户的文件源。

### 种子文件的结构

Torrent 文件是文件列表和有关要下载的所有文件的元数据信息的组合。它以密钥的形式包含以下信息。

- `announce` - 向其他对等点宣布的跟踪器的 URL，用于通知文件的可用性
- `info` - 这映射到一个字典，其键取决于是否共享一个或多个文件：
  - files—a list of dictionaries each corresponding to a file (only when multiple files are being shared). Each dictionary has the following keys:
- `length` — 文件的大小（以字节为单位）。
- `path` — 对应于子目录名称的字符串列表，最后一个是实际文件名
- `length` — 文件的大小（以字节为单位）（仅当共享一个文件时）
- `name` — 保存文件的文件名
- `片长` - 每片的字节数。这通常是 28 KiB = 256 KiB = 262,144 B。
- `pieces` — 一个哈希列表，它是每个片段的 SHA-1 哈希的串联。

## 洪流安全合法吗？

在 P2P 用户之间交换数据的 Torrenting 协议是安全的，因为它只是共享任何类型文件的手段。因此，协议本身并不是不安全或非法的。但是，通过网络共享的内容可能包含可能违反共享文档法律地位的文件或媒体。在这种情况下，此类数据的交换可能会导致对参与公开共享此类文件的各方采取法律行动。

## 参考

* [TORRENT 文件 - 维基百科](https://en.wikipedia.org/wiki/Torrent_file)

