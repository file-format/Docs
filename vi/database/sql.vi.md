{
  "date" : "2020-11-11",
  "keywords" :[ "SQL", "phần mở rộng", "tệp", "định dạng tệp", "Loại tệp cơ sở dữ liệu", "Định dạng tệp cơ sở dữ liệu", "Tệp cơ sở dữ liệu" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp SQL và API có thể tạo và mở tệp SQL.",
  "title" :"Định dạng tệp SQL - Tệp dữ liệu ngôn ngữ truy vấn có cấu trúc",
  "linktitle" : "SQL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Tệp SQL là gì?

Tệp có phần mở rộng .sql là tệp Ngôn ngữ truy vấn có cấu trúc (SQL) chứa mã để hoạt động với cơ sở dữ liệu quan hệ. Nó được sử dụng để viết các câu lệnh SQL cho các hoạt động CRUD (Tạo, Đọc, Cập nhật và Xóa) trên cơ sở dữ liệu. Các tệp SQL phổ biến khi làm việc với máy tính để bàn cũng như cơ sở dữ liệu dựa trên web. Có một số lựa chọn thay thế cho SQL, chẳng hạn như Java Persistence Query Language (JPQL), LINQ, HTSQL, 4D QL và một số ngôn ngữ khác. Các tệp SQL có thể được mở bằng trình chỉnh sửa truy vấn của Microsoft SQL Server, MySQL và các trình soạn thảo văn bản thuần túy khác như Notepad trên HĐH Windows.

## Tóm tắt lịch sử

* Do Donal D. Chamberlin và Raymond F. Boyce tại IBM phát triển và giới thiệu vào đầu những năm 1970
* Được sử dụng để lưu trữ và truy xuất dữ liệu từ hệ thống quản lý cơ sở dữ liệu bán quan hệ ban đầu của IBM, System R
* Bắt đầu được sử dụng trong cơ sở các sản phẩm thương mại dựa trên nguyên mẫu System R của họ bao gồm System/38, SQL/DS và DB2, được bán trên thị trường lần lượt vào năm 1979, 1981 và 1983.
* Chính thức được các nhóm tiêu chuẩn ANSI và ISO áp dụng làm tiêu chuẩn "Ngôn ngữ cơ sở dữ liệu SQL" cho các hệ thống quản lý cơ sở dữ liệu quan hệ (RDBMS) vào năm 1986

## Định dạng tệp SQL

Các tệp SQL ở định dạng văn bản thuần túy và có thể bao gồm một số thành phần ngôn ngữ. Nhiều câu lệnh có thể được thêm vào một tệp SQL nếu việc thực thi chúng có thể thực hiện được mà không phụ thuộc vào nhau. Các lệnh SQL này có thể được thực thi bởi trình soạn thảo truy vấn để thực hiện các thao tác CRUD.

### Phần tử ngôn ngữ SQL

Các phần tử ngôn ngữ SQL như được liệt kê dưới đây.

|Phần tử|Mô tả|
---|---|
|mệnh đề| Các thành phần cấu thành của câu lệnh và truy vấn.|
|Biểu thức| Có thể tạo ra giá trị vô hướng hoặc bảng bao gồm các cột và hàng dữ liệu|
|Vị ngữ| Chỉ định các điều kiện có thể được ước tính thành logic ba giá trị SQL (3VL) (đúng/sai/không xác định) hoặc giá trị chân lý Boolean và được sử dụng để hạn chế tác động của các câu lệnh và truy vấn hoặc để thay đổi luồng chương trình.|
|Truy vấn| Truy xuất dữ liệu dựa trên các tiêu chí cụ thể. Đây là một thành phần quan trọng của SQL.|
|Báo cáo| Có thể có ảnh hưởng lâu dài đến sơ đồ và dữ liệu hoặc có thể kiểm soát các giao dịch, luồng chương trình, kết nối, phiên hoặc chẩn đoán.|

### Ví dụ SQL
Câu lệnh SQL sau đây tạo một bảng có tên **DATA**, theo sau là các lệnh `INSERT` bổ sung để chèn các bản ghi vào bảng này.
```
CREATE TABLE DATA
(ID INTEGER REFERENCES STATION(ID),
MONTH INTEGER CHECK (MONTH BETWEEN 1 AND 12),
TEMP_F REAL CHECK (TEMP_F BETWEEN -80 AND 150),
RAIN_I REAL CHECK (RAIN_I BETWEEN 0 AND 100),
PRIMARY KEY (ID, MONTH));
```
```
INSERT INTO STATS VALUES (23, 1, 57.4, 0.31);
INSERT INTO STATS VALUES (21, 7, 91.7, 5.15);
INSERT INTO STATS VALUES (45, 1, 27.3, 0.18);
INSERT INTO STATS VALUES (65, 7, 74.8, 2.11);
INSERT INTO STATS VALUES (78, 1, 6.7, 2.10);
INSERT INTO STATS VALUES (88, 7, 65.8, 4.52);
```

## Người giới thiệu ##

* [SQL của Wikipedia](https://en.wikipedia.org/wiki/SQL)
* [Cú pháp SQL](https://en.wikipedia.org/wiki/SQL_syntax)

