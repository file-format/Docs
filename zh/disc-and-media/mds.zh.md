{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 MDS 文件格式和可以创建和打开 MDS 文件的 API。”,
  "title" :"MDS 文件格式 - 媒体描述符附属文件”，
  "linktitle" : "MDS",
  "menu" : {
    "docs" : {
      "identifier":"disc_and_media-mds",
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2023-01-23"
}

## 什么是 .mds 文件？

MDS（媒体描述符附属文件）是与软件 Alcohol 120% 和 Daemon Tools 相关联的文件，这两个软件都用于创建和管理虚拟 CD 和 DVD 驱动器。 MDS 文件包含有关光盘上数据布局的信息，包括所有文件的位置和光盘的结构。这允许虚拟驱动器模拟物理磁盘的行为，以便软件可以读取虚拟磁盘上的数据，就好像它是真实磁盘一样。

当您想要将映像文件挂载到虚拟驱动器时，MDS 文件与相应的映像文件一起使用，格式为 ISO、BIN 或 CUE。 MDS 文件包含磁盘上数据布局的描述，虚拟光驱软件使用此信息创建虚拟磁盘。这使您可以像使用物理光盘一样使用该软件，而无需将光盘实际插入驱动器。

## 与酒精的关系 120%

Alcohol 120% 是一种用于创建和管理虚拟 CD 和 DVD 驱动器的流行软件，它使用 MDS 文件格式来保存和访问光盘映像。 MDS 文件格式为 Alcohol 120% 专有，只能由 Alcohol 120% 软件或其他支持它的软件打开和使用。

## 如何打开 .MDS 文件？

要在 Alcohol 120% 中打开 MDS 文件，您需要在计算机上安装该软件。安装 Alcohol 120% 后，您可以通过执行以下操作打开 MDS 文件：

1. 启动 Alcohol 120%。
2. 单击“文件”菜单并选择“打开”。
3. 导航到计算机上 MDS 文件的位置并选择它。
4. MDS 文件现在将在 Alcohol 120% 中打开，系统将提示您选择相应的映像文件（例如 ISO、BIN 或 CUE）。
5. 选择映像文件后，Alcohol 120% 会将映像装载到虚拟驱动器。

或者，如果将 Alcohol 120% 设置为打开 MDS 文件的默认程序，您也可以通过双击打开 MDS 文件。您还可以使用其他支持 MDS 格式的软件，如 Daemon Tools、Virtual CloneDrive、Virtual Drive Manager 和 MagicISO。

## 参考
* [Alcohol 120% - CD和DVD刻录软件](https://www.alcohol-soft.com/)

