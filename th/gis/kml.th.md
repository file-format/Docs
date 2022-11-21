{
  "date" : "2019-10-11",
  "keywords" :[ "ไฟล์ kml", "ไฟล์ kml คืออะไร", "ไฟล์", "ตัวอย่าง kml", "นามสกุลไฟล์ kml", "นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KML - ภาษามาร์กอัป Keyhole",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ KML และ API ที่สามารถสร้างและเปิดไฟล์ KML",
  "linktitle" : "KML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ KML คืออะไร?

KML, Keyhole Markup Language) มีข้อมูลเชิงพื้นที่ในรูปแบบ XML ไฟล์ที่บันทึกเป็น KML สามารถเปิดได้ในแอปพลิเคชันระบบสารสนเทศภูมิศาสตร์ (GIS) หากรองรับ แอปพลิเคชันจำนวนมากได้เริ่มให้การสนับสนุนรูปแบบไฟล์ KML หลังจากที่ได้รับการยอมรับเป็นมาตรฐานสากล KML ใช้โครงสร้างตามแท็กที่มีองค์ประกอบและแอตทริบิวต์ที่ซ้อนกัน แท็กทั้งหมดคำนึงถึงขนาดตัวพิมพ์และลำดับของแท็กเหล่านี้ตาม [KML](https://developers.google.com/kml/documentation/kmlreference) ข้อมูลอ้างอิง เป็นสิ่งสำคัญที่ต้องปฏิบัติตาม

## ประวัติย่อ ##

เดิมที KML ได้รับการพัฒนาเพื่อใช้กับ Google Earth ซึ่งแต่เดิมรู้จักกันในชื่อ Keyhole Earth Viewer KLM ถูกนำมาใช้เป็นมาตรฐานสากลในปี 2008 โดย Open Geospatial Consortium ในปี 2008 เนื่องจากรูปแบบนี้ได้รับการพัฒนาเพื่อใช้กับ Google Earth จึงมีความโดดเด่นในการเป็นรูปแบบแรกที่ดูและแก้ไขไฟล์ KML เมื่อเวลาผ่านไป ปัจจุบันมีโครงการจำนวนมากขึ้นเรื่อยๆ ที่ให้การสนับสนุนรูปแบบไฟล์ KML รวมถึง API ต่างๆ ในภาษาต่างๆ

## ข้อมูลจำเพาะรูปแบบไฟล์ KML ##

การอ้างอิง KML เป็นคำแนะนำฉบับสมบูรณ์สำหรับการอ้างอิงเพื่อให้มีข้อกำหนดรูปแบบไฟล์ที่สมบูรณ์ ไฟล์ KML มาตรฐานประกอบด้วย:

* เครื่องหมายบอกตำแหน่ง
* เครื่องหมายบอกตำแหน่ง HTMLin ที่สื่อความหมาย
* การซ้อนทับพื้น
* เส้นทาง
* รูปหลายเหลี่ยม

นอกเหนือจากนี้ ไฟล์ KML เวอร์ชันขั้นสูงสามารถมี:

* รูปแบบสำหรับเรขาคณิต
* สไตล์สำหรับไอคอนที่เน้น
* ภาพซ้อนทับหน้าจอ
* ลิงค์เครือข่าย

องค์ประกอบ KML แต่ละรายการมีข้อมูลละติจูดซึ่งระบุตำแหน่งทางภูมิศาสตร์ของข้อมูลที่มีอยู่ในไฟล์ อย่างไรก็ตาม อาจมีพารามิเตอร์เพิ่มเติม เช่น ส่วนหัว ระดับความสูง และความเอียง

### เครื่องหมายบอกตำแหน่ง ###

ใช้เพื่อแสดงตำแหน่งบนพื้นผิวโลกและระบุโดย<Point> ธาตุ. ต่อไปนี้คือตัวอย่างการแสดงหมุดในไฟล์ KML

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Placemark>
    <name>Simple placemark</name>
    <description>Attached to the ground. Intelligently places itself
       at the height of the underlying terrain.</description>
    <Point>
      <coordinates>-122.0822035425683,37.42228990140251,0</coordinates>
    </Point>
  </Placemark>
</kml>
```

### HTML อธิบายในเครื่องหมายบอกตำแหน่ง ###

ข้อมูลเพิ่มเติมสามารถเชื่อมโยงกับหมุดที่ปรับปรุงการแสดงของหมุด ข้อมูลดังกล่าวรวมถึงลิงค์ ขนาดตัวอักษร สไตล์ และสี นอกจากนี้ยังรวมถึงการจัดตำแหน่งข้อความและตารางเพื่อเป็นส่วนหนึ่งของหมุด

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <Placemark>
      <name>CDATA example</name>
      <description>
        <![CDATA[
          <h1>CDATA Tags are useful!</h1>
          <p><font color#"red">Text is <i>more readable</i> and
          <b>easier to write</b> when you can avoid using entity
          references.</font></p>
        ]]>
      </description>
      <Point>
        <coordinates>102.595626,14.996729</coordinates>
      </Point>
    </Placemark>
  </Document>
</kml>
```

### การซ้อนทับพื้น ###

สิ่งเหล่านี้แสดงถึงชั้นของภาพบนพื้นผิวโลก เดอะ<icon> elment มีลิงค์ไปยังไฟล์ภาพซ้อนทับ

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Folder>
    <name>Ground Overlays</name>
    <description>Examples of ground overlays</description>
    <GroundOverlay>
      <name>Large-scale overlay on terrain</name>
      <description>Overlay shows Mount Etna erupting
          on July 13th, 2001.</description>
      <Icon>
        <href>https://developers.google.com/kml/documentation/images/etna.jpg</href>
      </Icon>
      <LatLonBox>
        <north>37.91904192681665</north>
        <south>37.46543388598137</south>
        <east>15.35832653742206</east>
        <west>14.60128369746704</west>
        <rotation>-0.1556640799496235</rotation>
      </LatLonBox>
    </GroundOverlay>
  </Folder>
</kml>
```

### เส้นทาง ###

เส้นทางแสดงโดย<LineString> องค์ประกอบที่เป็นชุดของคู่ละติจูด เมื่อใช้สิ่งเหล่านี้ คุณจะสามารถสร้างเส้นทางประเภทต่างๆ มากมายใน Google Earth

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <name>Paths</name>
    <description>Examples of paths. Note that the tessellate tag is by default
      set to 0. If you want to create tessellated lines, they must be authored
      (or edited) directly in KML.</description>
    <Style id#"yellowLineGreenPoly">
      <LineStyle>
        <color>7f00ffff</color>
        <width>4</width>
      </LineStyle>
      <PolyStyle>
        <color>7f00ff00</color>
      </PolyStyle>
    </Style>
    <Placemark>
      <name>Absolute Extruded</name>
      <description>Transparent green wall with yellow outlines</description>
      <styleUrl>#yellowLineGreenPoly</styleUrl>
      <LineString>
        <extrude>1</extrude>
        <tessellate>1</tessellate>
        <altitudeMode>absolute</altitudeMode>
        <coordinates> -112.2550785337791,36.07954952145647,2357
          -112.2549277039738,36.08117083492122,2357
          -112.2552505069063,36.08260761307279,2357
          -112.2564540158376,36.08395660588506,2357
          -112.2580238976449,36.08511401044813,2357
          -112.2595218489022,36.08584355239394,2357
          -112.2608216347552,36.08612634548589,2357
          -112.262073428656,36.08626019085147,2357
          -112.2633204928495,36.08621519860091,2357
          -112.2644963846444,36.08627897945274,2357
          -112.2656969554589,36.08649599090644,2357
        </coordinates>
      </LineString>
    </Placemark>
  </Document>
</kml>
```

## การอ้างอิงเชิงพื้นที่ในไฟล์ KML ##

ข้อมูลที่อยู่ในไฟล์ภูมิสารสนเทศใดๆ เกี่ยวกับตำแหน่งทางภูมิศาสตร์สามารถมีความหมายต่างกันได้โดยไม่มีข้อมูลอ้างอิงเชิงพื้นที่ ตามค่าเริ่มต้น การอ้างอิงเชิงพื้นที่ของไฟล์ KML ถูกกำหนดโดย World Geodetic System ปี 1984, WGS84

## อ้างอิง ##

* [ข้อมูลอ้างอิง KML](https://developers.google.com/kml/documentation/kmlreference)
* [บทแนะนำสำหรับนักพัฒนาซอฟต์แวร์ของ Google สำหรับ KML](https://developers.google.com/kml/documentation/kml_tut)
* [รูปแบบไฟล์ KML](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)

