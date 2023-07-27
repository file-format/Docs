{
  "date" : "2019-10-11",
  "keywords" :["x3d 文件","x3d 文件格式","什么是 x3d 文件","文件","x3d 示例","x3d 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X3D - 3D 图像文件",
  "description":"了解 X3D 文件格式和可以打开和创建 X3D 文件的 API。",
  "linktitle" : "X3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .x3d 文件？
X3D 是一种基于 [XML](/zh/web/xml/) 的 3D 图形文件格式，用于呈现 3D 信息。它是一个模块化标准，由多个 ISO 规范定义。该格式支持矢量和光栅图形、透明度、照明效果和动画设置，包括旋转、淡入淡出和摆动。它在 2001 年成为 [VRML](/zh/3d/vrml/) 文件格式的继任者。X3D 具有编码颜色信息的优势（与 [STL](/zh/cad/stl/) 不同），该信息在将模型打印在颜色上时使用3D打印机。该格式具有对 VRML 的扩展，提供了使用 XML 语法以及 VRML97 的类似 Open Inventor 的语法或二进制格式对场景进行编码的能力。

X3D 的抽象规范 (ISO/IEC 19775) 于 2004 年首次获得 ISO 批准。X3D 的 XML 和 ClassicVRML 编码 (ISO/IEC 19776) 于 2005 年首次获得批准。

## X3D 文件格式

X3D 场景文件有一个通用的文件结构：

* 文件头（XML、ClassicVRML 或 Compressed Binary）
* X3D 根节点的开始，包括版本和配置文件属性
* 带有 Component 和 Meta 语句的 head 部分（都是可选的）
* X3D 场景图及其子节点
* X3D 根节点结束

## 例子 ＃＃

```
<!-- -------------------- X3D header and X3D root node with profile declaration -->
<!DOCTYPE X3D PUBLIC "ISO//Web3D//DTD X3D 3.2//EN"
                     "http://www.web3d.org/specifications/x3d-3.2.dtd">
<X3D profile#'Immersive' version#'3.2'
     xmlns:xsd#'http://www.w3.org/2001/XMLSchema-instance'
     xsd:noNamespaceSchemaLocation#'http://www.web3d.org/specifications/x3d-3.2.xsd'>

<!-- -------------------- head section with included meta data -->
  <head>
    <meta content#'HelloWorld.x3d' name#'title'/>
    <meta content#'Simple X3D example' name#'description'/>
    <meta content#'30 October 2000' name#'created'/>
    <meta content#'7 August 2010' name#'modified'/>
    <meta content#'Don Brutzman' name#'creator'/>
    <meta content#'http://www.web3D.org' name#'reference'/>
    <meta content#'http://x3dGraphics.com' name#'reference'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/HelloWorld.x3d' name#'identifier'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/HelloWorldTall.png' name#'image'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/license.html' name#'license'/>
    <meta content#'X3D-Edit 3.2, https://savage.nps.edu/X3D-Edit' name#'generator'/>
  </head>

<!-- -------------------- the X3D scene node with X3D nodes -->
  <Scene>
    <!-- Example scene to illustrate X3D nodes and fields (XML elements and attributes) -->
    <Group>
      <Viewpoint centerOfRotation#'0 -1 0' description#'Hello world!' position#'0 -1 7'/>
      <Transform rotation#'0 1 0 3'>
        <Shape>
          <Sphere/>
          <Appearance>
            <Material diffuseColor#'0 0.5 1'/>
            <ImageTexture url#'"earth-topo.png" "earth-topo.jpg" "earth-topo-small.gif"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo.png"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo.jpg"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo-small.gif"'/>
          </Appearance>
        </Shape>
      </Transform>
      <Transform translation#'0 -2 0'>
        <Shape>
          <Text string#'"Hello" "world!"'>
            <FontStyle justify#'"MIDDLE" "MIDDLE"'/>
          </Text>
          <Appearance>
            <Material diffuseColor#'0.1 0.5 1'/>
          </Appearance>
        </Shape>
      </Transform>
    </Group>
  </Scene>

<!-- -------------------- footer, closing X3D toot element -->
</X3D>
```

## 参考 ＃＃

* [X3D - 维基百科](https://en.wikipedia.org/wiki/X3D)
* [Web3D 联盟官方网站](https://www.web3d.org/)
* [X3D官网](https://www.web3d.org/x3d/what-x3d)

