{
  "date" : "2019-10-11",
  "keywords" :[ "tệp xpm", "định dạng tệp xpm", "tệp xpm là gì", "tệp", "ví dụ xpm", "phần mở rộng tệp xpm","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp XPM - X PixMap",
  "description":"Tìm hiểu về định dạng tệp XPM và các API có thể tạo và mở tệp XPM.",
  "linktitle" : "XPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp XPM là gì?

Tệp có phần mở rộng .xpm là định dạng tệp hình ảnh được sử dụng bởi Hệ thống X Windows. Nó hỗ trợ các pixel trong suốt và thường nhắm mục tiêu tạo các biểu tượng pixmap. Nó hỗ trợ dữ liệu pixmap đơn sắc, tỷ lệ gra và màu. Chúng được thiết kế để có thể chỉnh sửa bằng tay và có thể được bao gồm trong mã [C](/vi/programming/c/). Với mục đích này, các tệp XPM ở định dạng tệp văn bản thuần túy và tuân theo cú pháp ngôn ngữ lập trình C. Các tệp XPM có thể được mở bằng nhiều ứng dụng xem hình ảnh, chẳng hạn như
Bộ đồ họa CorelDRAW 2020, Corel PaintShop Pro, IrfanView và Canvas X.

## Định dạng tệp XPM

Định dạng tệp XPM sử dụng cú pháp C để chúng được tích hợp trong các chương trình C và C++. Nó bao gồm sáu phần khác nhau sau đây.

* \<Values>
* \<Colors>
* \<Pixels>
* \<Extensions>

Các phần thực sự là một chuỗi các chuỗi như sau.

```
/* XPM */
static char*<variable_name>[] = {
  <Values>
  <Colors>
  <Pixels>
  <Extensions>
};
```
Sau đây là nội dung chi tiết của từng phần.

`<Values> ` - Phần này là một chuỗi chứa bốn hoặc sáu số nguyên nằm trong cơ số 10 và tương ứng với:

* chiều rộng và chiều cao của pixmap
* số lượng màu sắc
* số ký tự trên mỗi pixel
* tọa độ điểm phát sóng tùy chọn và thẻ XPMEXT

`<Colors> ` - Phần này chứa nhiều chuỗi tương ứng với số lượng màu. Mỗi chuỗi như sau:

```
<chars>{<key><color> }+
```
`<Pixels> ` - Phần này bao gồm<height> chuỗi và<width> \*<chars_per_pixel> nhân vật. Mọi<chars_per_pixel> chuỗi độ dài phải là một trong các nhóm được xác định trước đó trong<Colors> tiết diện.

`<Extension> ` - Phần mở rộng phải được gắn nhãn, nếu nó không trống, trong<Values> tiết diện. Nó có thể bao gồm một số<Extension> tiểu mục có thể thuộc hai loại sau:

* một chuỗi độc lập bao gồm như sau: XPMEXT<extension-name><extension-data>
* hoặc một khối được tạo bởi nhiều chuỗi:XPMEXT<extension-name><related extension-data composed of several strings>

## Người giới thiệu

* [XPM - Wikipedia](https://en.wikipedia.org/wiki/X_PixMap)
* [Hướng dẫn sử dụng XPM](http://www.xfree86.org/current/xpm.pdf)

