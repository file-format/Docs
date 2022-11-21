{
  "date" : "2021-06-17",
  "keywords" :[ "DBC", "นามสกุล", "ไฟล์ dbc", "รูปแบบไฟล์ dbc", "ประเภทไฟล์ฐานข้อมูล", "รูปแบบไฟล์ฐานข้อมูล", "ไฟล์ dbc คืออะไร" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"เรียนรู้เกี่ยวกับรูปแบบไฟล์ DBC และ API ที่สามารถสร้างและเปิดไฟล์ DBC",
  "title" :"DBC - ไฟล์ฐานข้อมูล CAN",
  "linktitle" : "DBC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-17"
}

## ไฟล์ DBC คืออะไร??
ไฟล์ที่มีนามสกุล .dbc เรียกอีกอย่างว่าไฟล์ฐานข้อมูล CAN ไฟล์ DBC เป็นไฟล์ข้อความธรรมดาที่ประกอบด้วยข้อมูลสำหรับการถอดรหัสข้อมูลดิบ CAN บัสเป็นค่าทางกายภาพหรือในรูปแบบที่มนุษย์อ่านได้ มีการแนะนำไฟล์ DBC เนื่องจากเป็นวิธีทั่วไปในการจัดการการระบุตัวตนและการแปลข้อมูล ประเภทไฟล์ DBC ได้รับการพัฒนาเพื่อให้วิธีการเก็บบันทึกตามที่อธิบายไว้ในเครือข่าย CAN

## รูปแบบไฟล์ DBC
รูปแบบไฟล์ DBC แสดงเฉพาะส่วนการอ่านหรือพาสซีฟเท่านั้น ไม่มีวิธีในการส่งรายละเอียดเพิ่มเติม เพื่อรองรับยานพาหนะที่ยังไม่มีการปรับแต่งแบบเนทีฟโดยเฉพาะ สิ่งนี้ทำได้โดยใช้ประเภทยานพาหนะ DBC ทั่วไปเพื่อใช้ไฟล์ DBC เพื่อแปลข้อมูล CAN เป็นเมตริก แต่ละข้อความใน DBC จะกลายเป็นโครงสร้าง C โดยมีสัญญาณเป็นสมาชิกของโครงสร้าง C

### โครงสร้าง DBC
ข้อมูล DBC ประกอบด้วยองค์ประกอบต่อไปนี้:

#### ข้อความ DBC อย่างง่าย
ข้อความ DBC อย่างง่ายประกอบด้วยรหัสข้อความและสัญญาณอย่างน้อยหนึ่งรายการ ต่อไปนี้เป็นการสาธิตข้อความที่ประกอบด้วยสัญญาณ 8 บิตเดียว

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_unsigned : 0|8@1+ (1,0) [0|0] "" DBG
```
#### สัญญาณที่ลงนาม
สามารถส่งสัญญาณที่ลงนามได้โดยใช้การชดเชยเชิงลบกับสัญญาณ ต่อไปนี้คือตัวอย่างสัญญาณที่ลงนามไปยังข้อความก่อนหน้า

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_unsigned : 0|8@1+ (1,0) [0|0] "" DBG
 SG_ IO_DEBUG_test_signed : 8|8@1- (1,-128) [0|0] "" DBG
```
#### สัญญาณเศษส่วน
สามารถส่งสัญญาณเศษส่วนได้โดยกำหนดช่วงและความแม่นยำหากจำเป็น

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_unsigned : 0|8@1+ (1,0) [0|0] "" DBG
 SG_ IO_DEBUG_test_signed : 8|8@1- (1,-128) [0|0] "" DBG
 SG_ IO_DEBUG_test_float1 : 16|8@1+ (0.1,0) [0|0] "" DBG
 SG_ IO_DEBUG_test_float2 : 24|12@1+ (0.01,-20.48) [-20.48|20.47] "" DBG
```
#### ประเภทการแจงนับ
ชนิดการแจงนับจะใช้เมื่อผู้ใช้ต้องการดูชื่อ แทนตัวเลข ดูตัวอย่างต่อไปนี้

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_enum : 8|8@1+ (1,0) [0|0] "" DBG

BA_ "FieldType" SG_ 500 IO_DEBUG_test_enum "IO_DEBUG_test_enum";

VAL_ 500 IO_DEBUG_test_enum 2 "IO_DEBUG_test2_enum_two" 1 "IO_DEBUG_test2_enum_one" ;
```
#### ข้อความแบบมัลติเพล็กซ์
การกำหนดข้อความมัลติเพล็กซ์ที่ใช้ ID ข้อความเดียวเป็นตัวเลือก อย่างไรก็ตาม ข้อความเหล่านี้จะถูกถอดรหัสแตกต่างกันไป ขึ้นอยู่กับค่ามัลติเพล็กซ์ที่ส่ง ในการส่งข้อความแบบมัลติเพล็กซ์ด้านล่าง จะต้องส่งข้อความแยกต่างหาก:

```
BO_ 200 SENSOR_SONARS: 8 SENSOR
 SG_ SENSOR_SONARS_mux M : 0|4@1+ (1,0) [0|0] "" DRIVER,IO
 SG_ SENSOR_SONARS_err_count : 4|12@1+ (1,0) [0|0] "" DRIVER,IO
 SG_ SENSOR_SONARS_left m0 : 16|12@1+ (0.1,0) [0|0] "" DRIVER,IO
 SG_ SENSOR_SONARS_middle m0 : 28|12@1+ (0.1,0) [0|0] "" DRIVER,IO
 SG_ SENSOR_SONARS_right m0 : 40|12@1+ (0.1,0) [0|0] "" DRIVER,IO
 SG_ SENSOR_SONARS_rear m0 : 52|12@1+ (0.1,0) [0|0] "" DRIVER,IO
 SG_ SENSOR_SONARS_no_filt_left m1 : 16|12@1+ (0.1,0) [0|0] "" DBG
 SG_ SENSOR_SONARS_no_filt_middle m1 : 28|12@1+ (0.1,0) [0|0] "" DBG
 SG_ SENSOR_SONARS_no_filt_right m1 : 40|12@1+ (0.1,0) [0|0] "" DBG
 SG_ SENSOR_SONARS_no_filt_rear m1 : 52|12@1+ (0.1,0) [0|0] "" DBG
```

## ตัวอย่าง DBC

นี่คือตัวอย่างที่สมบูรณ์ของไฟล์ dbc:

```
VERSION ""

NS_ :
	BA_
	BA_DEF_
	BA_DEF_DEF_
	BA_DEF_DEF_REL_
	BA_DEF_REL_
	BA_DEF_SGTYPE_
	BA_REL_
	BA_SGTYPE_
	BO_TX_BU_
	BU_BO_REL_
	BU_EV_REL_
	BU_SG_REL_
	CAT_
	CAT_DEF_
	CM_
	ENVVAR_DATA_
	EV_DATA_
	FILTER
	NS_DESC_
	SGTYPE_
	SGTYPE_VAL_
	SG_MUL_VAL_
	SIGTYPE_VALTYPE_
	SIG_GROUP_
	SIG_TYPE_REF_
	SIG_VALTYPE_
	VAL_
	VAL_TABLE_

BS_:

BU_: DBG DRIVER IO MOTOR SENSOR


BO_ 100 DRIVER_HEARTBEAT: 1 DRIVER
 SG_ DRIVER_HEARTBEAT_cmd : 0|8@1+ (1,0) [0|0] "" SENSOR,MOTOR

BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_unsigned : 0|8@1+ (1,0) [0|0] "" DBG
 SG_ IO_DEBUG_test_enum : 8|8@1+ (1,0) [0|0] "" DBG
 SG_ IO_DEBUG_test_signed : 16|8@1- (1,0) [0|0] "" DBG
 SG_ IO_DEBUG_test_float : 24|8@1+ (0.5,0) [0|0] "" DBG

BO_ 101 MOTOR_CMD: 1 DRIVER
 SG_ MOTOR_CMD_steer : 0|4@1- (1,-5) [-5|5] "" MOTOR
 SG_ MOTOR_CMD_drive : 4|4@1+ (1,0) [0|9] "" MOTOR

BO_ 400 MOTOR_STATUS: 3 MOTOR
 SG_ MOTOR_STATUS_wheel_error : 0|1@1+ (1,0) [0|0] "" DRIVER,IO
 SG_ MOTOR_STATUS_speed_kph : 8|16@1+ (0.001,0) [0|0] "kph" DRIVER,IO

BO_ 200 SENSOR_SONARS: 8 SENSOR
 SG_ SENSOR_SONARS_mux M : 0|4@1+ (1,0) [0|0] "" DRIVER,IO
 SG_ SENSOR_SONARS_err_count : 4|12@1+ (1,0) [0|0] "" DRIVER,IO
 SG_ SENSOR_SONARS_left m0 : 16|12@1+ (0.1,0) [0|0] "" DRIVER,IO
 SG_ SENSOR_SONARS_middle m0 : 28|12@1+ (0.1,0) [0|0] "" DRIVER,IO
 SG_ SENSOR_SONARS_right m0 : 40|12@1+ (0.1,0) [0|0] "" DRIVER,IO
 SG_ SENSOR_SONARS_rear m0 : 52|12@1+ (0.1,0) [0|0] "" DRIVER,IO
 SG_ SENSOR_SONARS_no_filt_left m1 : 16|12@1+ (0.1,0) [0|0] "" DBG
 SG_ SENSOR_SONARS_no_filt_middle m1 : 28|12@1+ (0.1,0) [0|0] "" DBG
 SG_ SENSOR_SONARS_no_filt_right m1 : 40|12@1+ (0.1,0) [0|0] "" DBG
 SG_ SENSOR_SONARS_no_filt_rear m1 : 52|12@1+ (0.1,0) [0|0] "" DBG




CM_ BU_ DRIVER "The driver controller driving the car";
CM_ BU_ MOTOR "The motor controller of the car";
CM_ BU_ SENSOR "The sensor controller of the car";
CM_ BO_ 100 "Sync message used to synchronize the controllers";

BA_DEF_ "BusType" STRING ;
BA_DEF_ BO_ "GenMsgCycleTime" INT 0 0;
BA_DEF_ SG_ "FieldType" STRING ;

BA_DEF_DEF_ "BusType" "CAN";
BA_DEF_DEF_ "FieldType" "";
BA_DEF_DEF_ "GenMsgCycleTime" 0;

BA_ "GenMsgCycleTime" BO_ 100 1000;
BA_ "GenMsgCycleTime" BO_ 500 100;
BA_ "GenMsgCycleTime" BO_ 101 100;
BA_ "GenMsgCycleTime" BO_ 400 100;
BA_ "GenMsgCycleTime" BO_ 200 100;
BA_ "FieldType" SG_ 100 DRIVER_HEARTBEAT_cmd "DRIVER_HEARTBEAT_cmd";
BA_ "FieldType" SG_ 500 IO_DEBUG_test_enum "IO_DEBUG_test_enum";


VAL_ 100 DRIVER_HEARTBEAT_cmd 2 "DRIVER_HEARTBEAT_cmd_REBOOT" 1 "DRIVER_HEARTBEAT_cmd_SYNC" 0 "DRIVER_HEARTBEAT_cmd_NOOP" ;
VAL_ 500 IO_DEBUG_test_enum 2 "IO_DEBUG_test2_enum_two" 1 "IO_DEBUG_test2_enum_one" ;

```







## อ้างอิง ##

* [รูปแบบ DBC](http://socialledge.com/sjsu/index.php/DBC_Format)
* [ข้อมูลเบื้องต้นเกี่ยวกับไฟล์ J1939 และ DBC](https://www.kvaser.com/developer-blog/an-introduction-j1939-and-dbc-files/)

