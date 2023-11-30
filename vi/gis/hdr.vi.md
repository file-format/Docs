{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp HDR- Định dạng tệp tiêu đề ESRI BIL",
  "description":"Tệp HDR là gì?",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "identifier":"gis-hdr",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-23"
}

## Tập tin HDR là gì?

Tệp HDR là tệp tiêu đề GIS chứa thông tin tiêu đề cho tệp Dải được xen kẽ theo dòng (.BIL). Nó mô tả dữ liệu hình ảnh và có cùng tên với tên của tệp hình ảnh. Tệp HDR bao gồm một tập hợp các mục, mỗi mục mô tả một thuộc tính cụ thể của hình ảnh. Tệp HDR mô tả bố cục và định dạng của tệp BIL để dịch sang tọa độ trong thế giới thực kết hợp với tệp tham chiếu địa lý riêng biệt.

## Định dạng tệp HDR

Các tệp HDR được lưu ở định dạng tệp văn bản ASCII. Nó chứa một tập hợp các mục trong đó mỗi mục mô tả một thuộc tính cụ thể của hình ảnh. Mỗi tệp HDR có định dạng sau:

```
<keyword> <value>
```

`<keyword> ` - Nó cho biết thuộc tính cụ thể đang được đặt
`<value> ` - Đó là giá trị mà thuộc tính đang được đặt

Không có giới hạn về thứ tự của các mục trong tiêu đề. Tuy nhiên, mỗi mục phải nằm trên một dòng riêng biệt để tuân thủ phương pháp phân tích cú pháp được trình đọc HDR sử dụng.

## Tổng Hợp Từ Khóa Sử Dụng Trong File HDR

|Từ khóa |Giá trị được chấp nhận |Mặc định|
---|---|---|
|nrows |bất kỳ số nguyên nào > 0| không có
|ncols |bất kỳ số nguyên nào > 0| không có
|nbands |bất kỳ số nguyên nào > 0| 1
|nbit |1, 4, 8, 16, 32| số 8
|thứ tự byte| I = Intel;M = Motorola |giống như máy chủ|
|bố cục| bil, bip, bsq| tỷ|
|bỏ qua byte| bất kỳ số nguyên nào ≥ 0| 0
|ulxmap |bất kỳ số thực nào| 0|
|ulymap |số thực bất kỳ |nrows - 1|
|xdim |bất kỳ số thực nào| 1
|ydim |bất kỳ số thực nào| 1
|bandrowbytes |bất kỳ số nguyên nào > 0| số nguyên nhỏ nhất ≥ (ncols x nbits) / 8|
|totalrowbytes |bất kỳ số nguyên nào > 0| đối với bil: nbands x bandrowbytes;đối với bip: số nguyên nhỏ nhất ≥ (ncols x nbands x nbits) / 8|
|bandgapbytes |bất kỳ số nguyên nào ≥ 0| 0|

## Người giới thiệu

* [Định dạng tệp HRD - ArcGIS](https://webhelp.esri.com/arcgisdesktop/9.2/index.cfm?TopicName=BIL,_BIP,_and_BSQ_raster_files)

