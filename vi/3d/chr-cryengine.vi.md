{
"date" :  "2023-10-11",
   "keywords":[
"chr",
"tập tin chr",
"tập tin ký tự chr cryengine",
"cách mở tệp chr",
"tài liệu",
"phần mở rộng tập tin chr",
"sự mở rộng",
"tài liệu"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft": "false",
"toc":true,
"title":"Định dạng tệp CHR - Tệp ký tự CryENGINE",
   "description":"Tìm hiểu về định dạng tệp CHR CryENGINE Character và API có thể tạo và mở tệp CHR.",
"linktitle":"CHR CryENGINE",
   "menu":{
      "docs":{
         "identifier":"3d-chr-cryengine",
         "parent":"3d"
}
},
"lastmod":"2023-10-11"
}

## Một tập tin CHR là gì?

Tệp CHR trong ngữ cảnh của CryENGINE đề cập đến **Tệp ký tự CryENGINE**. CryENGINE là công cụ trò chơi do Crytek phát triển và các tệp này được sử dụng để lưu trữ mô hình nhân vật và dữ liệu liên quan để sử dụng trong trò chơi điện tử và các ứng dụng thời gian thực khác.

## Tệp ký tự CryENGINE

Tệp ký tự CryENGINE thường chứa các thành phần sau:

1. **Mô hình nhân vật**: Đây là mô hình nhân vật 3D, bao gồm hình học, kết cấu và hoạt ảnh. Những mô hình này thường được tạo bằng phần mềm như Autodesk Maya hoặc Blender, sau đó được nhập vào CryENGINE.
    




















2. **Dữ liệu hoạt ảnh**: CryENGINE hỗ trợ các hoạt ảnh phức tạp cho các nhân vật, vì vậy tệp ".chr" có thể bao gồm nhiều hoạt ảnh khác nhau như đi bộ, chạy, nhảy và hơn thế nữa. Những hoạt ảnh này thường được lưu trữ dưới dạng dữ liệu khung hình chính.
    




















3. **Thông tin về Rigging**: Rigging đề cập đến quá trình tạo cấu trúc khung xương cho mô hình nhân vật, cho phép áp dụng hoạt ảnh vào mô hình. Tệp ".chr" có thể chứa thông tin về hệ thống phân cấp xương và cách kết nối lưới của nhân vật với bộ xương này.
    




















4. **Dữ liệu Vật liệu và Kết cấu**: Thông tin về vật liệu được sử dụng trên mô hình ký tự và bản đồ kết cấu liên quan có thể được đưa vào tệp ".chr". CryENGINE hỗ trợ kết xuất dựa trên vật lý nên những tài liệu này có thể khá chi tiết.
    




















5. **Dữ liệu Vật lý**: Nếu nhân vật có ý định tương tác với thế giới trò chơi, tệp ".chr" có thể bao gồm dữ liệu vật lý như hình dạng va chạm hoặc các ràng buộc đối với vật lý ragdoll.
    




















6. **Cài đặt cấu hình**: Các cài đặt cấu hình khác nhau liên quan đến hành vi của nhân vật trong thế giới trò chơi, chẳng hạn như hành vi AI hoặc các sự kiện theo kịch bản, cũng có thể là một phần của tệp ".chr".

## động cơ khóc

CryENGINE là công cụ trò chơi mạnh mẽ được phát triển bởi Crytek, công ty trò chơi điện tử của Đức. Nó được biết đến với khả năng đồ họa tiên tiến và đã được sử dụng để tạo ra một số trò chơi điện tử có hình ảnh ấn tượng và công nghệ tiên tiến. Dưới đây là một số tính năng và thông tin chính về CryENGINE:

1. **Đồ họa và kết xuất**: CryENGINE nổi tiếng với khả năng đồ họa tiên tiến. Nó hỗ trợ các tính năng như chiếu sáng toàn cầu theo thời gian thực, ánh sáng và bóng động chất lượng cao, hiển thị dựa trên vật lý (PBR) và kết cấu có độ phân giải cao. Những tính năng này góp phần tạo ra thế giới trò chơi chân thực và ấn tượng về mặt hình ảnh.
    




















2. **Công cụ vật lý**: CryENGINE bao gồm công cụ vật lý tích hợp cho phép tương tác thực tế giữa các đối tượng trong thế giới trò chơi. Nó hỗ trợ các tính năng như vật lý cơ thể cứng nhắc, vật lý cơ thể mềm và vật lý ragdoll, khiến nó phù hợp để tạo ra môi trường năng động và nhập vai.
    




















3. **Địa hình và thảm thực vật**: CryENGINE cung cấp các công cụ để tạo môi trường ngoài trời rộng lớn và chi tiết. Nó hỗ trợ chỉnh sửa địa hình, bố trí thảm thực vật và hệ thống thời tiết năng động, cho phép các nhà phát triển tạo ra các bối cảnh ngoài trời mở rộng và thực tế.
    




















4. **Hoạt hình nhân vật**: CryENGINE bao gồm các công cụ mạnh mẽ dành cho hoạt hình nhân vật. Nó hỗ trợ các giàn nhân vật phức tạp, hoạt hình khuôn mặt và hệ thống cây hòa trộn cho phép các nhà phát triển tạo ra các chuyển động và hoạt ảnh nhân vật sống động như thật.
    




















5. **Hệ thống AI**: Công cụ có hệ thống AI cho phép tạo ra các NPC thông minh (nhân vật không phải người chơi) và AI của kẻ thù. Các nhà phát triển có thể lập kịch bản cho hành vi và tương tác của AI để tạo ra trải nghiệm chơi game đầy thử thách và hấp dẫn.
       





















6. **Kịch bản**: CryENGINE sử dụng ngôn ngữ kịch bản có tên "Schematyc" cho phép các nhà phát triển tạo ra các tương tác và logic trong trò chơi. Ngoài ra, nó còn hỗ trợ C++ cho các nhu cầu lập trình nâng cao hơn.

## Định dạng tệp được sử dụng bởi CryENGINE

Dưới đây là một số loại tệp phổ biến được liên kết với CryENGINE:

1. **cryproj**: Tệp dự án CryENGINE. Các tệp này lưu trữ các cài đặt và cấu hình dành riêng cho dự án cho dự án trò chơi cụ thể.
    




















2. **.level**: Tệp cấp độ chứa dữ liệu thế giới trò chơi 3D, bao gồm địa hình, vật thể, ánh sáng và các cài đặt dành riêng cho cấp độ khác. Cấp độ là thành phần cơ bản của thiết kế trò chơi trong CryENGINE.
    




















3. **.cgf**: Định dạng hình học ký tự. Các tệp này chứa dữ liệu mô hình 3D cho các nhân vật, đồ vật và nội dung trò chơi khác. Các tệp CGF có thể bao gồm dữ liệu hình học, kết cấu và hoạt ảnh.
    




















4. **.chrparams**: Tệp tham số ký tự. Các tệp này lưu trữ cài đặt và cấu hình cho mô hình nhân vật và hoạt ảnh của chúng.
    




















5. **.dds**: Định dạng họa tiết DirectX. CryENGINE thường sử dụng các tệp DDS để lưu trữ kết cấu, bao gồm bản đồ khuếch tán, bản đồ thông thường và các loại kết cấu khác.
    




















6. **.cryshader**: Tập tin CryENGINE Shader. Các tệp này xác định cách hiển thị vật liệu và đối tượng trong thế giới trò chơi, chỉ định trình đổ bóng, thuộc tính vật liệu, v.v.
    




















7. **.crytif**: Tệp thông tin kết cấu. Các tệp này lưu trữ thông tin bổ sung về kết cấu, chẳng hạn như cài đặt nén, mipmap và các chi tiết khác liên quan đến kết cấu.
    




















8. **.cdf**: Tệp định nghĩa ký tự. Các tệp CDF được sử dụng để xác định nội dung ký tự và thuộc tính của chúng, bao gồm tệp đính kèm, trạng thái hoạt ảnh và cài đặt liên quan đến ký tự.
    




















9. **.dds**: CryENGINE cũng sử dụng tệp DDS (DirectDraw Surface) cho các bản đồ kết cấu khác nhau, chẳng hạn như bản đồ thông thường, bản đồ cụ thể và bản đồ khuếch tán.
    




















10. **.anim**: Tệp hoạt hình. Các tệp này lưu trữ dữ liệu hoạt ảnh cho các ký tự và đối tượng, bao gồm khung hình chính, vị trí xương và chuỗi hoạt ảnh.
    




















11. **.xml**: Các tệp XML có thể được sử dụng cho nhiều cấu hình và định nghĩa dữ liệu khác nhau trong CryENGINE, chẳng hạn như logic trò chơi, hành vi AI, v.v.
    




















12. **.pak**: [Tệp PAK](/vi/game/pak/) là các tệp lưu trữ được sử dụng để đóng gói nội dung và tài nguyên trò chơi, giúp việc phân phối và tải trò chơi hiệu quả hơn.

## Làm cách nào để mở tệp CHR?

Các chương trình mở tệp CHR bao gồm

- **Crytek CryENGINE SDK** (Bản dùng thử miễn phí) cho Windows

**SubType:** Tệp hình ảnh 3D

## Các tệp CHR khác

Dưới đây là các loại tệp khác sử dụng phần mở rộng tệp **.chr**.

**3D**
- [CHR - Tệp ký tự CryENGINE](/vi/3d/chr-cryengine/)
- [CHR - Tệp ký tự tối đa 3ds](/vi/3d/chr-3ds/)

**Phông chữ & Trò chơi**
- [CHR - Bộ ký tự Borland](/vi/font/chr/)
- [CHR - Câu lạc bộ Văn học Doki Doki! Tệp ký tự](/vi/game/chr-doki/)

## Người giới thiệu
- [CryEngine](https://en.wikipedia.org/wiki/CryEngine)

