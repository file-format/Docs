{
  "date" : "2021-06-17",
  "keywords" :[ "DBC", "phần mở rộng", "tệp dbc", "định dạng tệp dbc", "Loại tệp cơ sở dữ liệu", "Định dạng tệp cơ sở dữ liệu", "tệp dbc là gì" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp DBC và API có thể tạo và mở tệp DBC.",
  "title" :"DBC - Tệp cơ sở dữ liệu CAN",
  "linktitle" : "DBC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-17"
}

## Tệp DBC là gì?
Các tệp có phần mở rộng .dbc còn được gọi là tệp cơ sở dữ liệu CAN. Tệp DBC là một tệp văn bản đơn giản bao gồm thông tin để giải mã dữ liệu bus CAN thô thành các giá trị vật lý hoặc ở dạng con người có thể đọc được. Tệp DBC được giới thiệu vì đây là cách rất phổ biến để quản lý nhận dạng và dịch dữ liệu. Loại tệp DBC được phát triển để cung cấp phương tiện lưu giữ hồ sơ như được mô tả trong mạng CAN.

## Định dạng tệp DBC
Định dạng tệp DBC chỉ đại diện cho phần đọc hoặc thụ động, nó không cung cấp phương tiện để truyền phức tạp. Để hỗ trợ các phương tiện chưa có bản điều chỉnh riêng cụ thể. Điều này được thực hiện bằng cách sử dụng loại phương tiện DBC chung để sử dụng các tệp DBC để dịch dữ liệu CAN thành số liệu. Mỗi thông báo trong DBC trở thành cấu trúc C với các tín hiệu là thành viên của cấu trúc C.

### Cấu trúc DBC
Dữ liệu DBC bao gồm các thành phần sau:

#### Tin nhắn DBC đơn giản
Một tin nhắn DBC đơn giản bao gồm ID tin nhắn và ít nhất một tín hiệu. Sau đây là phần trình diễn của một thông báo bao gồm một tín hiệu 8 bit duy nhất.

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_unsigned : 0|8@1+ (1,0) [0|0] "" DBG
```
#### Tín hiệu đã ký
Tín hiệu đã ký có thể được gửi bằng cách áp dụng độ lệch âm cho tín hiệu. Sau đây là một ví dụ về tín hiệu đã ký cho tin nhắn trước đó.

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_unsigned : 0|8@1+ (1,0) [0|0] "" DBG
 SG_ IO_DEBUG_test_signed : 8|8@1- (1,-128) [0|0] "" DBG
```
#### Tín hiệu phân số
Tín hiệu phân đoạn có thể được gửi bằng cách quyết định phạm vi và độ chính xác nếu cần.

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_unsigned : 0|8@1+ (1,0) [0|0] "" DBG
 SG_ IO_DEBUG_test_signed : 8|8@1- (1,-128) [0|0] "" DBG
 SG_ IO_DEBUG_test_float1 : 16|8@1+ (0.1,0) [0|0] "" DBG
 SG_ IO_DEBUG_test_float2 : 24|12@1+ (0.01,-20.48) [-20.48|20.47] "" DBG
```
#### Các kiểu liệt kê
Kiểu liệt kê được sử dụng khi người dùng muốn xem tên, thay vì số. Xem ví dụ sau.

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_enum : 8|8@1+ (1,0) [0|0] "" DBG

BA_ "FieldType" SG_ 500 IO_DEBUG_test_enum "IO_DEBUG_test_enum";

VAL_ 500 IO_DEBUG_test_enum 2 "IO_DEBUG_test2_enum_two" 1 "IO_DEBUG_test2_enum_one" ;
```
#### Tin nhắn ghép kênh
xác định một tin nhắn được ghép kênh sử dụng một ID tin nhắn duy nhất là một tùy chọn, tuy nhiên, chúng được giải mã khác nhau tùy thuộc vào giá trị được ghép kênh nào được gửi. Để gửi một tin nhắn ghép kênh dưới đây, một tin nhắn riêng phải được gửi:

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

## Ví dụ DBC

Đây là một ví dụ đầy đủ về tệp dbc:

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







## Người giới thiệu ##

* [Định dạng DBC](http://socialledge.com/sjsu/index.php/DBC_Format)
* [Giới thiệu về các tệp J1939 và DBC](https://www.kvaser.com/developer-blog/an-introduction-j1939-and-dbc-files/)

