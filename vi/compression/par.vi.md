{
"date" :  "2023-07-18",
   "keywords":[
"PAR",
"Tệp PAR",
"cách mở tệp mệnh giá",
"tài liệu",
"Phần mở rộng tệp PAR",
"sự mở rộng",
"tài liệu"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft": "false",
"toc":true,
"title":"Định dạng tệp PAR - Tệp chỉ mục Parchive",
   "description":"Tìm hiểu về định dạng PAR và các API có thể tạo và mở tệp PAR.",
"linktitle":"PAR",
   "menu":{
      "docs":{
         "identifier":"compression-par",
         "parent":"compression"
}
},
"lastmod":"2023-07-18"
}

## Tập tin PAR là gì?

Trong kho lưu trữ Parchive (PAR), tệp .par đề cập đến tệp chỉ mục chứa một nhóm khối lượng chẵn lẻ hoặc khối chẵn lẻ. Tệp chỉ mục này được sử dụng cho mục đích phát hiện và khôi phục lỗi khi một hoặc nhiều tệp trong kho lưu trữ bị mất hoặc bị hỏng.

Kho lưu trữ Parchive thường bao gồm cả tệp dữ liệu gốc và khối lượng chẵn lẻ tương ứng. Khối chẵn lẻ được tạo bằng thuật toán sửa lỗi Reed-Solomon. Các khối chẵn lẻ này chứa thông tin dư thừa có thể được sử dụng để khôi phục các tệp dữ liệu gốc.

Tệp .par, còn được gọi là tập hợp khối lượng chẵn lẻ, chứa thông tin về cấu trúc và vị trí của khối lượng chẵn lẻ trong kho lưu trữ. Nó phục vụ như một chỉ mục hoặc bản đồ cho quá trình phục hồi. Bằng cách sử dụng tệp .par, phần mềm PAR chuyên dụng có thể xác định khối lượng chẵn lẻ nào là cần thiết và cách sử dụng chúng để tái tạo lại các tệp bị thiếu hoặc bị hỏng.

Khi một hoặc nhiều tệp trong kho lưu trữ Parchive không thể truy cập được hoặc bị hỏng, tệp .par có thể được sử dụng cùng với các ổ đĩa chẵn lẻ có sẵn để khôi phục dữ liệu bị mất. Phần mềm PAR đọc tệp .par, xác định các tệp bị thiếu hoặc bị hỏng và sử dụng khối lượng chẵn lẻ để xây dựng lại chúng.

## Làm cách nào để mở tệp PAR?

Để mở và sử dụng tệp .par, bạn sẽ cần phần mềm PAR chuyên dụng. Dưới đây là một số tùy chọn phần mềm phổ biến có thể xử lý tệp .par:

- **QuickPar:** QuickPar là phần mềm PAR được sử dụng rộng rãi cho Windows. Nó cho phép bạn tạo, xác minh và sửa chữa các tệp PAR. Bạn có thể mở tệp .par trong QuickPar để xác minh tính toàn vẹn của tệp hoặc sử dụng tệp đó để sửa chữa các tệp bị hỏng hoặc bị thiếu trong kho lưu trữ Parchive.

- **MultiPar:** MultiPar là một phần mềm cải cách hành chính phổ biến khác có sẵn cho Windows. Nó hỗ trợ cả định dạng tệp PAR và PAR2, đồng thời cung cấp các tính năng nâng cao để tạo, xác minh và sửa chữa các kho lưu trữ. MultiPar có thể mở tệp .par và thực hiện các hoạt động phát hiện và khôi phục lỗi dựa trên khối lượng chẵn lẻ được cung cấp.

- **MacPAR deLuxe:** MacPAR deLuxe là phần mềm PAR được thiết kế dành riêng cho macOS. Nó hỗ trợ các định dạng tệp PAR và PAR2 và cung cấp chức năng tương tự như QuickPar và MultiPar. MacPAR deLuxe có thể mở tệp .par và hỗ trợ xác minh kho lưu trữ cũng như khôi phục các tệp bị hỏng hoặc bị thiếu.

## Định dạng tệp PAR - Thông tin thêm

Định dạng tệp PAR, thường được gọi là Parchive, là định dạng tệp cụ thể được sử dụng để tạo dữ liệu chẵn lẻ và thực hiện phát hiện và khôi phục lỗi trong kho lưu trữ tệp. Định dạng tệp PAR thường bao gồm ba loại: PAR, PAR2 và PAR3.

- **PAR:** Định dạng tệp PAR ban đầu, còn được gọi là PAR1, được phát triển bởi dự án Parchive. Nó bao gồm dữ liệu chẵn lẻ được tạo từ các tệp dữ liệu gốc. Các tệp PAR cung cấp mức độ phát hiện và phục hồi lỗi cơ bản nhưng có những hạn chế về khả năng sửa lỗi.

- **PAR2:** PAR2 là phiên bản cải tiến của định dạng tệp PAR. Nó cung cấp khả năng sửa lỗi nâng cao hơn và các tính năng khôi phục nâng cao. Các tệp PAR2 thường được sử dụng để tạo dữ liệu chẵn lẻ có thể khôi phục các tệp bị mất hoặc bị hỏng trong kho lưu trữ. Các tệp PAR2 cung cấp khả năng bảo vệ tốt hơn khỏi hỏng dữ liệu và được sử dụng rộng rãi cho mục đích lưu trữ tệp.

- **PAR3:** PAR3 là phiên bản mới nhất của định dạng tệp PAR và cung cấp những cải tiến hơn nữa về sửa lỗi và phục hồi. Nó thậm chí còn cung cấp mức độ dự phòng và khả năng sửa lỗi cao hơn so với PAR2. Các tệp PAR3 được thiết kế để cung cấp các tùy chọn bảo vệ và phục hồi mạnh mẽ hơn cho dữ liệu được lưu trữ trong kho lưu trữ.

Cả hai định dạng tệp PAR2 và PAR3 đều được phần mềm PAR hỗ trợ rộng rãi và cung cấp khả năng xác minh tính toàn vẹn của tệp trong kho lưu trữ và khôi phục dữ liệu bị mất hoặc bị hỏng. Các tệp PAR và PAR2 vẫn được sử dụng phổ biến, trong khi các tệp PAR3 đang dần được áp dụng do khả năng sửa lỗi được nâng cao.

## Người giới thiệu
* [Parchive](https://en.wikipedia.org/wiki/Parchive)

