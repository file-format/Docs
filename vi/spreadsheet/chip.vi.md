{
"ngày": "2023-03-01",
  "keywords": [
"tệp chip",
"tập tin chip là gì",
"tài liệu",
"cách mở tập tin chip",
"phần mở rộng tập tin chip",
"sự mở rộng"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Định dạng tệp CHIP - Tệp chú thích microarray",
  "description":"Tìm hiểu về định dạng tệp CHIP và các API có thể tạo và mở tệp CHIP.",
"linktitle":"CHIP",
  "menu": {
    "docs": {
      "identifier": "spreadsheet-chip",
      "parent": "spreadsheet"
}
},
"lastmod": "2023-03-01"
}

## Tập tin CHIP là gì?

Tệp CHIP là tệp chú thích microarray và có liên quan đến phần mềm Phân tích làm giàu bộ gen (GSEA). GSEA là một phương pháp tính toán nhằm đánh giá liệu một bộ gen được xác định trước (một bộ gen) có cho thấy sự khác biệt có ý nghĩa thống kê giữa hai trạng thái sinh học hay không, chẳng hạn như mô khỏe mạnh so với mô bị bệnh hoặc tế bào được điều trị bằng thuốc so với tế bào không được điều trị. Để thực hiện GSEA, bạn cần có bộ dữ liệu biểu hiện gen và cơ sở dữ liệu bộ gen. Cơ sở dữ liệu bộ gen chứa thông tin về các gen trong bộ gen, chẳng hạn như chức năng, con đường hoặc biểu hiện cụ thể của mô.

Tệp CHIP là một loại cơ sở dữ liệu bộ gen cụ thể được GSEA sử dụng. Nó chứa thông tin về các gen và bộ gen có liên quan đến nền tảng microarray đang được sử dụng trong thí nghiệm. Tệp CHIP cung cấp các chú thích cho từng đầu dò trên microarray, chẳng hạn như ký hiệu gen, tên gen, mô tả gen và vị trí nhiễm sắc thể. Thông tin này được sử dụng để so khớp các mẫu dò với các gen trong tập dữ liệu biểu hiện gen và gán chúng vào các bộ gen thích hợp để phân tích GSEA.

Để sử dụng tệp CHIP trong GSEA, bạn cần nhập tệp đó vào phần mềm và liên kết tệp đó với tập dữ liệu microarray của bạn. GSEA hỗ trợ nhiều nền tảng microarray khác nhau và cung cấp các tệp CHIP dựng sẵn cho nhiều nền tảng trong số đó. Tuy nhiên, bạn cũng có thể tạo tệp CHIP của riêng mình bằng cách sử dụng cơ sở dữ liệu chú thích từ các nguồn bên ngoài, chẳng hạn như NCBI hoặc Makeembl.

## Thêm thông tin

Tệp CHIP không phải là bảng tính nhưng có thể mở và chỉnh sửa tệp này trong chương trình bảng tính như Microsoft Excel hoặc Google Trang tính. Tệp CHIP là một loại tệp văn bản chứa dữ liệu được phân cách bằng tab, có thể dễ dàng nhập vào chương trình bảng tính để xem và chỉnh sửa.

Trong chương trình bảng tính, bạn có thể thao tác dữ liệu trong tệp CHIP để thêm, xóa hoặc sửa đổi chú thích cho các gen và bộ gen trên microarray. Ví dụ: bạn có thể sử dụng chương trình bảng tính để thêm chú thích tùy chỉnh cho các gen không có trong tệp CHIP gốc hoặc để hợp nhất nhiều tệp CHIP từ các nguồn khác nhau thành một tệp duy nhất.

Tuy nhiên, điều quan trọng cần lưu ý là tệp CHIP có định dạng và cấu trúc cụ thể phải được duy trì để tương thích với phần mềm GSEA. Nếu bạn sửa đổi nội dung của tệp CHIP trong chương trình bảng tính, bạn phải đảm bảo rằng các sửa đổi đó không làm thay đổi định dạng hoặc nội dung tệp theo cách có thể ảnh hưởng đến tính chính xác hoặc tính hợp lệ của phân tích GSEA.

## Làm cách nào để mở tệp CHIP?

Vì tệp CHIP chứa dữ liệu được phân cách bằng tab nên nếu bạn muốn xem dữ liệu bảng tính, bạn có thể mở tệp đó trong Microsoft Excel.

## Người giới thiệu
* [GSEA](https://en.wikipedia.org/wiki/Gene_set_enrichment_analysis)
