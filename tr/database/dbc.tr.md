{
  "date" : "2021-06-17",
  "keywords" :[ "DBC", "uzantı", "dbc dosyası", "dbc dosya formatı", "Veritabanı Dosya Tipi", "Veritabanı Dosya Formatı", "dbc dosyası nedir" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"DBC dosya formatı ve DBC dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"DBC - CAN Veritabanı Dosyası",
  "linktitle" : "DBC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-17"
}

## .dbc dosyası nedir?
.dbc uzantılı dosyalar CAN veritabanı dosyaları olarak da bilinir. DBC dosyası, ham CAN veri yolu verilerinin kodunun fiziksel değerlere veya insan tarafından okunabilir biçimde çözülmesine yönelik bilgilerden oluşan basit bir metin dosyasıdır. DBC dosyası tanıtılmıştır, çünkü bu, verilerin tanımlanmasını ve çevrilmesini yönetmenin en yaygın yoludur. DBC dosya türü, bir CAN ağında açıklandığı gibi kayıt tutma araçlarını sağlamak için geliştirilmiştir.

## DBC Dosya Biçimi
DBC dosya formatı yalnızca okuma veya pasif kısmı temsil eder, iletimleri detaylandırmak için bir araç sağlamaz. Henüz belirli bir yerel uyarlaması olmayan araçları desteklemek için. Bu, CAN verilerini metriklere çevirmek üzere DBC dosyalarını kullanmak için genel DBC araç türü kullanılarak yapılır. Bir DBC'deki her mesaj, sinyallerin C yapısının üyeleri olduğu bir C yapısı haline gelir.

### DBC yapısı
DBC verileri aşağıdaki unsurlardan oluşur:

#### Basit DBC Mesajı
Basit bir DBC mesajı, Mesaj Kimliği ve en az bir sinyalden oluşur. Aşağıda, tek bir 8 bitlik sinyalden oluşan bir mesajın gösterimi yer almaktadır.

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_unsigned : 0|8@1+ (1,0) [0|0] "" DBG
```
#### İmzalı sinyaller
İşaretli bir sinyal, bir sinyale negatif ofset uygulanarak gönderilebilir. Aşağıda bir önceki mesaja imzalı sinyal örneği verilmiştir.

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_unsigned : 0|8@1+ (1,0) [0|0] "" DBG
 SG_ IO_DEBUG_test_signed : 8|8@1- (1,-128) [0|0] "" DBG
```
#### Kesirli Sinyaller
Aralığa ve gerekirse hassasiyete karar verilerek kesirli bir sinyal gönderilebilir.

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_unsigned : 0|8@1+ (1,0) [0|0] "" DBG
 SG_ IO_DEBUG_test_signed : 8|8@1- (1,-128) [0|0] "" DBG
 SG_ IO_DEBUG_test_float1 : 16|8@1+ (0.1,0) [0|0] "" DBG
 SG_ IO_DEBUG_test_float2 : 24|12@1+ (0.01,-20.48) [-20.48|20.47] "" DBG
```
#### Numaralandırma Türleri
Numaralandırma türü, kullanıcı sayıların yerine adları görmek istediğinde kullanılır. Aşağıdaki örneğe bakın.

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_enum : 8|8@1+ (1,0) [0|0] "" DBG

BA_ "FieldType" SG_ 500 IO_DEBUG_test_enum "IO_DEBUG_test_enum";

VAL_ 500 IO_DEBUG_test_enum 2 "IO_DEBUG_test2_enum_two" 1 "IO_DEBUG_test2_enum_one" ;
```
#### Çoklu Mesaj
tek bir mesaj kimliği kullanan bir çoklanmış mesajın tanımlanması bir seçenektir, ancak hangi çoklu değerin gönderildiğine bağlı olarak bunların kodu farklı şekilde çözülür. Aşağıda çoklu mesaj göndermek için ayrı bir mesaj gönderilmelidir:

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

## DBC Örneği

İşte tam bir dbc dosyası örneği:

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







## Referanslar ##

* [DBC Biçimi](http://socialledge.com/sjsu/index.php/DBC_Format)
* [J1939 ve DBC dosyalarına giriş](https://www.kvaser.com/developer-blog/an-introduction-j1939-and-dbc-files/)

