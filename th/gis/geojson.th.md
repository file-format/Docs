{
  "date" : "2019-10-11",
  "keywords" :[ "ไฟล์ geojson", "ไฟล์ geojson คืออะไร", "ไฟล์", "ตัวอย่าง geojson", "นามสกุลไฟล์ geojson", "นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GeoJSON - รูปแบบไฟล์ทางภูมิศาสตร์ตาม JSON",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ GeoJSON และ API ที่สามารถสร้างและเปิดไฟล์ GeoJSON",
  "linktitle" : "GeoJSON",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ GeoJSON คืออะไร??

GeoJSON เป็นรูปแบบตาม JSON ที่ออกแบบมาเพื่อแสดงคุณลักษณะทางภูมิศาสตร์ด้วยแอตทริบิวต์ที่ไม่ใช่เชิงพื้นที่ รูปแบบนี้กำหนดออบเจกต์ JSON (JavaScript Object Notation) ที่แตกต่างกันและรูปแบบการรวม รูปแบบ JSON แสดงถึงข้อมูลโดยรวมเกี่ยวกับลักษณะทางภูมิศาสตร์ ขอบเขตเชิงพื้นที่ และคุณสมบัติต่างๆ ออบเจกต์ของไฟล์นี้อาจระบุรูปทรงเรขาคณิต (Point, LineString, Polygon) คุณลักษณะหรือชุดคุณลักษณะ คุณลักษณะนี้แสดงที่อยู่และสถานที่เป็นถนนของจุด ถนนสายหลัก และเส้นขอบเป็นสตริงเส้น และประเทศ จังหวัด และภูมิภาคเป็นรูปหลายเหลี่ยม เมื่อใช้ GeoJSON แอปพลิเคชันการกำหนดเส้นทางและการนำทางบนมือถือต่างๆ สามารถระบุความครอบคลุมของบริการของตนได้ ส่วนขยายของ GeoJSON คือ TopoJSON ที่มีขนาดเล็กกว่าและเข้ารหัสโทโพโลยีเชิงพื้นที่

## ประวัติย่อ ##

Internet Engineering Task Force (IETF) ร่วมกับผู้เขียนรูปแบบ ได้สร้าง [GeoJSON WG](https://datatracker.ietf.org/wg/geojson/charter/) เพื่อเผยแพร่ GeoJSON ในเดือนเมษายน 2015 แทนที่ 2008 ข้อมูลจำเพาะ GeoJSON [RFC 7946](https://tools.ietf.org/html/rfc7946) ข้อกำหนดมาตรฐานใหม่ของรูปแบบ GeoJSON ที่เผยแพร่ในเดือนสิงหาคม 2016

## รูปแบบไฟล์ GeoJSON ##

### พิกัด ###

พิกัดเป็นองค์ประกอบพื้นฐานของข้อมูลทางภูมิศาสตร์ใดๆ นี่คือมิติเดียว (ลองจิจูด, ละติจูด) ที่แสดงตัวเลขเดียว (รูปแบบทศนิยม) และบางครั้งบันทึกพิกัดสำหรับระดับความสูงด้วย เวลาก็เป็นมิติเช่นกัน แต่ความซับซ้อนทำให้บันทึกเป็นพิกัดได้ยาก พิกัดใน JSON GeoJSON ทั้งสองมีรูปแบบเหมือนตัวเลข

### ตำแหน่ง ###

อาร์เรย์พิกัดที่เรียงตามลำดับแสดงถึง [ตำแหน่ง](http://geojson.org/geojson-spec.html#positions) นี่คือหน่วยที่เล็กที่สุดที่สามารถระบุจุดบนโลกได้

`[ลองจิจูด ละติจูด ระดับความสูง]`

ก่อนการเปิดตัวข้อกำหนดปัจจุบัน GeoJSON อนุญาตให้บันทึกสามพิกัดต่อตำแหน่ง แต่ข้อกำหนดใหม่ไม่อนุญาต

### เรขาคณิต ###

รูปทรงเรขาคณิตเป็นรูปทรงง่ายๆ (จุด เส้นโค้ง และพื้นผิว) ใน GeoJSON ซึ่งประกอบด้วยประเภทและชุดของพิกัด จุดเป็นรูปทรงเรขาคณิตที่ง่ายที่สุดที่ใช้แทนตำแหน่งเดียว

`{ "ประเภท": "จุด", "พิกัด": [0, 0] }`

### เส้นสาย ###

ใช้ตำแหน่งที่เชื่อมต่อกันอย่างน้อยสองแห่งเพื่อแสดงเส้น

`{ "ประเภท": "LineString", "พิกัด": [[10, 30], [10, 10]] }`

สตริงจุดและเส้นเป็นสองประเภทที่ง่ายที่สุดของรูปทรงเรขาคณิต รูปทรงเรขาคณิตทั้งสองประเภทไม่รบกวนกฎทางเรขาคณิตมากนัก จุดสามารถแสดงในสถานที่ใดก็ได้ และเส้นสามารถมีจุดมากกว่าหนึ่งจุด แม้ว่าจุดนั้นจะมีจุดตัดกันในตัวเองก็ตาม

### รูปหลายเหลี่ยม ###

รูปทรงเรขาคณิต GeoJSON ดูเหมือนจะซับซ้อนกว่าในรูปหลายเหลี่ยมอย่างมาก รูปหลายเหลี่ยมมีพื้นที่ภายในและภายนอกและสามารถมีรูอยู่ข้างในได้

```
{
  "type": "Polygon",
  "Coordinates": [
    [
      [30, 10], [10, 10], [10, 0], [20, 40]
    ]
  ]
}
```

เมื่อเปรียบเทียบกับ LineStrings ในรูปหลายเหลี่ยม รายการของพิกัดจะซ้อนกันอีกหนึ่งระดับและสามารถมีการตัดลึกหนาบางเช่นโดนัท

### ระดับพิกัด ###

ในรูปแบบ GeoJSON สำหรับคุณสมบัติพิกัด มีความลึกสี่ระดับ

### คุณสมบัติ ###

รูปทรงเรขาคณิตเป็นส่วนสำคัญของ GeoJSON ดังนั้นข้อมูลในโลกแห่งความเป็นจริงจึงเป็นมากกว่ารูปทรงธรรมดาที่มีตัวตนและคุณสมบัติ คุณสมบัติจะบันทึกรูปทรงเรขาคณิตรวมถึงคุณสมบัติต่างๆ

```
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [20, 10]
},
  "properties": {
    "name": "fortune island"
  }
}

```

คุณสมบัติของคุณลักษณะสามารถเป็นวัตถุประเภท [JSON](http://json.org/) ที่มีการแมปค่าคีย์เชิงลึกระดับเดียว

### การรวบรวมคุณลักษณะ ###

ที่ระดับบนสุดของไฟล์ GeoJSON FeatureCollection เป็นสิ่งที่พบได้บ่อยที่สุดที่มีลักษณะดังนี้:

```
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [20, 10]
    },
      "properties": {
        "name": "null island"
  }
}
  ]
}
```

แพ็คเกจซอฟต์แวร์แผนที่และ GIS จำนวนมากรองรับ GeoJSON รวมถึงซอฟต์แวร์ GeoDjango, OpenLayers และ Geoforge นอกจากนี้ยังเข้ากันได้กับ PostGIS และ Mapnik บริการ API ของแผนที่ Google, yahoo และ Bing ยังรองรับ GeoJSON

## อ้างอิง ##

* [macwright.org](https://macwright.org/2015/03/23/geojson-second-bite.html)
* [GeoJSON - โดย Wikipedia](https://en.wikipedia.org/wiki/GeoJSON)
