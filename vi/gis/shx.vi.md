{
  "date" : "2021-07-29",
  "keywords" :[ "tệp shx", "định dạng tệp shx", "tệp shx là gì", "tệp", "ví dụ shx", "phần mở rộng tệp shx","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHX - Định dạng Chỉ mục Hình dạng Shapefile",
  "description":"Tìm hiểu về định dạng tệp SHX và các API có thể tạo và mở tệp SHX.",
  "linktitle" : "SHX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## Tệp SHX là gì?
Tệp SHX thuộc định dạng chỉ mục hình dạng, là chỉ mục vị trí của hình học đối tượng để cho phép tìm kiếm tiến và lùi nhanh chóng. SHX là tệp bù trừ truy cập trực tiếp. Không có dữ liệu trong tệp này, chỉ có một bản sao của hàng trăm byte đầu tiên, số bản ghi và phần bù cho byte bắt đầu của bản ghi đó trong tệp shp. Xin lưu ý rằng tệp có phần mở rộng .shx không liên kết [SHP](/vi/gis/shp/) và [DBF](/vi/database/dbf/).

## Định dạng tệp SHX
Định dạng SHX chứa chỉ mục vị trí của hình dạng đối tượng và tiêu đề 100 byte tương tự như tệp SHP, theo sau là bất kỳ số bản ghi độ dài cố định 8 byte nào chứa hai trường sau:
| byte | Loại | Độ bền | Cách sử dụng |
-------|-------|------------|---------------------------------|
| 0–3 | int32 | lớn | Bản ghi offset (bằng từ 16 bit) |
| 4–7 | int32 | lớn | Độ dài bản ghi (bằng từ 16 bit) |

Chỉ mục này cho phép tìm kiếm ngược trong shapefile bằng cách, trước tiên, tìm kiếm ngược trong chỉ mục hình dạng và sau đó đọc phần bù bản ghi. Phần bù đó có thể được sử dụng để tìm đến vị trí chính xác trong tệp SHP. Bạn cũng có thể tìm kiếm chuyển tiếp; một số lượng bản ghi tùy ý sử dụng cùng một phương pháp. Mặc dù, có thể tạo chỉ mục hoàn chỉnh cùng với tệp SHP, nhưng nó có thể làm tăng cơ hội khiến tệp SHP bị hỏng nhanh chóng.


## Người giới thiệu

* [Shapefile - theo Wikipedia)](https://vi.wikipedia.org/wiki/Shapefile)


