{
  "date" : "2022-04-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp DDS- Tệp hình ảnh bề mặt DirectDraw",
  "description":"Tìm hiểu về định dạng tệp DDS và API có thể tạo và mở tệp DDS.",
  "linktitle" : "DDS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-04-02"
}

## Tệp DDS là gì?

Tệp DDS là tệp hình ảnh raster sử dụng định dạng bộ chứa DirectDraw Surface (DDS). Nó lưu trữ kết cấu không nén và nén (DXTn) và triển khai các loại khác nhau để lưu trữ các loại dữ liệu khác nhau. Nó cũng hỗ trợ một số loại dữ liệu khác nhau như kết cấu một lớp, kết cấu với mipmap, bản đồ khối, bản đồ khối và mảng kết cấu. Điều này cho phép các tệp DDS lưu trữ các mô hình đơn vị kết cấu trò chơi video ngoài ảnh kỹ thuật số và hình nền màn hình Windows. Định dạng tệp DDS được Microsoft phát triển để sử dụng với DirectX SDK.

## Định dạng tệp DDS

Các tệp DDS được lưu dưới dạng tệp nhị phân và có thể được sử dụng với DirectX SDK. Nó sử dụng sức mạnh của DirectX để phát triển các ứng dụng kết xuất thời gian thực như trò chơi 3D.

### Bố cục tệp DDS

[Bố cục tệp DDS](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide#dds-file-layout) đã được Microsoft ghi lại chi tiết. Tệp DDS nhị phân chứa thông tin sau.

* DWORD (số ma thuật) chứa giá trị mã bốn ký tự 'DDS ' (0x20534444).
* Mô tả dữ liệu trong tệp.

DDS_HEADER mô tả dữ liệu và DDS_PIXELFORMAT mô tả định dạng pixel. Cả hai đều thay thế các cấu trúc DDSURFACEDESC2, DDSCAPS2 và DDPIXELFORMAT DirectDraw 7 không dùng nữa.

```
DWORD               dwMagic;
DDS_HEADER          header;
```

[Hướng dẫn lập trình định dạng tệp DDS](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide) giải thích thêm các chi tiết kỹ thuật của định dạng tệp này.

## Người giới thiệu

* [DDS - Theo Wikipedia](https://en.wikipedia.org/wiki/DirectDraw_Surface)
* [Hướng dẫn tham khảo kỹ thuật định dạng tệp ZSoft PCX](http://qzx.com/pc-gpe/pcx.txt)

