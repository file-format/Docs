{
  "date" : "2019-10-11",
  "keywords" :[ "yaml", ".yaml","tệp yaml là gì","cách mở tệp yaml", "phần mở rộng", "tệp", "tệp yaml","định dạng tệp yaml", "phần mở rộng .yaml" , "yaml vs json" ,"ví dụ về tệp YAML", "ví dụ về tệp docker yaml"],
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "description" :" Tìm hiểu về định dạng tệp YAML và API có thể tạo và mở tệp YAML.",
  "title" :"Định dạng tệp YAML",
  "linktitle" : "YAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-05"
}

## Tệp YAML là gì? ##

**Tệp YAML** bao gồm một ngôn ngữ YAML (YAML Ain't Markup Language) là ngôn ngữ tuần tự hóa dữ liệu dựa trên Unicode; được sử dụng cho các tệp cấu hình, nhắn tin trên internet, tính bền vững của đối tượng, v.v. YAML sử dụng phần mở rộng .yaml cho các tệp của nó. Cú pháp của nó độc lập với một ngôn ngữ lập trình cụ thể. Về cơ bản, YAML được thiết kế để tương tác với con người và hoạt động tốt với các ngôn ngữ lập trình hiện đại. Hỗ trợ tuần tự hóa các cấu trúc dữ liệu gốc tùy ý đã tăng khả năng đọc của các tệp YAML, nhưng nó làm cho quá trình tạo tệp và phân tích cú pháp trở nên phức tạp một chút.

## Lược Sử ##

YAML lần đầu tiên được đề xuất vào năm 2001 và được phát triển bởi Clark Evans, Ingy döt Net và Oren Ben-Kiki. YAML lần đầu tiên được cho là có nghĩa là "Yet Another Markup Language" để biểu thị mục đích của nó là một ngôn ngữ đánh dấu. Sau đó, nó được thay đổi mục đích thành "Ngôn ngữ đánh dấu YAML Aint" để biểu thị mục đích của nó là hướng dữ liệu.


## Định dạng tệp YAML ##

Tệp YAML bao gồm các loại dữ liệu sau

- **Scalars**: Scalars là các giá trị như Strings, Integers, Booleans, v.v.
- **Sequences**: Sequences là danh sách với mỗi mục bắt đầu bằng dấu gạch nối (-). Danh sách cũng có thể được lồng vào nhau.
- **Ánh xạ**: Ánh xạ cung cấp khả năng liệt kê các khóa có giá trị.

### Cú pháp ###

- **Khoảng trắng**: Thụt đầu dòng khoảng trắng được sử dụng để biểu thị cấu trúc lồng nhau và tổng thể.

```yaml
tên: John Smith
tiếp xúc:
nhà: 1012355532
văn phòng: 5002586256
địa chỉ:
đường phố: |
Ngõ Lốc Xoáy 123
Phòng 16
thành phố: East Centerville
tiểu bang: KS
```

- **Nhận xét**: Nhận xét được viết bắt đầu bằng ký hiệu "#".

```yaml
# Đây là một bình luận YAML
```

- **Danh sách**: Dấu gạch nối (-) được sử dụng để chỉ các thành viên trong danh sách với mỗi thành viên trên một dòng riêng biệt. Danh sách thành viên cũng có thể được đặt trong dấu ngoặc vuông ([...]) với các thành viên được phân tách bằng dấu phẩy (,).

```yaml
  - A
  - B
  - C
```

```yaml
[A, B, C]
```

- **Mảng kết hợp**: Mảng kết hợp được bao quanh bởi dấu ngoặc nhọn ({...}). Các khóa và giá trị được phân tách bằng dấu hai chấm (:) và mỗi cặp được phân tách bằng dấu phẩy (,).

```yaml
  {name: John Smith, age: 20}
```

- **Chuỗi**: Chuỗi có thể được viết có hoặc không có dấu nháy kép (") hoặc dấu nháy đơn (').

```yaml
chuỗi mẫu
"Chuỗi mẫu"
'Chuỗi mẫu'
```

- **Nội dung khối vô hướng**: Nội dung vô hướng có thể được viết bằng ký hiệu khối bằng cách sử dụng như sau:
  - **|**: All live breaks are significant.
  - **>**: Each line break is folded to space. It removes the leading whitespace for each line.

```yaml
dữ liệu: |
YAML
(YAML không phải là ngôn ngữ đánh dấu)
là một ngôn ngữ tuần tự hóa dữ liệu
```

```yaml
dữ liệu: ?
YAML (YAML không phải là ngôn ngữ đánh dấu)
là một ngôn ngữ tuần tự hóa dữ liệu
```

- **Nhiều tài liệu**: Nhiều tài liệu được phân tách bằng ba dấu gạch ngang (---) trong một luồng. Dấu gạch ngang cho biết phần đầu của tài liệu. Dấu gạch nối cũng được sử dụng để tách các chỉ thị khỏi nội dung tài liệu. Phần cuối của văn bản được biểu thị bằng dấu ba chấm (...).

```yaml
  ---
Tài liệu 1
  ---
Tài liệu 2
...
```

- **Type**: Để chỉ định loại giá trị, sử dụng dấu chấm than kép (!!).

```yaml
một: !!phao 123
b:!!str 123
```

- **Thẻ**: Để gán thẻ cho một ghi chú, dấu và (&) được sử dụng và để tham chiếu nút đó, dấu hoa thị (*) được sử dụng.

```yaml
tên: John Smith
hóa đơn đến: &id01
đường phố: |
Ngõ Lốc Xoáy 123
Phòng 16
thành phố: East Centerville
tiểu bang: KS

gửi đến: *id01
```

- **Chỉ thị**: Các tài liệu YAML có thể được đặt trước các chỉ thị trong một luồng. Chỉ thị bắt đầu bằng dấu phần trăm (%) theo sau là tên và sau đó là các tham số được phân tách bằng dấu cách.

```yaml
%YAML 1.2
  ---
Nội dung tài liệu
```
## Ví dụ về tệp YAML
Tại đây, bạn có thể xem **ví dụ về tệp docker yaml** bên dưới:

```
topology:
database_node_name: docker_controller
docker_controller_node_name: docker_controller
self_service_portal_node_name: docker_controller
kvm_compute_node_names: kvm_compute1
docker_compute_node_names: docker_compute1
```

## YAML so với JSON
Về cơ bản, cả JSON và YAML đều được phát triển để cung cấp định dạng trao đổi dữ liệu mà con người có thể đọc được. YAML được hiện thực hóa dưới dạng siêu định dạng JSON. Điều đó có nghĩa là chúng ta có thể phân tích cú pháp JSON bằng trình phân tích cú pháp YAML. Mặc dù việc thực hiện lý thuyết này trong thực tế là một chút khó khăn. Do đó, một số khác biệt cơ bản giữa YAML và JSON được đưa ra dưới đây:

|YAML| JSON|
---|---|
|Quá trình phân tích cú pháp dữ liệu tuần tự hóa phức tạp và tốn thời gian |Phân tích dữ liệu tuần tự hóa JSON nhanh chóng và dễ dàng với thiết kế đơn giản hơn|
|Ít hỗ trợ từ cộng đồng| Hỗ trợ cộng đồng lớn hơn và phổ biến |
|Hỗ trợ bình luận| Không hỗ trợ bình luận|
|Khả năng sử dụng tham chiếu các đối tượng dữ liệu khác| Không thể tuần tự hóa các cấu trúc phức tạp với các tham chiếu đối tượng |
|Hệ thống phân cấp được biểu thị bằng cách sử dụng các ký tự dấu cách kép. Ký tự tab không được phép|Đối tượng và Mảng được biểu thị trong dấu ngoặc nhọn và dấu ngoặc vuông.|
|Dấu ngoặc kép của chuỗi là tùy chọn nhưng nó hỗ trợ dấu ngoặc đơn và dấu ngoặc kép.|Chuỗi phải nằm trong dấu ngoặc kép.|
|Nút gốc có thể là bất kỳ kiểu dữ liệu hợp lệ nào|Nút gốc phải là một mảng hoặc một đối tượng.|


## Người giới thiệu ##

- [YAML - Wikipedia](https://vi.wikipedia.org/wiki/YAML)
- [YAML](https://yaml.org/spec/1.2/spec.html)

