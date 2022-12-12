{
  "date" : "2021-03-11",
  "keywords" :[ "APNX", "Chỉ mục số trang của Amazon", "phần mở rộng", "tệp", "định dạng", "Sách điện tử", "Amazon Kindle" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp Amazon APNX và các API có thể tạo và mở tệp APNX.",
  "title" :"APNX - Chỉ mục số trang Amazon",
  "linktitle" : "APNX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-05-28"
}

## Tệp APNX là gì? ##

Tệp Chỉ mục Số trang Amazon sử dụng phần mở rộng .apnx là một loại tệp Sách điện tử; được sử dụng bởi Amazon Kindle. Các tệp này thực sự được gọi là tệp phân trang được sử dụng bởi các thiết bị Kindle. Vì vậy, các tệp APNX thường được tạo để đánh dấu các trang của Sách điện tử Kindle. Tính năng phân trang đã được bắt đầu trên các thiết bị Amazon Kindle kể từ phần sụn 3.1 của nó. Nó xem xét tệp APNX để tìm chỉ mục trang và sau đó ánh xạ nó với số trang trong sách in gốc. Các tệp này được lưu vào thiết bị Kindle cùng với tệp sách điện tử Amazon. Bạn không thể mở hoặc chỉnh sửa tệp APNX.

## Thông số kỹ thuật định dạng tệp APNX ##

### Cách trình bày

|byte| nội dung| bình luận|
---|---|---|
|4 |00010001 | Định dạng định danh. Giá trị của 65537 little-endian.|
|4 |bắt đầu tiếp theo | Phần bù sau vị trí kết thúc của tiêu đề đầu tiên. Bắt đầu một chuỗi thông tin tiêu đề mới|
|4 |chiều dài| Độ dài của tiêu đề đầu tiên|
|N |tiêu đề đầu tiên | Chuỗi chứa tiêu đề nội dung. Nó bắt đầu trình tự tiếp theo|
|2 |không rõ | Luôn là 1|
|2 |chiều dài | Độ dài của tiêu đề thứ hai|
|2 |số trang | Tổng số byte sau tiêu đề thứ hai đại diện cho các trang. Tổng số này bao gồm các byte bị sơ đồ trang bỏ qua.|
|2 |không rõ | Luôn luôn 32|
|N |tiêu đề thứ hai | Chuỗi chứa tiêu đề ánh xạ trang|
|4*N |phần đệm | Số đầu tiên được cung cấp trong tiêu đề ánh xạ trang cho biết số byte 0.|
|4*N |danh sách trang ||

### Tiêu đề nội dung

Tiêu đề nội dung bao gồm một chuỗi được đặt trong {} chứa các cặp khóa, giá trị:

|nội dung| bình luận|
---|---|
|nội dungGuid| hướng dẫn.|
|assin | Định danh Amazon cho phiên bản sách trên Kindle.|
|cdeType | MOBI cdeType. Phải luôn là EBOK cho sách điện tử.|
|fileRevisionId | Sửa đổi tập tin này.|

#### Thí dụ
```
{"contentGuid":"d8c14b0","asin":"B000JML5VM","cdeType":"EBOK","fileRevisionId":"1296874359405"}
```
### Tiêu đề ánh xạ trang
Tiêu đề ánh xạ trang bao gồm một chuỗi được đặt trong {} chứa các cặp khóa, giá trị.

|nội dung| bình luận|
---|---|
|assin | ISBN 10 cho cuốn sách giấy mà các trang tương ứng với|
|pageMap| Bộ ba giá trị. Có vẻ như: "(N,N,N)\
1) Số byte sau tiêu đề bắt đầu chuỗi đánh số trang\
2) không xác định\
3) không xác định\|
#### Thí dụ
```
{"asin":"1906694184","pageMap":"(4,a,1)"}
```

### Danh sách trang

Danh sách trang là một chuỗi các độ lệch trong HTML thô. Mỗi
giá trị là bắt đầu của một trang mới. Mỗi mục là một endian lớn 4 byte
int.



## Người giới thiệu

* [Định dạng tệp APNX của Amazon](https://nachtimwald.com/2011/02/09/amazon-apnx-file-format/)
* [APNX - bởi MobileRead Wiki](https://wiki.mobileread.com/wiki/APNX)

