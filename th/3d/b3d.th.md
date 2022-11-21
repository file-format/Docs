{
  "date" : "2021-04-19",
  "keywords": [ "Blitz3D", "b3d", "file", "extension", "format", "blitz3d games" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ B3D ที่ใช้ในเกม blitz3d และ API ที่สามารถเปิดและสร้างไฟล์ B3D",
  "title" :"ไฟล์โมเดลเอนทิตี B3D - Blitz3D",
  "linktitle" : "B3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-04-19"
}

## ไฟล์ B3D คืออะไร??

ไฟล์ที่มีนามสกุล .b3d คือไฟล์โมเดลที่ใช้โดย Blitz3D ซึ่งอาจมีโมเดลวิดีโอเกมสำหรับตัวละคร สิ่งปลูกสร้าง ภูมิประเทศ และวัตถุอื่นๆ Blitz3D เป็นภาษาโปรแกรมที่ใช้ในการสร้าง **เกม blitz3d** Blitz3D เป็นภาษาโปรแกรมที่ทรงพลัง ยืดหยุ่น และใช้งานง่ายซึ่งออกแบบมาเพื่อจุดประสงค์เดียวในการเขียนวิดีโอเกม นักพัฒนาสามารถสร้างเกม 3D ที่เต็มไปด้วยแอ็คชั่น, ปริศนา 2 มิติ, การผจญภัย, RPGS, อะไรก็ตามเพียงแค่ใช้ Blitz3D

Blitz3D ใช้ภาษาโปรแกรมพื้นฐาน ซึ่งง่ายต่อการเรียนรู้และใช้งาน ข้อเท็จจริงทั้งหมดเหล่านี้ทำให้ Blitz เหมาะสำหรับผู้เริ่มต้นและโปรแกรมเมอร์ที่มีประสบการณ์มากกว่า แม้ว่าคุณสมบัติจะค่อนข้างล้าสมัยกว่าที่พบในเอนจิ้น 3D สมัยใหม่ส่วนใหญ่ แต่โปรแกรมเมอร์เกมจำนวนมากทั่วโลกยังคงใช้ Blitz3D ต่อไป

## ประวัติโดยย่อของ Blitz3D

Blitz3D ได้รับการเผยแพร่โดยทั่วไปสำหรับระบบปฏิบัติการ Microsoft Windows ในเดือนกันยายน พ.ศ. 2544 เพื่อแข่งขันกับภาษาการพัฒนาเกมอื่นๆ ที่คล้ายคลึงกัน Blitz3D เป็นเวอร์ชันอัปเกรดเหนือเอนจิน 2 มิติ BlitzBasic รุ่นก่อนหน้า ซึ่งขยายชุดคำสั่งด้วยการเพิ่ม API สำหรับเอนจิ้น 3 มิติที่ใช้ DirectX 7 ผู้ใช้ Blitz3D ควรเปรียบเทียบ BlitzMax ซึ่งเป็นเครื่องมือที่ใหม่กว่าโดย BlitzBasic BlitzMax เป็นเวอร์ชันที่ซับซ้อนแต่มีประสิทธิภาพมากกว่าของ Blitz3D ซึ่งรองรับภาษาการเขียนโปรแกรมเชิงวัตถุ เป็นกราฟิก API ที่อัปเดตเพื่อให้เหมาะกับอักขระ Unicode, OpenGL และส่งออกไปยัง OSX และ Linux แทนที่จะเป็น Windows เท่านั้น

## ตัวอย่าง B3D
ไฟล์ b3d ที่มี 1 TEXS chunk, 1 BRUS chunk และ 1 NODE chunk จะมีลักษณะดังนี้:

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
เมชที่เรียบง่ายไม่มีภาพเคลื่อนไหวและไม่มีพื้นผิวจะมีลักษณะดังนี้:

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


## อ้างอิง
* [B3D](https://moddb.fandom.com/wiki/B3D)
* [Blitz BASIC](https://en.wikipedia.org/wiki/Blitz_BASIC)

