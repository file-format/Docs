{
  "date" : "2022-07-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp HDR - Tệp hình ảnh HDR là gì?",
  "description":"Tìm hiểu về định dạng tệp HDR và các API có thể tạo và mở tệp HDR.",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-07-21"
}

## Tệp HDR là gì?

Tệp HDR là định dạng tệp hình ảnh raster Dải động cao (HDR) để lưu trữ ảnh máy ảnh kỹ thuật số. Nó cho phép người chỉnh sửa ảnh nâng cao màu sắc và độ sáng của hình ảnh kỹ thuật số có dải động hạn chế. Sự sửa đổi này có thể cải thiện độ sáng xung quanh các góc, mang lại hình ảnh gần với tự nhiên. Các tệp HDR thường được lưu dưới dạng hình ảnh raster 32 bit. Adobe Photoshop có thể tạo và mở các tệp HDR.

Các tệp HDR còn được gọi là HDRI.

## Định dạng tệp HDR - Thông tin khác

Định dạng tệp HDR dựa trên định dạng tệp Radiance Picture (.pic) gốc. Dữ liệu pixel của tệp HDR thường được lưu trữ không nén, nhưng trong một số trường hợp, dữ liệu này được nén bằng hệ thống mã hóa độ dài chạy đơn giản.

### Cấu trúc tệp HDR

Một tệp hình ảnh HDR bao gồm ba phần sau:

* **Header:** Tệp HDR được xác định bằng byte đầu tiên trong tệp hình ảnh, tức là "#?RADIANCE".
* **Chuỗi độ phân giải:** Tiêu đề được theo sau bởi một dòng độ phân giải duy nhất bao gồm 4 giá trị; mỗi nhãn X và Y theo sau là một giá trị số nguyên. Thứ tự của X và Y biểu thị chuyển động quay. Sự kết hợp của X và Y với các giá trị dương và âm bao gồm tất cả các hướng và góc quay có thể có của hình ảnh.
* **Dữ liệu pixel:** Dữ liệu pixel của tệp HDR không được nén hoặc được nén bằng cách sử dụng mã hóa độ dài chạy tiêu chuẩn.

## API HDR/HDRI mã nguồn mở

* **[imageinfo](https://github.com/xiaozhuai/imageinfo )** - Thư viện tiêu đề đơn siêu nhanh đa nền tảng [C++](/vi/programming/cpp/) để lấy kích thước và định dạng hình ảnh mà không cần tải/giải mã.
* **[imgaeinfo-rs](https://github.com/xiaozhuai/imageinfo-rs)** - Thư viện Rust để lấy kích thước và định dạng hình ảnh mà không cần tải/giải mã. Hỗ trợ [.avif](/vi/image/avif/), [.bmp](/vi/image/bmp), [.cur](/vi/image/cur/), [.dds](/vi/image/dds/), [. gif](/vi/image/gif/), hdr (pic), [heic (heif)](/vi/image/heic/), [.icns](/vi/image/icns/), [.ico](/vi/image/ico /), [.jp2](/vi/image/jp2/), [jpeg (jpg)](/vi/image/jpeg/), [jpx](/vi/image/jpx/), ktx, [png](/vi/image/png /), [psd](/vi/image/psd/), qoi, tga, tiff (tif) và webp.
* **[HdrHistogram](https://github.com/HdrHistogram/HdrHistogram)** - Triển khai Java của HdrHistogram.

## Người giới thiệu

* [Rạng rỡ HDR](http://paulbourke.net/dataformats/pic/)
* [thông tin hình ảnh](https://github.com/xiaozhuai/imageinfo )

