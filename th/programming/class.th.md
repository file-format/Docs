{
  "date" : "2019-10-11",
  "keywords" :[ "คลาส", ".คลาส", "ไฟล์คลาสคืออะไร", "วิธีเปิดไฟล์คลาส", "นามสกุล", "ไฟล์", "ไฟล์คลาส", "รูปแบบไฟล์คลาส", "นามสกุล .class ", "ไฟล์คลาสในภาษาจาวา" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"คลาส - รูปแบบไฟล์คลาส Java",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์คลาสและ API ที่สามารถสร้างและเปิดไฟล์คลาส",
  "linktitle" : "Class",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## ไฟล์คลาสคืออะไร?

**ไฟล์คลาสใน Java** เป็นเอาต์พุตที่คอมไพล์แล้วของคลาส [.java](/th/programming/java/) ที่ดำเนินการจริงโดย Java Virtual Machine (JVM) ไฟล์คลาสสามารถดำเนินการแยกจากกันและสามารถเป็นส่วนหนึ่งของไฟล์ [JAR](/th/programming/jar/) เป็นบันเดิลร่วมกับไฟล์แพ็คเกจอื่นๆ สิ่งเหล่านี้สามารถสร้างได้โดยใช้คำสั่ง **`javac`** จากอินเตอร์เฟสบรรทัดคำสั่ง Java IDE บางตัวเช่น [Eclipse](https://www.eclipse.org/downloads/packages/release/2020-06/r/eclipse-ide-java-developers) และ NetBeans ให้สร้างไฟล์เอาต์พุต .class จาก Java ของโปรเจ็กต์ ไฟล์.

## รูปแบบไฟล์คลาส

ไฟล์คลาส Java ประกอบด้วย bytecode ซึ่งเป็นโค้ดระดับกลางที่จะรันโดย JVM ไฟล์คลาสประกอบด้วยสตรีมของไบต์ 8 บิตและรายการข้อมูลหลายไบต์จะถูกจัดเก็บไว้ในลำดับบิ๊กเอนด์เสมอ

### โครงสร้างคลาสไฟล์

โครงสร้างไฟล์คลาสแสดงไว้ด้านล่าง
```
ClassFile {
    u4             magic;
    u2             minor_version;
    u2             major_version;
    u2             constant_pool_count;
    cp_info        constant_pool[constant_pool_count-1];
    u2             access_flags;
    u2             this_class;
    u2             super_class;
    u2             interfaces_count;
    u2             interfaces[interfaces_count];
    u2             fields_count;
    field_info     fields[fields_count];
    u2             methods_count;
    method_info    methods[methods_count];
    u2             attributes_count;
    attribute_info attributes[attributes_count];
}
```
ที่ไหน:

* u1 = ปริมาณหนึ่งไบต์ที่ไม่ได้ลงนาม
* u2 = ปริมาณสองไบต์ที่ไม่ได้ลงนาม
* u4 = ปริมาณสี่ไบต์ที่ไม่ได้ลงนาม

รายละเอียดของโครงสร้างไฟล์ .class ตามที่อธิบายไว้ใน Oracle [รูปแบบไฟล์คลาส](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html) และสามารถอ้างอิงได้โดย นักพัฒนาสำหรับการอ้างอิง ข้อมูลสรุปของฟิลด์เหล่านี้มีดังนี้

* `magic` - ไอเท็มเวทย์มนตร์ให้หมายเลขเวทย์มนตร์ที่ระบุรูปแบบไฟล์คลาส มีค่าเป็น 0xCAFEBABE
* `minor_version`, `major_version` - ค่าของรายการ minor_version และ major_version คือหมายเลขรุ่นรองและรุ่นหลักของไฟล์คลาสนี้
* `constant_pool_count` - ค่าของรายการ Constant_pool_count เท่ากับจำนวนรายการในตาราง Constant_pool บวกหนึ่ง ค่าคงที่คงตัวดัชนีถือว่าถูกต้องหากมีค่ามากกว่าศูนย์และน้อยกว่าค่าคงที่คงที่ โดยมีข้อยกเว้นสำหรับค่าคงที่ประเภท long และ double
* `constant_pool[]` - Constant_pool คือตารางของโครงสร้าง (§4.4) ที่แสดงค่าคงที่ของสตริงต่างๆ ชื่อคลาสและอินเทอร์เฟซ ชื่อฟิลด์ และค่าคงที่อื่นๆ ที่อ้างถึงภายในโครงสร้าง ClassFile และโครงสร้างย่อย รูปแบบของแต่ละรายการในตาราง Constant_pool ถูกระบุด้วย "แท็ก" ไบต์แรก
* `access_flags` - ค่าของรายการ access_flags เป็นมาสก์ของแฟล็กที่ใช้เพื่อแสดงสิทธิ์การเข้าถึงและคุณสมบัติของคลาสหรืออินเทอร์เฟซนี้
* `this_class` - ค่าของไอเท็ม this_class ต้องเป็นดัชนีที่ถูกต้องในตาราง Constant_pool
* `super_class` - สำหรับคลาส ค่าของรายการ super_class ต้องเป็นศูนย์หรือต้องเป็นดัชนีที่ถูกต้องในตาราง Constant_pool
* `interfaces_count` - ค่าของรายการ interfaces_count ให้จำนวนของ super interfaces โดยตรงของคลาสหรือประเภท interface นี้
* `อินเทอร์เฟซ[]` - แต่ละค่าในอาร์เรย์อินเทอร์เฟซต้องเป็นดัชนีที่ถูกต้องในตาราง Constant_pool
* `fields_count` - ค่าของรายการ field_count แสดงจำนวนของโครงสร้าง field_info ในตารางฟิลด์
* `เขตข้อมูล[]` - แต่ละค่าในตารางเขตข้อมูลต้องเป็นโครงสร้าง field_info ที่ให้คำอธิบายที่สมบูรณ์ของเขตข้อมูลในคลาสหรืออินเทอร์เฟซนี้
* `methods_count` - ค่าของรายการ method_count แสดงจำนวนโครงสร้าง method_info ในตาราง method
* `เมธอด[]` - แต่ละค่าในตารางเมธอดต้องเป็นโครงสร้าง method_info ที่ให้คำอธิบายที่สมบูรณ์ของเมธอดในคลาสหรืออินเทอร์เฟซนี้ หากไม่มีการตั้งค่าแฟล็ก ACC_NATIVE และ ACC_ABSTRACT ในรายการ access_flags ของโครงสร้าง method_info คำสั่ง Java Virtual Machine ที่ใช้เมธอดจะถูกจัดเตรียมไว้ด้วย
* `attributes_count` - ค่าของรายการ attributes_count ระบุจำนวนของแอตทริบิวต์ (§4.7) ในตารางแอตทริบิวต์ของคลาสนี้
* `attributes[]` - แต่ละค่าของตารางแอตทริบิวต์ต้องเป็นโครงสร้าง attribute_info




## อ้างอิง

* [รูปแบบไฟล์ของคลาส](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html)

