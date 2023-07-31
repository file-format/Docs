{
  "date" : "2019-12-03",
  "keywords" :[ "DOCX","tệp", "định dạng", "loại tệp", "phần mở rộng","tệp DOCX là gì?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOCX",
  "description":"Tìm hiểu về định dạng tệp DOCX và các API có thể tạo và mở tệp DOCX.",
  "linktitle" : "DOCX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## Tệp DOCX là gì? ##

DOCX là một định dạng nổi tiếng cho các tài liệu Microsoft Word. Được giới thiệu từ năm 2007 cùng với việc phát hành Microsoft Office 2007, cấu trúc của định dạng Tài liệu mới này đã được thay đổi từ tệp nhị phân đơn giản thành sự kết hợp của tệp XML và tệp nhị phân. Các tệp Docx có thể được mở bằng Word 2007 và các phiên bản mới hơn nhưng không thể mở bằng các phiên bản MS Word cũ hơn hỗ trợ phần mở rộng tệp DOC.

## Lược Sử ##

Sau khi Microsoft mở các thông số kỹ thuật cho định dạng tệp DOC, các đối thủ cạnh tranh của nó đã dễ dàng thiết kế ngược định dạng này và cung cấp hỗ trợ tương tự trong các ứng dụng của riêng họ. Ngoài ra, sự cạnh tranh từ Open Office dưới dạng Định dạng Tài liệu Mở của nó đã buộc Microsoft phải áp dụng các tiêu chuẩn mở và rộng rãi hơn. Đó là vào đầu năm 2000 khi Microsoft quyết định thực hiện thay đổi để phù hợp với tiêu chuẩn cho **Office Open XML**. Các tài liệu theo Tiêu chuẩn mới này đã được cung cấp [phần mở rộng .docx](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd), chữ "X" dành cho XML. Đến năm 2007, định dạng tệp mới này đã trở thành một phần của Office 2007 và cũng được đưa vào các phiên bản mới của Microsoft Office. Loại tệp mới có thêm lợi thế về kích thước tệp nhỏ, ít thay đổi về hỏng hóc hơn và thể hiện hình ảnh được định dạng tốt.

## Thông số kỹ thuật định dạng tệp DOCX - Thông tin thêm

Tệp Docx bao gồm một tập hợp các tệp XML được chứa bên trong kho lưu trữ ZIP. Nội dung của một tài liệu Word mới có thể được xem bằng cách giải nén nội dung của nó. Bộ sưu tập chứa danh sách các tệp XML được phân loại là:

* Tệp siêu dữ liệu - chứa thông tin về các tệp khác có sẵn trong kho lưu trữ
* Tài liệu - chứa nội dung thực tế của tài liệu

### Tệp siêu dữ liệu ###

Microsoft Word sử dụng các tệp này để tìm mối quan hệ giữa các tệp và để định vị nội dung tài liệu. Khi một kho lưu trữ tài liệu Word được giải nén, nó chứa một số tệp như được trình bày chi tiết bên dưới.

#### Mối quan hệ - \_rels/.rels ####

Tệp này chứa thông tin cho MS Word biết nơi tìm nội dung tài liệu và các tài liệu tham khảo khác. Mỗi mối quan hệ được xác định bởi một id mối quan hệ duy nhất và chỉ định tệp XML được tham chiếu làm mục tiêu. Một tệp mối quan hệ mẫu được hiển thị như sau:

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"word/document.xml"/>.
```

#### Loại nội dung ####

Một tài liệu có thể chứa một số loại phương tiện bên trong như hình ảnh, chủ đề, chữ nghệ thuật, v.v. [Content_Types].xml chứa thông tin về các loại phương tiện như vậy có trong tài liệu. Nội dung của một tệp XML như vậy được hiển thị như sau:

```
<Override PartName#"/word/document.xml" ContentType#"application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/>
```

#### Tham chiếu đến Tài nguyên - \_rels/document.xml.rels ####

Thông tin về tài nguyên, chẳng hạn như hình ảnh được nhúng trong tài liệu, được tham chiếu trong tệp XML này.

#### Nội dung tài liệu chính ####

Điều này đề cập đến tệp XML chính của kho lưu trữ chứa nội dung văn bản của tài liệu. Nội dung này được thể hiện bằng nhiều nút theo thông số kỹ thuật của OpenOffice XML. Hầu hết nội dung của tệp này bao gồm Đoạn văn và Bảng, mặc dù chúng cũng có thể là các nút khác.

### Các nút định dạng tệp ###

Tệp document.xml chính là một tập hợp các nút để biểu diễn toàn bộ nội dung của một tệp. Mỗi nút có điểm bắt đầu và điểm kết thúc bao bọc các nút khác hoặc nội dung. Một ví dụ đơn giản về tệp xml như sau:

```
<w:document>
   <w:body>
       <w:p w:rsidR#"005F670F" w:rsidRDefault#"005F79F5">
           <w:r><w:t>Example Document</w:t></w:r>
       </w:p>
       <w:sectPr w:rsidR#"005F670F">
           <w:pgSz w:w#"12240" w:h#"15840"/>
           <w:pgMar w:top#"1440" w:right#"1440" w:bottom#"1440" w:left#"1440" w:header#"720" w:footer#"720"
                    w:gutter#"0"/>
           <w:cols w:space#"720"/>
           <w:docGrid w:linePitch#"360"/>
       </w:sectPr>
   </w:body>
</w:document>
```

Sau đây là thông tin về một số nút có trong tệp DOCX để trình bày nội dung.

`<w:document> ` - Đại diện cho phần tử gốc của nội dung chính của tệp.

`<w:body> ` - Đại diện cho phần nội dung của tài liệu có thể bao gồm nhiều nút phần tử khác như đoạn văn, bảng và phần.

#### Đoạn ####

Một đoạn văn là chủ sở hữu nội dung chính trong một tài liệu. Nó được đại diện bởi **<w:p> ** phần tử trong một tài liệu. Một đoạn tiếp tục bao gồm một hoặc nhiều lần chạy **<w:r> ** có chứa văn bản thực sự của đoạn văn. Ngoài các lần chạy, các đoạn văn cũng có thể chứa các thành phần tài liệu khác như siêu liên kết, nhận xét, v.v. Một ví dụ về cấu trúc đoạn văn được hiển thị bên dưới:

```
<w:p>
<w:pPr>
<w:pStyle> w:val#"MyStyle"/>
<w:spacing w:before#"120" w:after#"120"/>
</w:pPr>
<w:r>
<w:t xml"space#"preserve">A paragraph is main container in a document that further consists of a one or more runs where the text of paragraph is actually contained.</w:t>
</w:r>
</w:p>
```

## Người giới thiệu ##

* [Định dạng tệp MS - DOCX](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd)
* [Office Open XML](http://officeopenxml.com/)

