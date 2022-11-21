{
  "date" : "2022-02-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์ MP - ไฟล์ LaTeX MetaPost",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ MP และ API ที่สามารถสร้างและเปิดไฟล์ MP",
  "linktitle" : "MP",
  "menu" : {
    "docs" : {
      "identifier":"image-mp",
      "parent" : "image"
}
},
  "lastmod" : "2022-02-23"
}

## ไฟล์ MP คืออะไร??

ไฟล์ MP เป็นไฟล์ภาพเวกเตอร์ที่สร้างโดยภาษาโปรแกรม MetaPost เพื่อสร้างรูปภาพ ภาพเวกเตอร์ที่สร้างโดยใช้รูปแบบไฟล์ MP จะถูกบันทึกเป็นไฟล์ [EPS](/th/image/eps/) (Encapsulated PostScript) นอกจากนี้ MetaPost ยังมาพร้อมกับเฟรมเวิร์ก TeX และ Metafont และสามารถสร้างไฟล์ MP จากภายในไฟล์ TEX และ LTX ที่แอปพลิเคชันเหล่านี้ใช้ ไฟล์ MP มีคำสั่งการวาดและการวาดอัลกอริทึมทางคณิตศาสตร์สำหรับการแสดงผลไฟล์ EPS เอาต์พุต เครื่องมือ PDFTex สามารถใช้ EPS ที่สร้างขึ้นเพื่อสร้างไฟล์ [PDF](/th/pdf/) ได้โดยตรง

## รูปแบบไฟล์ MP

ไฟล์ MP จะถูกบันทึกลงดิสก์เป็นไฟล์ไบนารี และสร้างเอาต์พุต EPS เมื่อส่งออกไปยังรูปแบบไฟล์ภาพเวกเตอร์เอาต์พุต ภาพวาดที่สร้างโดยใช้ MetaPost จะรวมอยู่ในรูปแบบที่จัดรูปแบบภายในเอกสารทางเทคนิคและสิ่งพิมพ์วารสารที่สร้างด้วย LaTex

### ตัวอย่างไฟล์ MetaPost MP

ต่อไปนี้เป็นตัวอย่าง อ้างอิงจาก [Berkeley Eductational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost) ซึ่งมีลูกศรและตัวอักษร "A" อยู่เหนือตรงกลางของ ลูกศร

```
outputtemplate:="%j%c.mps";
beginfig(1);

z1=(0,0);
z2=(10mm,10mm);

drawarrow(z1--z2);
label.ulft(btex $A$ etex, .5[z1,z2]);

endfig;

bye
```
## อ้างอิง ##

* [MetaPost โดย Wikipedia](https://en.wikipedia.org/wiki/MetaPost)
* [เมตาโพสต์ตัวอย่างน้ำยางโดย Berkeley Educational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost)

