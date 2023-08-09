{
  "date" : "2021-04-08",
  "keywords" :[ "tệp oar", "định dạng tệp oar", "tệp oar là gì", "tệp", "ví dụ về oar", "phần mở rộng tệp oar","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OAR - Định dạng tệp lưu trữ OpenSimulator",
  "description":"Tìm hiểu về định dạng tệp OAR và API có thể tạo và mở tệp OAR.",
  "linktitle" : "OAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-15"
}

## Tệp OAR là gì?

Tệp có phần mở rộng .oar là tệp lưu trữ được sử dụng bởi ứng dụng OpenSimulator, một máy chủ ứng dụng 3D nguồn mở để tạo môi trường ảo có thể truy cập được cho nhiều người dùng qua mạng. Định dạng tệp OAR cung cấp dữ liệu nội dung cần thiết để tải đầy đủ địa hình, kết cấu đối tượng và hàng tồn kho trên một hệ thống khác. OpenSimulator cũng có siêu lưới tùy chọn cho phép người dùng truy cập các bản cài đặt OpenSimulator khác trên web. Các tệp OAR có ứng dụng/oar loại MIME internet và chứa một hoặc nhiều tệp được lưu trữ.


## Định dạng tệp OAR

OAR là các tệp nhị phân được lưu trữ ở định dạng tệp lưu trữ nén. Phiên bản mới nhất của định dạng tệp OAR là [phiên bản 1.0](http://opensimulator.org/wiki/OAR_Format_1.0) có những thay đổi lớn so với [phiên bản 0.8](http://opensimulator.org/wiki/OAR_Format_0.8) trước đó .số Phiên bản mới nhất hỗ trợ lưu trữ nhiều vùng trong một OAR duy nhất và không tương thích ngược với các phiên bản OpenSimulator trước 0.7.5. Tệp OAR là tệp tar được nén gzipped (tar.gz) ở định dạng unix tar ban đầu (không phải USTAR).

## Ví dụ về vùng OAR
Các tệp AOR có thể chứa nhiều vùng. Cấu trúc của kho lưu trữ như sau (ví dụ này có 4 vùng):

```
archive.xml
assets/
regions/
  1_1_Arizona/
    landdata/
    objects/
    settings/
    terrain/
  2_1_New_Mexico/
    landdata/
    objects/
    settings/
    terrain/
  1_2_Utah/
    landdata/
    objects/
    settings/
    terrain/
  2_2_Colorado/
    landdata/
    objects/
    settings/
    terrain/
```
## Lưu trữ OAR.xml

Tệp kiểm soát lưu trữ chứa số phiên bản chính để xác định khả năng tương thích với các thay đổi định dạng trong tương lai. Sự hiện diện của nội dung ở định dạng OAR được biểu thị bằng phần tử boolean<assets_included> . Thông tin về các vùng bao gồm được chứa trong một bảng kê khai có trong tệp điều khiển. Một ví dụ về Archive.xml như sau.

```
<?xml version="1.0" encoding="utf-16"?>
<archive major_version="1" minor_version="0">
  <creation_info>
    <datetime>1343204139</datetime>
  </creation_info>
  <assets_included>True</assets_included>
  <regions>
    <row>
      <region>
        <id>12345678-1111-1111-1111-111111111111</id>
        <dir>1_1_Arizona</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-2222-2222-2222-222222222222</id>
        <dir>2_1_New_Mexico</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
    <row>
      <region>
        <id>12345678-3333-3333-3333-333333333333</id>
        <dir>1_2_Utah</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-4444-4444-4444-444444444444</id>
        <dir>2_2_Colorado</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
  </regions>
</archive>
```

## Người giới thiệu

* [Định dạng OAR v 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
* [OpenSimulator](http://opensimulator.org/wiki/Main_Page)

