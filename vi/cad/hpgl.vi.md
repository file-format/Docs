{
  "date" : "2020-07-28",
  "keywords" :[ "HPGL", "Định dạng tệp", "Mở", "Đọc", "Tạo", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp HPGL và API có thể tạo và mở tệp HPGL.",
  "title" :"Định dạng tệp HPGL - Học hỏi từ các chuyên gia định dạng tệp!",
  "linktitle" : "HPGL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## Tệp HPGL là gì?

Tệp HPGFL (Ngôn ngữ đồ họa Hewlett-Packard) chứa tập lệnh điều khiển máy vẽ do HP phát triển. Máy vẽ HP sử dụng tệp này để vẽ và in nội dung vectơ và raster trên giấy.

### Lệnh HPGL

Một lệnh HPGL bao gồm như sau.
* Một phần lệnh của bảng chữ cái gồm hai ký tự
* Một phần tham số
* Phần Kẻ hủy diệt

Mỗi tham số trong tệp phải được phân chia bằng dấu phân cách trong trường hợp có nhiều tham số.

### Lệnh HPGL Ví dụ

```
Example :PA5000,1000;
  (command)    PA
  (parameter)  5000
  (separator)  ,
  (parameter)  1000
  (terminator) ;
```

### Hệ tọa độ

Các hệ thống tọa độ bao gồm các chỉ báo đo lường 2 chiều để định vị bất kỳ vị trí cụ thể nào. HPGL sử dụng cả hệ tọa độ Plotter và hệ tọa độ người dùng cho mục đích này.

#### Hệ tọa độ máy vẽ

Hệ tọa độ này được sử dụng để vẽ các bản vẽ dựa trên chuyển động của máy vẽ. Một đơn vị XY điển hình của chuyển động tối thiểu của máy vẽ là 0,025mm. Phạm vi vẽ có thể thay đổi với các loại máy vẽ.

#### Hệ tọa độ người dùng

Hệ tọa độ do người dùng chỉ định có thể được thiết lập bằng cách sử dụng tỷ lệ và gốc tọa độ. Chúng được chuyển đổi thành tọa độ máy vẽ bằng cách sử dụng lệnh IP và lệnh SC. Các tọa độ hệ thống máy vẽ được sử dụng theo mặc định nếu việc chuyển đổi này không được thực hiện.

## Định dạng tệp HPGL
Các tệp HPGL ở định dạng ASCII (tệp văn bản) và bắt đầu bằng một vài lệnh thiết lập. Điều này thiết lập các tham số nhất định cho máy vẽ để vẽ đồ thị. Một tệp HPGL điển hình trông như sau.

|Lệnh|Ý nghĩa
---|---|
|IN;|khởi tạo, bắt đầu công việc vẽ đồ thị|
|IP;|đặt các điểm chia tỷ lệ (P1 và P2) về vị trí mặc định của chúng|
|SP1;|chọn bút 1|
|PU0,0;|nhấc Bút lên và di chuyển đến điểm bắt đầu cho hành động tiếp theo|
|PD100,0,100,100,0,100,0,0;|đặt Bút xuống và di chuyển đến các vị trí sau (vẽ một hộp xung quanh trang)|
|PU50,50;|Pen Up và di chuyển đến tọa độ X,Y 50,50|
|CI25;|vẽ đường tròn có bán kính 25|
|SS;|chọn bộ ký tự chuẩn|
|DT*,1;|đặt dấu phân cách văn bản thành dấu hoa thị và không in chúng (số 1, nghĩa là "đúng")|
|PU20,80;|nhấc bút và di chuyển đến 20,80|
|LBXin chào thế giới*;|vẽ nhãn|

## Người giới thiệu
* [HPGL của Wikipedia](https://vi.wikipedia.org/wiki/HP-GL)
* [Hướng dẫn tham khảo HPGL](https://www.isoplotec.co.jp/HPGL/eHPGL.htm)

