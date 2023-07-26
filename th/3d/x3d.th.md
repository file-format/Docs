{
  "date" : "2019-10-11",
  "keywords" :[ "ไฟล์ x3d", "รูปแบบไฟล์ x3d", "ไฟล์ x3d คืออะไร", "ไฟล์", "ตัวอย่าง x3d", "นามสกุลไฟล์ x3d","ส่วนขยาย", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X3D - ไฟล์ภาพ 3 มิติ",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ X3D และ API ที่สามารถเปิดและสร้างไฟล์ X3D",
  "linktitle" : "X3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ X3D คืออะไร??
X3D เป็นรูปแบบไฟล์กราฟิก 3 มิติที่ใช้ [XML](/th/web/xml/) สำหรับการนำเสนอข้อมูล 3 มิติ เป็นมาตรฐานแบบโมดูลาร์และถูกกำหนดผ่านข้อกำหนด ISO หลายข้อ รูปแบบนี้รองรับกราฟิกแบบเวกเตอร์และแรสเตอร์ ความโปร่งใส เอฟเฟกต์แสง และการตั้งค่าแอนิเมชัน รวมถึงการหมุน การจาง และการแกว่ง กลายเป็นรูปแบบที่สืบทอดมาจากรูปแบบไฟล์ [VRML](/th/3d/vrml/) ในปี 2544 X3D มีข้อได้เปรียบในการเข้ารหัสข้อมูลสี (ไม่เหมือน [STL](/th/cad/stl/)) ที่ใช้ระหว่างการพิมพ์แบบจำลองบนสี เครื่องพิมพ์สามมิติ. รูปแบบมีส่วนขยายของ VRML ทำให้สามารถเข้ารหัสฉากโดยใช้ไวยากรณ์ XML รวมถึงไวยากรณ์แบบ Open Inventor ของ VRML97 หรือการจัดรูปแบบไบนารี

ข้อกำหนดเชิงนามธรรมสำหรับ X3D (ISO/IEC 19775) ได้รับการอนุมัติครั้งแรกโดย ISO ในปี 2004 การเข้ารหัส XML และ ClassicVRML สำหรับ X3D (ISO/IEC 19776) ได้รับการอนุมัติครั้งแรกในปี 2005

## รูปแบบไฟล์ X3D

ไฟล์ฉาก X3D มีโครงสร้างไฟล์ทั่วไป:

* ส่วนหัวของไฟล์ (ทั้ง XML, ClassicVRML หรือไบนารีที่บีบอัด)
* การเริ่มต้นของรูตโหนด X3D รวมถึงแอตทริบิวต์เวอร์ชันและโปรไฟล์
* ส่วนหัวพร้อมคำสั่ง Component และ Meta (ทั้งสองตัวเลือก)
* กราฟ X3D Scene และโหนดย่อย
* จุดสิ้นสุดของรูทโหนด X3D

## ตัวอย่างรูปแบบไฟล์ X3D

```
<!-- -------------------- X3D header and X3D root node with profile declaration -->
<!DOCTYPE X3D PUBLIC "ISO//Web3D//DTD X3D 3.2//EN"
                     "http://www.web3d.org/specifications/x3d-3.2.dtd">
<X3D profile#'Immersive' version#'3.2'
     xmlns:xsd#'http://www.w3.org/2001/XMLSchema-instance'
     xsd:noNamespaceSchemaLocation#'http://www.web3d.org/specifications/x3d-3.2.xsd'>

<!-- -------------------- head section with included meta data -->
  <head>
    <meta content#'HelloWorld.x3d' name#'title'/>,
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

## อ้างอิง ##

* [X3D - โดย Wikipedia](https://en.wikipedia.org/wiki/X3D)
* [เว็บไซต์ทางการของ Web3D Consortium](https://www.web3d.org/)
* [เว็บไซต์อย่างเป็นทางการของ X3D](https://www.web3d.org/x3d/what-x3d)

