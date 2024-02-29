{
  "date": "2021-06-17",
  "keywords": [
"DBC",
"افزونه",
"فایل dbc",
"فرمت فایل dbc",
"نوع فایل پایگاه داده",
"فرمت فایل پایگاه داده",
"فایل dbc چیست"
]،
  "author": {
    "display_name": "Muhammad Umar"
}،
  "draft": "false",
  "toc": true,
  "description": "درباره فرمت فایل DBC و APIهایی که می‌توانند فایل‌های DBC را ایجاد و باز کنند، بیاموزید.",
  "title": "DBC - فایل پایگاه داده CAN",
  "linktitle": "DBC",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-db-fac"
}
}،
  "lastmod": "2021-06-17"
}

## فایل DBC چیست؟
فایل های با پسوند dbc. به عنوان فایل های پایگاه داده CAN نیز شناخته می شوند. فایل DBC یک فایل متنی ساده است که شامل اطلاعاتی برای رمزگشایی داده های CAN bus خام به مقادیر فیزیکی یا به شکل قابل خواندن توسط انسان است. فایل DBC معرفی شده است، زیرا این روش بسیار رایج برای مدیریت شناسایی و ترجمه داده ها است. نوع فایل DBC برای فراهم کردن ابزار نگهداری سوابق همانطور که در یک شبکه CAN توضیح داده شده است توسعه داده شد.

## فرمت فایل DBC
فرمت فایل DBC فقط بخش خواندنی یا غیرفعال را نشان می دهد، و وسیله ای برای ارسال دقیق ارائه نمی دهد. برای پشتیبانی از وسایل نقلیه ای که هنوز سازگاری بومی خاصی ندارند. این کار با استفاده از نوع خودروی عمومی DBC برای استفاده از فایل‌های DBC برای ترجمه داده‌های CAN به معیارها انجام می‌شود. هر پیام در یک DBC به ساختار C تبدیل می شود که سیگنال ها اعضای ساختار C هستند.

### ساختار DBC
داده های DBC از عناصر زیر تشکیل شده است:

#### پیام DBC ساده
یک پیام DBC ساده شامل شناسه پیام و حداقل یک سیگنال است. در زیر نمایشی از یک پیام است که از یک سیگنال 8 بیتی تشکیل شده است.

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_unsigned : 0|8@1+ (1,0) [0|0] "" DBG
```
#### سیگنال های امضا شده
یک سیگنال امضا شده را می توان با اعمال یک افست منفی به یک سیگنال ارسال کرد. در زیر نمونه ای از سیگنال امضا شده به پیام قبلی آورده شده است.

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_unsigned : 0|8@1+ (1,0) [0|0] "" DBG
 SG_ IO_DEBUG_test_signed : 8|8@1- (1,-128) [0|0] "" DBG
```
#### سیگنال های کسری
یک سیگنال کسری را می توان با تعیین محدوده و دقت در صورت لزوم ارسال کرد.

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_unsigned : 0|8@1+ (1,0) [0|0] "" DBG
 SG_ IO_DEBUG_test_signed : 8|8@1- (1,-128) [0|0] "" DBG
 SG_ IO_DEBUG_test_float1 : 16|8@1+ (0.1,0) [0|0] "" DBG
 SG_ IO_DEBUG_test_float2 : 24|12@1+ (0.01,-20.48) [-20.48|20.47] "" DBG
```
#### انواع شمارش
زمانی که کاربر می خواهد به جای اعداد، نام ها را ببیند، از نوع شمارش استفاده می شود. مثال زیر را ببینید.

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_enum : 8|8@1+ (1,0) [0|0] "" DBG

BA_ "FieldType" SG_ 500 IO_DEBUG_test_enum "IO_DEBUG_test_enum";

VAL_ 500 IO_DEBUG_test_enum 2 "IO_DEBUG_test2_enum_two" 1 "IO_DEBUG_test2_enum_one" ;
```
#### پیام چندگانه
تعریف یک پیام چندگانه که از یک شناسه پیام واحد استفاده می کند یک گزینه است، با این حال، بسته به اینکه کدام مقدار چند وجهی ارسال شده است، رمزگشایی متفاوتی دارند. برای ارسال یک پیام چندگانه در زیر، یک پیام جداگانه باید ارسال شود:

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

## مثال DBC

در اینجا یک مثال کامل از یک فایل dbc آمده است:

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







## منابع ##

* [فرمت DBC] (http://socialledge.com/sjsu/index.php/DBC_Format)

* [مقدمه ای بر فایل های J1939 و DBC](https://www.kvaser.com/developer-blog/an-introduction-j1939-and-dbc-files/)


