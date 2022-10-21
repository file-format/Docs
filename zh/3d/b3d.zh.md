{
  "date" : "2021-04-19",
  "keywords": [ "Blitz3D", "b3d", "file", "extension", "format", "blitz3d games" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 B3D 文件格式；用于 blitz3d 游戏和可打开和创建 B3D 文件的 API。",
  "title" :"B3D - Blitz3D 实体模型文件",
  "linktitle" : "B3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-04-19"
}

## 什么是一 .b3d 文件？
带有 .b3d 扩展名的文件是 Blitz3D 使用的模型文件，其中可能包含角色、建筑物、地形和其他对象的视频游戏模型。 Blitz3D 是一种用于创建 **blitz3d 游戏** 的编程语言。 Blitz3D 是一种功能强大、灵活且易于使用的编程语言，专为编写视频游戏而设计。开发人员可以通过使用 Blitz3D 来创建动感十足的 3D 游戏、2D 益智游戏、冒险、角色扮演游戏等。 Blitz3D 基于 BASIC 编程语言；这也很容易学习和使用。所有这些事实使 Blitz 成为初学者和更有经验的程序员的理想选择。尽管它的功能被认为比大多数现代 3D 引擎中的功能有些陈旧，但 Blitz3D 继续被全球许多游戏程序员使用。

## Blitz3D 简史
Blitz3D 基本上是在 2001 年 9 月针对 Microsoft Windows 操作系统发布的，以与其他类似的游戏开发语言竞争。 Blitz3D 是早期 2D 引擎 BlitzBasic 的升级版本，它通过添加基于 DirectX 7 的 3D 引擎的 API 扩展了它的命令集。 Blitz3D 用户还应该比较 BlitzMax，它是 BlitzBasic 的后期引擎。 BlitzMax 是一个复杂但更强大的 Blitz3D 版本，它支持面向对象的编程语言。它是一个更新的图形 API，以更好地适应 Unicode 字符、OpenGL，并导出到 OSX 和 Linux 而不仅仅是 Windows。

## B3D 示例
包含 1 个 TEXS 块、1 个 BRUS 块和 1 个 NODE 块的 b3d 文件将如下所示：

```
BB3D
  1
  TEXS
    ...list of textures...
  BRUS
    ...list of brushes...
  NODE
    ...stuff in the node...
```
一个简单的、非动画和非纹理网格将如下所示：

```
BB3D
  1                           ;version
  NODE
    "root_node"               ;node name
    0,0,0                     ;position
    1,1,1                     ;scale
    1,0,0,0                   ;rotation
    MESH                      ;the mesh
      -1                      ;brush: no brush
      VRTS                    ;vertices in the mesh
        0                     ;no normal/color info in verts
        0,0                   ;no texture coords in verts
        {x,y,z...}            ;vertex coordinates
      TRIS                    ;triangles in the mesh
        -1                    ;no brush for this triangle
        {v0,v1,v2...}         ;vertices
```


## 参考
* [B3D](https://moddb.fandom.com/wiki/B3D)
* [闪电战基础](https://en.wikipedia.org/wiki/Blitz_BASIC)

