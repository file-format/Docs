{
  "date": "2021-06-17",
  "keywords": [
    "DBC",
    "extension",
    "dbc file",
    "dbc file format",
    "Database File Type",
    "Database File Format",
    "what is a dbc file"
  ],
  "author": {
    "display_name": "Muhammad Umar"
  },
  "draft": "false",
  "toc": true,
  "description": "DBC ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি DBC ফাইল তৈরি এবং খুলতে পারে।",
  "title": "DBC - CAN ডাটাবেস ফাইল",
  "linktitle": "DBC",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-dbc-bn"
    }
  },
  "lastmod": "2021-06-17"
}

## একটি DBC ফাইল কি?
.dbc এক্সটেনশন সহ ফাইলগুলি CAN ডাটাবেস ফাইল হিসাবেও পরিচিত। DBC ফাইল হল একটি সাধারণ টেক্সট ফাইল যেটিতে কাঁচা CAN বাস ডেটাকে ভৌত মান বা মানুষের পাঠযোগ্য আকারে ডিকোড করার জন্য তথ্য থাকে। ডিবিসি ফাইলটি চালু করা হয়েছে, কারণ এটি ডেটা সনাক্তকরণ এবং অনুবাদ পরিচালনা করার খুব সাধারণ উপায়। ডিবিসি ফাইলের ধরনটি একটি CAN নেটওয়ার্কে বর্ণিত রেকর্ড রাখার উপায় সরবরাহ করার জন্য তৈরি করা হয়েছিল।

## DBC ফাইল ফরম্যাট
DBC ফাইল ফরম্যাট শুধুমাত্র রিডিং বা প্যাসিভ অংশকে প্রতিনিধিত্ব করে, এটি বিস্তারিত ট্রান্সমিশন করার উপায় প্রদান করে না। যে যানবাহনগুলির এখনও একটি নির্দিষ্ট স্থানীয় অভিযোজন নেই তাদের সমর্থন করার জন্য৷ এটি মেট্রিক্সে CAN ডেটা অনুবাদ করতে DBC ফাইলগুলি ব্যবহার করার জন্য সাধারণ DBC গাড়ির ধরন ব্যবহার করে করা হয়। ডিবিসি-তে প্রতিটি বার্তা সি স্ট্রাকচারে পরিণত হয় এবং সি স্ট্রাকচারের সদস্য হয়।

### ডিবিসি কাঠামো
ডিবিসি ডেটা নিম্নলিখিত উপাদানগুলি নিয়ে গঠিত:

#### সহজ ডিবিসি বার্তা
একটি সাধারণ ডিবিসি বার্তায় মেসেজ আইডি এবং অন্তত একটি সংকেত থাকে। নিম্নলিখিত একটি বার্তার একটি প্রদর্শনী যা একটি একক 8-বিট সংকেত নিয়ে গঠিত।

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_unsigned : 0|8@1+ (1,0) [0|0] "" DBG
```
#### স্বাক্ষরিত সংকেত
একটি সংকেত একটি নেতিবাচক অফসেট প্রয়োগ করে একটি স্বাক্ষরিত সংকেত পাঠানো যেতে পারে. পূর্ববর্তী বার্তায় স্বাক্ষরিত সংকেতের একটি উদাহরণ নিম্নরূপ।

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_unsigned : 0|8@1+ (1,0) [0|0] "" DBG
 SG_ IO_DEBUG_test_signed : 8|8@1- (1,-128) [0|0] "" DBG
```
#### ভগ্নাংশ সংকেত
একটি ভগ্নাংশ সংকেত পরিসীমা নির্ধারণ করে পাঠানো যেতে পারে, এবং প্রয়োজন হলে নির্ভুলতা।

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_unsigned : 0|8@1+ (1,0) [0|0] "" DBG
 SG_ IO_DEBUG_test_signed : 8|8@1- (1,-128) [0|0] "" DBG
 SG_ IO_DEBUG_test_float1 : 16|8@1+ (0.1,0) [0|0] "" DBG
 SG_ IO_DEBUG_test_float2 : 24|12@1+ (0.01,-20.48) [-20.48|20.47] "" DBG
```
#### গণনার ধরন
ব্যবহারকারী যখন সংখ্যার পরিবর্তে নাম দেখতে চায় তখন একটি গণনার ধরন ব্যবহার করা হয়। নিম্নলিখিত উদাহরণ দেখুন.

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_enum : 8|8@1+ (1,0) [0|0] "" DBG

BA_ "FieldType" SG_ 500 IO_DEBUG_test_enum "IO_DEBUG_test_enum";

VAL_ 500 IO_DEBUG_test_enum 2 "IO_DEBUG_test2_enum_two" 1 "IO_DEBUG_test2_enum_one" ;
```
#### মাল্টিপ্লেক্সড মেসেজ
একটি একক বার্তা আইডি ব্যবহার করে এমন একটি মাল্টিপ্লেক্সযুক্ত বার্তা সংজ্ঞায়িত করা একটি বিকল্প, তবে, কোন মাল্টিপেক্সড মান পাঠানো হয়েছে তার উপর নির্ভর করে সেগুলি ভিন্নভাবে ডিকোড করা হয়। নীচে একটি মাল্টিপ্লেক্স বার্তা পাঠাতে, একটি পৃথক বার্তা পাঠাতে হবে:

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

## ডিবিসি উদাহরণ

এখানে একটি dbc ফাইলের একটি সম্পূর্ণ উদাহরণ:

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







## তথ্যসূত্র ##

* [DBC ফরম্যাট](http://socialledge.com/sjsu/index.php/DBC_Format)

* [J1939 এবং DBC ফাইলগুলির একটি ভূমিকা](https://www.kvaser.com/developer-blog/an-introduction-j1939-and-dbc-files/)


