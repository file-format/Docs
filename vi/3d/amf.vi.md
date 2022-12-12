{
  "date" : "2019-10-11",
  "keywords" :[ "amf", "amf file", "amf file format", "file format", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp AMF và các API có thể mở và tạo tệp AMF.",
  "title" :"AMF - Tệp sản xuất bồi đắp",
  "linktitle" : "AMF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp AMF là gì?
Tệp AMF bao gồm các hướng dẫn về mô tả đối tượng để các quy trình Sản xuất đắp dần sử dụng. Nó chứa một lỗ mở<amf> thẻ XML và kết thúc bằng một</amf> yếu tố. Điều này được bắt đầu bởi một dòng khai báo XML chỉ định phiên bản XML và mã hóa của tệp. Các khai báo có thể bao gồm thông tin đơn vị đo lường và trong trường hợp không có thông tin đó, milimét được sử dụng làm đơn vị mặc định.


## Định dạng tệp AMF

Định dạng tệp Sản xuất bồi đắp (**AMF**) xác định các tiêu chuẩn mở cho mô tả đối tượng để được sử dụng bởi các quy trình sản xuất bồi đắp như In 3D. Các chương trình CAD sử dụng định dạng tệp AMF bằng cách sử dụng các thông tin như hình học, màu sắc và chất liệu của các đối tượng. AMF khác với định dạng STL vì định dạng bên không hỗ trợ màu sắc, vật liệu, lưới và chòm sao.

### Các thành phần của tệp AMF

Năm yếu tố cấp cao nhất được xác định bằng<AMF> các thẻ như chi tiết dưới đây. Sự hiện diện của một thành phần đối tượng duy nhất là bắt buộc đối với tệp AMF đầy đủ chức năng.

`<object> ` - Phần tử đối tượng xác định một khối hoặc nhiều khối vật liệu, mỗi khối được liên kết với một ID vật liệu để in. Ít nhất một phần tử đối tượng phải có mặt trong tệp. Các đối tượng bổ sung là tùy chọn.

`<material> ` - Phần tử vật liệu tùy chọn xác định một hoặc nhiều vật liệu để in với ID vật liệu được liên kết. Nếu không có phần tử vật liệu nào được đưa vào, thì một vật liệu mặc định duy nhất sẽ được giả định.

`<texture> ` - Thành phần họa tiết tùy chọn xác định một hoặc nhiều hình ảnh hoặc họa tiết để ánh xạ màu hoặc họa tiết, mỗi hình ảnh hoặc họa tiết có một ID họa tiết được liên kết.

`<constellation> ` - Phần tử chòm sao tùy chọn kết hợp theo thứ bậc các đối tượng và các chòm sao khác thành một mẫu tương đối để in.

`<metadata> ` - Phần tử siêu dữ liệu tùy chọn chỉ định thông tin bổ sung về (các) đối tượng và các phần tử có trong tệp.

## Ví dụ AMF

Sau đây là một ví dụ về tệp AMF có thể được sao chép vào tệp [text](/vi/word-processing/txt/) và được lưu dưới dạng tệp nén [zip](/vi/compression/zip/) để mở.
```
<?xml version="1.0" encoding="utf-8"?>
<amf unit="inch" version="1.1">
  <metadata type="name">Split Pyramid</metadata>
  <metadata type="author">John Smith</metadata>
  <object id="1">
    <mesh>
      <vertices>
        <vertex><coordinates><x>0</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0.5</x><y>0.5</y><z>1</z></coordinates></vertex>
      </vertices>
      <volume materialid="2">
        <metadata type="name">Hard side</metadata>
        <triangle><v1>2</v1><v2>1</v2><v3>0</v3></triangle>
        <triangle><v1>0</v1><v2>1</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>1</v2><v3>2</v3></triangle>
        <triangle><v1>0</v1><v2>4</v2><v3>2</v3></triangle>
      </volume>
      <volume materialid="3">
        <metadata type="name">Soft side</metadata>
        <triangle><v1>2</v1><v2>3</v2><v3>1</v3></triangle>
        <triangle><v1>1</v1><v2>3</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>3</v2><v3>2</v3></triangle>
        <triangle><v1>4</v1><v2>2</v2><v3>1</v3></triangle>
      </volume>
    </mesh>
  </object>
  <material id="2">
    <metadata type="name">Hard material</metadata>
    <color><r>0.1</r><g>0.1</g><b>0.1</b></color>
  </material>
  <material id="3">
    <metadata type="name">Soft material</metadata>
    <color><r>0</r><g>0.9</g><b>0.9</b><a>0.5</a></color>
  </material>
</amf>
```
## Người giới thiệu

* [AMF - Wikipedia](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
* [Thông số kỹ thuật AMF trên ISO](https://www.iso.org/standard/67472.html)

