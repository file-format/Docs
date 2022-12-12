{
  "date" : "2019-12-12",
  "keywords" :[ "FBX", "file", "extension", "format", "3D File Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Hướng dẫn định dạng tệp của bạn để biết tệp FBX là gì và các API có thể tạo và mở chúng.",
  "title" :"FBX - Định dạng tệp 3D FilmBox",
  "linktitle" : "FBX",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp FBX là gì?

FBX, FilmBox, là một định dạng tệp 3D phổ biến ban đầu được Kaydara phát triển cho MotionBuilder. Nó được Autodesk Inc mua lại vào năm 2006 và hiện là một trong những định dạng trao đổi 3D chính được nhiều công cụ 3D sử dụng. FBX có sẵn ở cả định dạng tệp nhị phân và ASCII. Định dạng được thiết lập để cung cấp khả năng tương tác giữa các ứng dụng tạo nội dung kỹ thuật số. Có nhiều công cụ có sẵn để chuyển đổi từ/sang định dạng tệp FBX.

## Định dạng tệp FBX - Thông tin khác

FBX là một định dạng độc quyền và thông số kỹ thuật về định dạng tệp nhị phân của nó không có sẵn chính thức. Autodesk cung cấp C++ FBX SDK để đọc, viết và chuyển đổi sang/từ tệp FBX. Tập lệnh nhập và xuất Python cho FBX cũng có sẵn trong phần mềm Blender không sử dụng FBX SDK.

### Cấu trúc tệp dựa trên văn bản

Cấu trúc tệp dựa trên văn bản là một tài liệu có cấu trúc dạng cây với các mã định danh được đặt tên rõ ràng. Nó bao gồm một danh sách các nút lồng nhau được sắp xếp theo thứ bậc trong đó mỗi nút có:

* Mã định danh NodeType (tên lớp)
* Một bộ gồm các thuộc tính liên kết với nó, các phần tử của bộ là các kiểu dữ liệu nguyên thủy thông thường: ##float, integer, string##, v.v.
* Một danh sách chứa các nút có cùng định dạng (đệ quy).

Chúng có thể được biểu diễn một cách logic như sau:

```
NodeType: SomeProperty0a, SomeProperty0b, ... , {

 NestedNodeType1 : SomeProperty1a, ...
 NestedNodeType2 : SomeProperty2a, ... , {
 ... Sub-scope
 }

 ...
}
```

Một số nút tiêu chuẩn được định nghĩa là danh sách ẩn trong đó mỗi mục bao gồm một danh sách lồng nhau. Bất kỳ ứng dụng nào có ý định truy cập hình học FBX đều phải phân tích cú pháp các nội dung này và hiểu ý nghĩa hữu ích của nó. Một ví dụ về tệp FBX dựa trên văn bản được đưa ra dưới đây:

```
; FBX ...
; Copyright (C) 1997-2008 ...
; All rights reserved.
; ----------------------------------------------------
FBXHeaderExtension: {
    FBXHeaderVersion: 1003
    FBXVersion: 6000
    CurrentCameraResolution: {
        CameraName: "Model::Producer Perspective"
        CameraResolutionMode: "Window Size"
        CameraResolutionW: 1
        CameraResolutionH: 1
}
    CreationTimeStamp: {
    ...
}
}
;Object definitions
;------------------------------------------------------------------
Definitions: {
    Count: 2
    ObjectType: "Model" {
    Count: 2
}
}
...
```

## Cấu trúc tệp nhị phân của tệp FBX

Như đã nêu trước đó, thông số kỹ thuật định dạng tệp FBX không có sẵn công khai cho FBX. Vì Blender Foundation triển khai định dạng tệp FBX mà không sử dụng SDK do công ty cung cấp, một số chi tiết về định dạng tệp nhị phân [có sẵn](https://code.blender.org/2013/08/fbx-binary-file-format -specation/) như một phần của quá trình triển khai.

Cấu trúc tệp nhị phân tuân theo thứ tự sau:

* Tiêu đề
* Bản ghi đối tượng
* Chân trang

### Tiêu đề FBX

Thông tin tiêu đề tệp bao gồm 27 byte.

* Byte 0 - 20: Kaydara FBX Binary \x00 (tệp ma thuật, có 2 dấu cách ở cuối, sau đó là dấu kết thúc NULL).
* Byte 21 - 22: [0x1A, 0x00]## (không rõ nhưng tất cả các tệp được quan sát đều hiển thị các byte này).
* Byte 23 - 26: unsigned int, số phiên bản. 7300 cho phiên bản 7.3 chẳng hạn.

### Bản ghi đối tượng ###

Theo sau Tiêu đề là một bản ghi đối tượng là một bản ghi nút đầy đủ với tên trống và danh sách thuộc tính trống. Nó đệ quy chứa toàn bộ sự hình thành tập tin.

### Chân trang ###

Phần Chân trang FBX nằm ở cuối tệp không rõ nội dung.

## Định dạng bản ghi ##

Các bản ghi trong tệp FBX được phân loại thành:

* Bản ghi nút
* Hồ sơ tài sản

### Định dạng bản ghi nút ###

Mỗi Định dạng Bản ghi Nút được đặt tên và có cách bố trí bộ nhớ sau.


|Kích thước (Byte)|Loại ngày|Tên
--- | ---|---|
|4|UInt32|EndOffset
|4|UInt32|NumProperties
|4|UInt32|PropertyListLen
|1|UInt8|NameLen
|TênĐộ dài|char|Tên
|?|?|Property[n], trong đó n = 0:PropertyListLen
|Tùy chọn| |
|?|?|Danh sách lồng nhau
|13|uint8[]|Bản ghi Null

ở đâu:

* `EndOffset` là khoảng cách từ phần đầu của tệp đến phần cuối của bản ghi nút (tức là byte đầu tiên của bất kỳ thứ gì tiếp theo). Điều này có thể được sử dụng để dễ dàng bỏ qua các bản ghi không xác định hoặc không bắt buộc.
* `NumProperties` là số thuộc tính trong bộ giá trị được liên kết với nút. Danh sách lồng nhau là phần tử cuối cùng không được tính là thuộc tính.
* `PropertyListLen` là độ dài của danh sách thuộc tính. Đây là kích thước cần thiết để lưu trữ thuộc tính ##NumProperties##, tùy thuộc vào loại dữ liệu của thuộc tính.
* `NameLen` là độ dài của tên đối tượng, tính bằng ký tự. Trường hợp duy nhất mà đây là 0 dường như là cấp cao nhất của danh sách.
* `Name` là tên của đối tượng. Không có chấm dứt bằng không.
* `Property[n]` là thuộc tính thứ n. Đối với định dạng, hãy xem thuộc tính phần Định dạng Bản ghi. Các thuộc tính được viết tuần tự và không có phần đệm.
* `NestedList` là danh sách lồng nhau, sự hiện diện của danh sách này được biểu thị bằng bản ghi NULL–ở cuối.

Sự tồn tại của một mục nhập danh sách lồng nhau có thể được xác định bằng cách kiểm tra xem có còn byte nào cho đến khi đạt đến EndOffset hay không. Nếu vậy, bản ghi đối tượng tiếp theo sẽ được đọc ngay sau thuộc tính cuối cùng. Sau đó, bản ghi đối tượng theo sau 13 byte không, sau đó kết hợp với EndOffset. Mục đích hoặc yêu cầu của mục nhập NULL không được biết và có thể chỉ ra một số tính năng định dạng.

### Định dạng bản ghi thuộc tính ###

Bản ghi thuộc tính chứa thông tin chi tiết về các thuộc tính là một phần của Node. Một bản ghi thuộc tính có cách bố trí bộ nhớ sau:


|Kích thước (Byte)|Loại dữ liệu|Tên
--- | --- | ---
|1|char|Mã loại
|?|?|Dữ liệu

TypeCode đại diện cho các mã ký tự được sắp xếp theo nhóm yêu cầu xử lý tương tự. TypeCodes có thể được phân loại theo các loại sau và TypeCode có thể là một trong các mã ký tự trong số các loại này.

#### Các kiểu nguyên thủy ####

```
Y: 2 byte signed Integer
C: 1 bit boolean (1: true, 0: false) encoded as the LSB of a 1 Byte value.
I: 4 byte signed Integer
F: 4 byte single-precision IEEE 754 number
D: 8 byte double-precision IEEE 754 number
L: 8 byte signed Integer
```

Dữ liệu trong bản ghi kiểu vô hướng nguyên thủy chính xác là biểu diễn nhị phân của giá trị, theo thứ tự byte nhỏ về cuối.

#### Các kiểu mảng ####

```
f: Array of 4 byte single-precision IEEE 754 number
d: Array of 8 byte double-precision IEEE 754 number
l: Array of 8 byte signed Integer
i: Array of 4 byte signed Integer
b: Array of 1 byte Booleans (always 0 or 1)
```

Dữ liệu cho Kiểu mảng phức tạp hơn và có cấu trúc như sau.


|Kích thước (Byte)|Loại dữ liệu|Tên
--- | --- | ---
|4|Uint32|Độ dài mảng
|4|Uint32|Mã hóa
|4|Uint32|CompressionLength
|?|?|Nội dung

### Các loại đặc biệt ###

Sau đây là các Loại Mã Loại Đặc biệt.

```
S: String
R: raw binary data
```

Cả hai TypeCodes này được biểu diễn như sau:


|Kích thước (Byte)|Loại dữ liệu|Tên
--- | --- | ---
|4|Uin32|Độ dài
|Chiều dài| |

Chuỗi này không bị kết thúc bằng 0 và có thể chứa các ký tự \0 (điều này thực sự được sử dụng trong một số thuộc tính FBX).

## Người giới thiệu ##

* [FBX - SDK Autodesk](http://help.autodesk.com/view/FBX/2017/ENU/?guid#__files_GUID_105ED19A_9A5A_425E_BFD7_C1BBADA67AAB_htm)
* [Thông số kỹ thuật định dạng tệp nhị phân FBX](https://code.blender.org/2013/08/fbx-binary-file-format-specation/)
* [FBX - Wikipedia](https://vi.wikipedia.org/wiki/FBX#File_format)

