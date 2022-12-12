{
  "date" : "2019-10-11",
  "keywords" :[ "lớp", ".class","tệp lớp là gì","cách mở tệp lớp", "phần mở rộng", "tệp", "tệp lớp","định dạng tệp lớp", "phần mở rộng .class ", "tệp lớp trong java" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Lớp - Định dạng tệp lớp Java",
  "description":"Tìm hiểu về định dạng tệp Lớp học và các API có thể tạo và mở tệp Lớp học.",
  "linktitle" : "Class",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Tệp lớp là gì?

**Tệp lớp trong Java** là đầu ra được biên dịch của lớp [.java](/vi/programming/java/) thực sự được thực thi bởi Máy ảo Java (JVM). Các tệp lớp có thể được thực thi riêng lẻ cũng như có thể là một phần của tệp [JAR](/vi/programming/jar/) dưới dạng một gói cùng với các tệp gói khác. Chúng có thể được tạo bằng lệnh **`javac`** từ giao diện dòng lệnh. Một số Java IDE như [Eclipse](https://www.eclipse.org/downloads/packages/release/2020-06/r/eclipse-ide-java-developers) và NetBeans cung cấp khả năng tạo tệp đầu ra .class từ Java của dự án các tập tin.

## Định dạng tệp lớp

Tệp lớp Java bao gồm mã byte là mã trung gian được chạy bởi JVM. Tệp lớp bao gồm một luồng byte 8 bit và các mục dữ liệu nhiều byte luôn được lưu trữ theo thứ tự lớn-endian.

### Cấu trúc tệp lớp

Cấu trúc tệp lớp như được hiển thị bên dưới.
```
ClassFile {
    u4             magic;
    u2             minor_version;
    u2             major_version;
    u2             constant_pool_count;
    cp_info        constant_pool[constant_pool_count-1];
    u2             access_flags;
    u2             this_class;
    u2             super_class;
    u2             interfaces_count;
    u2             interfaces[interfaces_count];
    u2             fields_count;
    field_info     fields[fields_count];
    u2             methods_count;
    method_info    methods[methods_count];
    u2             attributes_count;
    attribute_info attributes[attributes_count];
}
```
ở đâu:

* u1 = số lượng một byte không dấu
* u2 = số lượng hai byte không dấu
* u4 = số lượng bốn byte không dấu

Chi tiết về cấu trúc tệp .class cũng được giải thích trong Oracle [định dạng tệp lớp](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html) và có thể được giới thiệu bởi nhà phát triển để tham khảo. Một bản tóm tắt của các lĩnh vực này như sau.

* `ma thuật` - Vật phẩm ma thuật cung cấp số ma thuật xác định định dạng tệp lớp; nó có giá trị 0xCAFEBABE.
* `minor_version`, `major_version` - Giá trị của các mục Minor_version và major_version là số phiên bản phụ và chính của tệp lớp này.
* `constant_pool_count` - Giá trị của mục constant_pool_count bằng với số mục trong bảng hằng_pool cộng thêm một. Chỉ số hằng_pool được coi là hợp lệ nếu nó lớn hơn 0 và nhỏ hơn hằng_pool_count, ngoại trừ các hằng số thuộc loại long và double.
* `constant_pool[]` - Hằng_pool là một bảng gồm các cấu trúc (§4.4) đại diện cho các hằng số chuỗi, tên lớp và giao diện, tên trường và các hằng số khác được tham chiếu trong cấu trúc ClassFile và các cấu trúc con của nó. Định dạng của mỗi mục trong bảng constant_pool được biểu thị bằng byte "thẻ" đầu tiên của nó.
* `access_flags` - Giá trị của mục access_flags là mặt nạ của các cờ được sử dụng để biểu thị quyền truy cập và thuộc tính của lớp hoặc giao diện này.
* `this_class` - Giá trị của mục this_class phải là một chỉ mục hợp lệ trong bảng hằng_pool.
* `super_class` - Đối với một lớp, giá trị của mục super_class phải bằng 0 hoặc phải là một chỉ mục hợp lệ trong bảng hằng số.
* `interfaces_count` - Giá trị của mục interfaces_count cung cấp số lượng siêu giao diện trực tiếp của lớp hoặc loại giao diện này.
* `giao diện[]` - Mỗi giá trị trong mảng giao diện phải là một chỉ mục hợp lệ trong bảng hằng số.
* `fields_count` - Giá trị của mục fields_count cung cấp số cấu trúc field_info trong bảng trường.
* `trường[]` - Mỗi giá trị trong bảng trường phải là cấu trúc field_info đưa ra mô tả đầy đủ về trường trong lớp hoặc giao diện này.
* `methods_count` - Giá trị của mục methods_count cung cấp số cấu trúc method_info trong bảng phương thức.
* `phương thức[]` - Mỗi giá trị trong bảng phương thức phải là cấu trúc method_info đưa ra mô tả đầy đủ về phương thức trong lớp hoặc giao diện này. Nếu cả hai cờ ACC_NATIVE và ACC_ABSTRACT đều không được đặt trong mục access_flags của cấu trúc method_info, thì hướng dẫn Máy ảo Java triển khai phương thức này cũng được cung cấp.
* `attributes_count` - Giá trị của thuộc tính_count cho biết số lượng thuộc tính (§4.7) trong bảng thuộc tính của lớp này.
* `thuộc tính[]` - Mỗi giá trị của bảng thuộc tính phải là một cấu trúc thuộc tính_thông tin.




## Người giới thiệu

* [Định dạng tệp của lớp](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html)

