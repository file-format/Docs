{
  "date" : "2019-12-13",
  "keywords" :[ "tệp pptx", "định dạng tệp pptx", "tệp pptx là gì", "tệp", "ví dụ pptx", "phần mở rộng tệp pptx","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp PPTX và API có thể tạo và mở tệp PPTX.",
  "title" :"PPTX - Định dạng tệp bản trình bày PowerPoint",
  "linktitle" : "PPTX",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp PPTX là gì?

Các tệp có phần mở rộng PPTX là các tệp trình bày được tạo bằng ứng dụng Microsoft PowerPoint phổ biến. Không giống như phiên bản trước của định dạng tệp bản trình bày PPT là nhị phân, định dạng PPTX dựa trên định dạng tệp bản trình bày XML mở của Microsoft PowerPoint. Tệp bản trình bày là một tập hợp các trang chiếu trong đó mỗi trang chiếu có thể bao gồm văn bản, hình ảnh, định dạng, hoạt ảnh và phương tiện khác. Các trang trình bày này được trình bày cho khán giả dưới dạng trình chiếu với cài đặt bản trình bày tùy chỉnh.

## Tóm tắt lịch sử

Định dạng tệp PPTX được giới thiệu vào năm 2007 và sử dụng tiêu chuẩn Open XML được Microsoft điều chỉnh vào năm 2000. Trước PPTX, định dạng tệp phổ biến được sử dụng là PPT là định dạng tệp nhị phân thuần túy. Loại tệp mới có thêm lợi thế về kích thước tệp nhỏ, ít thay đổi về lỗi và hình ảnh được định dạng tốt. Đó là vào đầu năm 2000 khi Microsoft quyết định thực hiện thay đổi để phù hợp với tiêu chuẩn cho **Office Open XML**. Đến năm 2007, định dạng tệp mới này đã trở thành một phần của Office 2007 và cũng được đưa vào các phiên bản mới của Microsoft Office.

## Thông số kỹ thuật định dạng tệp PPTX

Các tệp được tạo bằng định dạng tệp Office Open XML là một tập hợp các tệp XML cùng với các tệp khác cung cấp liên kết giữa tất cả các tệp cấu thành. Bộ sưu tập này thực sự là một kho lưu trữ nén có thể được giải nén để xem nội dung của nó. Để làm như vậy, chỉ cần đổi tên phần mở rộng tệp PPTX bằng zip và giải nén nó để quan sát nội dung của nó (Xem [Thông số định dạng tệp PPTX](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-pptx/ efd8bb2d-d888-4e2e-af25-cad476730c9f) của Microsoft).

Các phần sau đây làm sáng tỏ từng phần trong số này.

### [Content_Types].xml

Đây là tệp duy nhất được tìm thấy ở cấp độ cơ sở khi giải nén zip. Nó liệt kê các loại nội dung cho các phần trong gói. Tất cả các tham chiếu đến các tệp XML có trong gói đều được tham chiếu trong tệp XML này. Sau đây là kiểu nội dung cho một phần slide:

```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```

Nếu cần thêm các phần mới vào gói, thì có thể thực hiện bằng cách thêm phần mới và cập nhật bất kỳ mối quan hệ nào trong các tệp .rels. Cần lưu ý rằng đối với thay đổi như vậy, Content_Types.xml cũng phải được cập nhật.

### \_rels (Thư mục) ###

Mối quan hệ giữa các phần khác và tài nguyên bên ngoài gói được duy trì bởi phần quan hệ. Thư mục Mối quan hệ chứa một tệp XML duy nhất lưu trữ các mối quan hệ ở cấp độ gói. Liên kết đến các phần chính của tệp PPTX được chứa trong tệp này dưới dạng URI. Các URI này xác định loại mối quan hệ của từng phần chính với gói. Điều này bao gồm mối quan hệ với tài liệu văn phòng chính nằm dưới dạng ppt/presentation.xml và các phần khác trong docProps dưới dạng thuộc tính cốt lõi và mở rộng.

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```

Mỗi phần của tài liệu là nguồn của một hoặc nhiều mối quan hệ sẽ có phần mối quan hệ riêng, trong đó mỗi phần mối quan hệ như vậy được tìm thấy trong thư mục con \_rels của phần đó và được đặt tên bằng cách thêm '.rels' vào tên của phần đó. phần. Phần nội dung chính (presentation.xml) có phần quan hệ riêng của nó (presentation.xml.rels). Nó chứa các mối quan hệ với các phần khác của nội dung, chẳng hạn như slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml, cũng như các URI cho các liên kết bên ngoài.

#### Mối quan hệ rõ ràng ####

Đối với mối quan hệ rõ ràng, tài nguyên được tham chiếu bằng thuộc tính Id của<Relationship> yếu tố. Nghĩa là, Id trong nguồn ánh xạ trực tiếp tới Id của một mục mối quan hệ, với một tham chiếu rõ ràng tới đích.

Ví dụ: một trang chiếu có thể chứa một siêu kết nối như sau:

```
<a:hlinkClick r:id#"rId2">
```

R:id#"rId2" tham chiếu mối quan hệ sau trong phần mối quan hệ của trang chiếu (slide1.xml.rels).

```
<Relationship Id#"rId2" Type#"http://. . ./hyperlink" Target#"http://www.google.com/" TargetMode#"External"/>
```

#### Quan Hệ Ngầm ####

Đối với một mối quan hệ ngầm định, không có tham chiếu trực tiếp như vậy đến một `<Relationship> ID`. Thay vào đó, tài liệu tham khảo được hiểu.

### Thư mục ppt ###

Đây là thư mục chính chứa tất cả các thông tin chi tiết về nội dung của Bài thuyết trình. Theo mặc định, nó có các thư mục sau:

* \_rels
* chủ đề
* slide
* slideLayouts
* slideMasters

và các tệp xml sau:

* trình bày.xml
* presProps.xml
* bảngStyles.xml
* viewProps.xml

## Người giới thiệu ##

* [[MS-PPTX] - Định dạng tệp PPTX](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-pptx/efd8bb2d-d888-4e2e-af25-cad476730c9f)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

