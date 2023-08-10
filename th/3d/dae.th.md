{
  "date" : "2019-10-11",
  "keywords" :[ "ไฟล์ dae", "รูปแบบไฟล์ dae", "ไฟล์ dae คืออะไร", "ไฟล์", "ตัวอย่าง dae", "นามสกุลไฟล์ dae","นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ DAE และ API ที่สามารถเปิดและสร้างไฟล์ DAE",
  "title" :"DAE - รูปแบบไฟล์การแลกเปลี่ยนสินทรัพย์ดิจิทัล",
  "linktitle" : "DAE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ DAE คืออะไร??

ไฟล์ DAE เป็นรูปแบบไฟล์ Digital Asset Exchange ที่ใช้สำหรับแลกเปลี่ยนข้อมูลระหว่างแอปพลิเคชัน 3 มิติแบบโต้ตอบ รูปแบบไฟล์นี้อ้างอิงจาก COLLADA (COLLAborative Design Activity) XML schema ซึ่งเป็น XML schema มาตรฐานเปิดสำหรับการแลกเปลี่ยนสินทรัพย์ดิจิทัลระหว่างแอปพลิเคชันซอฟต์แวร์กราฟิก ISO/pAS 17506 ได้รับการรับรองมาตรฐาน ISO/pAS 17506 ไฟล์ DAE สามารถเปิดได้ในแอปพลิเคชันต่างๆ เช่น Adobe Photoshop, AutoDesk Maya, AutoDesk AutoCAD และ API เช่น [Aspose.CAD](https://products.aspose.com/cad/).

## รูปแบบไฟล์ DAE

รูปแบบไฟล์ DAE อ้างอิงจาก [COLLADA XML schema](https://www.khronos.org/files/collada_spec_1_5.pdf) ซึ่งองค์ประกอบทั้งหมดถูกกำหนดเป็นแท็ก XML ช่วยให้สามารถรวมเครื่องมือประมวลผล DCC และ 3D ที่หลากหลายเข้ากับขั้นตอนการผลิตสำหรับสินทรัพย์ 3 มิติได้ มีการเข้ารหัสที่ครอบคลุมของฉากภาพ รวมถึงเรขาคณิต แอนิเมชัน เฉดสี และฟิสิกส์ รูปแบบเปิด เก็บถาวรเกรด และเก็บข้อมูลเมตา

### แท็ก COLLADA

แท็กสคีมาของ COLLADA แสดงไว้ด้านล่าง
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
### แท็กสินทรัพย์

แท็กสินทรัพย์อธิบายผู้เขียนและสภาพแวดล้อมของไฟล์

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### ห้องสมุดกล้อง

เนื้อหาของ COLLADA มีอยู่ในห้องสมุด ไลบรารี่ของกล้องประกอบด้วยกล้องที่ไม่น่าแปลกใจ กล้องทั่วไปเป็นแบบเปอร์สเปคทีฟหรือออโธกราฟิก แท็กคลังกล้องถูกกำหนดดังนี้
```
<library_cameras>
    <camera id="PerspCamera" name="PerspCamera">
      <optics>
        <technique_common>
          <perspective>
            <yfov>37.8493</yfov>
            <aspect_ratio>1</aspect_ratio>
            <znear>10</znear>
            <zfar>1000</zfar>
          </perspective>
        </technique_common>
      </optics>
    </camera>
</library_cameras>
```
###ไฟ

ไฟทั่วไปเป็นแบบจุด จุด หรือแบบทิศทาง
```
<library_lights>
    </light>
    <light id="pointLightShape1-lib" name="pointLightShape1">
      <technique_common>
        <point>
          <color>1 1 1 </color>
          <constant_attenuation>1</constant_attenuation>
          <linear_attenuation>0</linear_attenuation>
          <quadratic_attenuation>0</quadratic_attenuation>
        </point>
      </technique_common>
    </light>
</library_lights>
```

### ตัวอย่างวัสดุ

เอฟเฟ็กต์ของอินสแตนซ์ Materials ถูกกำหนดดังนี้
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### ผลกระทบทั่วไป

เอฟเฟกต์ทั่วไปทำหน้าที่เหมือนสถานะ OpenGL 1 และสามารถกำหนดได้ดังต่อไปนี้

```
<library_effects>
    <effect id="Blue-fx">
      <profile_COMMON>
        <technique sid="common">
          <phong>
            <emission>
              <color>0 0 0 1 </color>
            </emission>
            ...
            <index_of_refraction>
              <float>0</float>
            </index_of_refraction>
          </phong>
        </technique>
      </profile_COMMON>
    </effect>
</library_effects>
```

### คุณสมบัติทางเรขาคณิต

เรขาคณิตอธิบายแอตทริบิวต์ OpenGL และกำหนดไว้ดังนี้
```
<library_geometries>
    <geometry id="box-lib" name="box">
      <mesh>
        <source id="box-lib-positions" name="position">
        </source>
        <source id="box-lib-normals" name="normal">
        </source>
        ...
        <vertices id="box-lib-vertices">
          <input semantic="POSITION" source="#box-lib-positions"/>
        </vertices>
        <polylist count="6" material="BlueSG">
          <input offset="0" semantic="VERTEX" source="#box-lib-vertices"/>
          <input offset="1" semantic="NORMAL" source="#box-lib-normals"/>
          <vcount>4 4 4 4 4 4 </vcount>
          <p>0 0 2 1 3 2 1 3 0 4 1 5 5 6 4 7 ...</p>
        </polylist>
      </mesh>
    </geometry>
</library_geometries>
```

### ฉากภาพ

ฉากภาพเป็นเหมือนฉากเอกภาพและมีลำดับชั้นของโหนดดังต่อไปนี้
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">,
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## อ้างอิง
* [ข้อมูลจำเพาะของ COLLADA 1.5.0](https://www.khronos.org/files/collada_spec_1_5.pdf)

