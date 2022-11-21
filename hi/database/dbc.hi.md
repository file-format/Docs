{
  "date" : "2021-06-17",
  "keywords" :[ "डीबीसी", "एक्सटेंशन", "डीबीसी फाइल", "डीबीसी फाइल फॉर्मेट", "डेटाबेस फाइल टाइप", "डेटाबेस फाइल फॉर्मेट", "डीबीसी फाइल क्या है"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"DBC फ़ाइल स्वरूप और API के बारे में जानें जो DBC फ़ाइलें बना और खोल सकते हैं।",
  "title" :"डीबीसी - कैन डेटाबेस फाइल",
  "linktitle" : "DBC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-17"
}

## डीबीसी फाइल क्या है?
.dbc एक्सटेंशन वाली फाइलों को CAN डेटाबेस फाइल के रूप में भी जाना जाता है। डीबीसी फाइल एक साधारण टेक्स्ट फाइल है जिसमें कच्चे कैन बस डेटा को भौतिक मूल्यों या मानव पठनीय रूप में डीकोड करने के लिए जानकारी होती है। DBC फ़ाइल पेश की गई है, क्योंकि यह डेटा की पहचान और अनुवाद को प्रबंधित करने का एक बहुत ही सामान्य तरीका है। DBC फ़ाइल प्रकार को CAN नेटवर्क में वर्णित रिकॉर्ड रखने के साधन प्रदान करने के लिए विकसित किया गया था।

## डीबीसी फ़ाइल प्रारूप
डीबीसी फ़ाइल प्रारूप केवल पढ़ने या निष्क्रिय भाग का प्रतिनिधित्व करता है, यह विस्तृत प्रसारण के लिए साधन प्रदान नहीं करता है। उन वाहनों का समर्थन करने के लिए जिनके पास अभी तक कोई विशिष्ट मूल अनुकूलन नहीं है। यह डेटा को मेट्रिक्स में अनुवाद करने के लिए डीबीसी फाइलों का उपयोग करने के लिए सामान्य डीबीसी वाहन प्रकार का उपयोग करके किया जाता है। डीबीसी में प्रत्येक संदेश सी संरचना के सदस्य होने वाले संकेतों के साथ सी संरचना बन जाता है।

### डीबीसी संरचना
DBC डेटा में निम्नलिखित तत्व होते हैं:

#### सरल डीबीसी संदेश
एक साधारण डीबीसी संदेश में संदेश आईडी और कम से कम एक संकेत होता है। निम्नलिखित एक संदेश का प्रदर्शन है जिसमें एकल 8-बिट सिग्नल होता है।

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_unsigned : 0|8@1+ (1,0) [0|0] "" DBG
```
#### हस्ताक्षरित संकेत
एक संकेत के लिए एक नकारात्मक ऑफसेट लागू करके एक हस्ताक्षरित संकेत भेजा जा सकता है। पिछले संदेश के लिए हस्ताक्षरित संकेत का एक उदाहरण निम्नलिखित है।

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_unsigned : 0|8@1+ (1,0) [0|0] "" DBG
 SG_ IO_DEBUG_test_signed : 8|8@1- (1,-128) [0|0] "" DBG
```
#### भिन्नात्मक संकेत
यदि आवश्यक हो तो सीमा, और सटीकता तय करके एक भिन्नात्मक संकेत भेजा जा सकता है।

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_unsigned : 0|8@1+ (1,0) [0|0] "" DBG
 SG_ IO_DEBUG_test_signed : 8|8@1- (1,-128) [0|0] "" DBG
 SG_ IO_DEBUG_test_float1 : 16|8@1+ (0.1,0) [0|0] "" DBG
 SG_ IO_DEBUG_test_float2 : 24|12@1+ (0.01,-20.48) [-20.48|20.47] "" DBG
```
#### गणना के प्रकार
एक गणना प्रकार का उपयोग तब किया जाता है जब उपयोगकर्ता संख्याओं के बजाय नाम देखना चाहता है। निम्नलिखित उदाहरण देखें।

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_enum : 8|8@1+ (1,0) [0|0] "" DBG

BA_ "FieldType" SG_ 500 IO_DEBUG_test_enum "IO_DEBUG_test_enum";

VAL_ 500 IO_DEBUG_test_enum 2 "IO_DEBUG_test2_enum_two" 1 "IO_DEBUG_test2_enum_one" ;
```
#### बहुसंकेतन संदेश
एकल संदेश आईडी का उपयोग करने वाले बहुसंकेतक संदेशों को परिभाषित करना एक विकल्प है, हालांकि, वे अलग-अलग तरीके से डिकोड किए जाते हैं, जिसके आधार पर बहुसंकेतक मान भेजा गया था। नीचे एक बहुसंकेतक संदेश भेजने के लिए, एक अलग संदेश भेजना होगा:

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

## डीबीसी उदाहरण

यहाँ एक dbc फ़ाइल का पूरा उदाहरण दिया गया है:

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







## संदर्भ ##

* [डीबीसी प्रारूप](http://socialledge.com/sjsu/index.php/DBC_Format)
* [J1939 और DBC फाइलों का परिचय](https://www.kvaser.com/developer-blog/an-introduction-j1939-and-dbc-files/)

