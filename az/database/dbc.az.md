{
  "date": "2021-06-17",
  "keywords": [
"DBC",
"uzadılması",
"dbc faylı",
"dbc fayl formatı",
"Verilənlər bazası fayl növü",
"Verilənlər bazası fayl formatı",
"dbc faylı nədir"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "DBC faylları yarada və aça bilən DBC fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "DBC - CAN verilənlər bazası faylı",
  "linktitle": "DBC",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-db-azc"
}
},
  "lastmod": "2021-06-17"
}

## DBC faylı nədir?
.dbc uzantılı fayllar CAN verilənlər bazası faylları kimi də tanınır. DBC faylı, xam CAN avtobus məlumatlarının fiziki dəyərlərə və ya insanların oxuna biləcəyi formada deşifrə edilməsi üçün məlumatdan ibarət sadə mətn faylıdır. DBC faylı təqdim olunur, çünki bu, məlumatların identifikasiyası və tərcüməsini idarə etmək üçün çox yayılmış üsuldur. DBC fayl növü CAN şəbəkəsində təsvir olunduğu kimi qeydlərin aparılması vasitələrini təmin etmək üçün hazırlanmışdır.

## DBC fayl formatı
DBC fayl formatı yalnız oxu və ya passiv hissəni təmsil edir, ötürülmələri hazırlamaq üçün bir vasitə təmin etmir. Hələ xüsusi yerli adaptasiyası olmayan avtomobilləri dəstəkləmək üçün. Bu, CAN məlumatlarını metriklərə çevirmək üçün DBC fayllarından istifadə etmək üçün ümumi DBC avtomobil növündən istifadə etməklə edilir. DBC-dəki hər bir mesaj C strukturunun üzvləri olan siqnallarla C strukturuna çevrilir.

### DBC strukturu
DBC məlumatları aşağıdakı elementlərdən ibarətdir:

#### Sadə DBC Mesajı
Sadə DBC mesajı Mesaj ID-sindən və ən azı bir siqnaldan ibarətdir. Aşağıda tək 8 bitlik siqnaldan ibarət mesajın nümayişi verilmişdir.

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_unsigned : 0|8@1+ (1,0) [0|0] "" DBG
```
#### İmzalanmış siqnallar
İmzalanmış siqnal siqnala mənfi ofset tətbiq etməklə göndərilə bilər. Aşağıda əvvəlki mesaja imzalanmış siqnal nümunəsi verilmişdir.

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_unsigned : 0|8@1+ (1,0) [0|0] "" DBG
 SG_ IO_DEBUG_test_signed : 8|8@1- (1,-128) [0|0] "" DBG
```
#### Fraksiya Siqnalları
Fraksiya siqnalı diapazona və tələb olunarsa dəqiqliyə qərar verməklə göndərilə bilər.

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_unsigned : 0|8@1+ (1,0) [0|0] "" DBG
 SG_ IO_DEBUG_test_signed : 8|8@1- (1,-128) [0|0] "" DBG
 SG_ IO_DEBUG_test_float1 : 16|8@1+ (0.1,0) [0|0] "" DBG
 SG_ IO_DEBUG_test_float2 : 24|12@1+ (0.01,-20.48) [-20.48|20.47] "" DBG
```
#### Sadalama növləri
İstifadəçi nömrələr əvəzinə adları görmək istədikdə bir siyahı növü istifadə olunur. Aşağıdakı nümunəyə baxın.

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_enum : 8|8@1+ (1,0) [0|0] "" DBG

BA_ "FieldType" SG_ 500 IO_DEBUG_test_enum "IO_DEBUG_test_enum";

VAL_ 500 IO_DEBUG_test_enum 2 "IO_DEBUG_test2_enum_two" 1 "IO_DEBUG_test2_enum_one" ;
```
#### Çoxaldılmış Mesaj
tək mesaj identifikatorundan istifadə edən multipleksləşdirilmiş mesajların müəyyən edilməsi bir seçimdir, lakin onlar hansı multipeks dəyərinin göndərilməsindən asılı olaraq fərqli şəkildə deşifrə edilir. Aşağıdakı multipleksləşdirilmiş mesaj göndərmək üçün ayrıca mesaj göndərilməlidir:

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

## DBC nümunəsi

Budur dbc faylının tam nümunəsi:

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







## İstinadlar ##

* [DBC Format](http://socialledge.com/sjsu/index.php/DBC_Format)

* [J1939 və DBC fayllarına giriş](https://www.kvaser.com/developer-blog/an-introduction-j1939-and-dbc-files/)


