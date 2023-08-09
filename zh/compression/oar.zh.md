{
  "date" : "2021-04-08",
  "keywords" :[ "oar file", "oar file format", "什么是 oar file", "file", "oar example", "oar file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OAR - OpenSimulator 存档文件格式",
  "description":"了解 OAR 文件格式和可以创建和打开 OAR 文件的 API。",
  "linktitle" : "OAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-15"
}

## 什么是一 .oar 文件？

扩展名为 .oar 的文件是 OpenSimulator 应用程序使用的存档文件，OpenSimulator 应用程序是一个开源 3D 应用程序服务器，用于创建可供多用户通过网络访问的虚拟环境。 OAR 文件格式提供了在不同系统上完全加载地形、对象纹理和库存所需的必要资产数据。 OpenSimulator 还具有可选的超网格，允许用户通过 Web 访问其他 OpenSimulator 安装。 OAR 文件具有互联网 MIME 类型 application/oar 并包含一个或多个存档文件。


## OAR 文件格式

OAR 是以压缩归档文件格式存储的二进制文件。 OAR 文件格式的最新版本是 [version 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)，与之前的 [version 0.8](http://opensimulator.org/wiki/OAR_Format_0.8) 相比有重大变化。最新版本支持在单个 OAR 中存储多个区域，并且不向后兼容 0.7.5 之前的 OpenSimulator 版本。 OAR 文件是原始 unix tar 格式（不是 USTAR）的 gzip 压缩 tar 文件 (tar.gz)。

## OAR 区域示例
AOR 文件可以包含多个区域。存档的结构如下（本示例包含 4 个区域）：

```
archive.xml
assets/
regions/
  1_1_Arizona/
    landdata/
    objects/
    settings/
    terrain/
  2_1_New_Mexico/
    landdata/
    objects/
    settings/
    terrain/
  1_2_Utah/
    landdata/
    objects/
    settings/
    terrain/
  2_2_Colorado/
    landdata/
    objects/
    settings/
    terrain/
```
## 桨存档.xml

存档控制文件包含一个主要版本号，用于定义与未来格式更改的兼容性。 OAR 格式的资产的存在由布尔元素指示<assets_included>.有关所包含区域的信息包含在控制文件中的清单中。 Archive.xml 的示例如下。

```
<?xml version="1.0" encoding="utf-16"?>
<archive major_version="1" minor_version="0">
  <creation_info>
    <datetime>1343204139</datetime>
  </creation_info>
  <assets_included>True</assets_included>
  <regions>
    <row>
      <region>
        <id>12345678-1111-1111-1111-111111111111</id>
        <dir>1_1_Arizona</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-2222-2222-2222-222222222222</id>
        <dir>2_1_New_Mexico</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
    <row>
      <region>
        <id>12345678-3333-3333-3333-333333333333</id>
        <dir>1_2_Utah</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-4444-4444-4444-444444444444</id>
        <dir>2_2_Colorado</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
  </regions>
</archive>
```

## 参考

* [OAR 格式 v 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
* [OpenSimulator](http://opensimulator.org/wiki/Main_Page)

