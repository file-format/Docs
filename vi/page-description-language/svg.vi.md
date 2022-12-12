{
  "date" : "2020-03-02",
  "keywords" :[ "SVG", "file", "file format", "Page Description Language", "Scalar" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp SVG và API có thể tạo và mở tệp SVG.",
  "title" :"Tệp SVG là gì?",
  "linktitle" : "SVG",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2020-03-02"
}

## Tệp SVG là gì? ##

Tệp SVG là tệp Đồ họa vectơ vô hướng sử dụng định dạng văn bản dựa trên XML để mô tả giao diện của hình ảnh. Từ Có thể mở rộng đề cập đến thực tế là SVG có thể được thu nhỏ theo các kích thước khác nhau mà không làm giảm bất kỳ chất lượng nào. Mô tả dựa trên văn bản của các tệp như vậy làm cho chúng không phụ thuộc vào độ phân giải. Đây là một trong những định dạng được sử dụng nhiều nhất để xây dựng trang web và đồ họa in nhằm đạt được khả năng mở rộng. Tuy nhiên, định dạng này chỉ có thể được sử dụng cho đồ họa hai chiều. Các tệp SVG có thể được xem/mở trong hầu hết các trình duyệt hiện đại bao gồm Chrome, Internet Explorer, Firefox và Safari.

## Lược Sử ##

Thông số kỹ thuật SVG có sẵn dưới dạng tiêu chuẩn mở của World Wide Web Consortium (W3C) từ năm 1999. Trước đó, các thông số định dạng tệp tương tự ở sáu định dạng khác nhau đã được gửi tới W3C cho đến năm 1998. Một bản cập nhật đã được áp dụng cho các thông số kỹ thuật vào năm 2011 và nó là phiên bản 1.1 . Vào năm 2016, SVG 2 đã được xuất bản dưới dạng phiên bản mới hơn bao gồm các tính năng ngoài các tính năng trong SVG 1.1.

## Thông số kỹ thuật định dạng tệp ##

Mô hình đối tượng tài liệu SVG (DOM) đặt nền móng cho tất cả các thông số kỹ thuật và giao diện tương ứng với các phần cụ thể của thông số kỹ thuật. Trình xem SVG phải triển khai các giao diện SVG DOM như được xác định trong các thông số kỹ thuật của W3C. DOM của nó hiển thị một số giao diện cho các loại dữ liệu và phần tử khác nhau.

### Hình dạng SVG ###

SVG có một số yếu tố hình dạng được xác định trước mà các nhà phát triển có thể sử dụng:

* Hình chữ nhật<rect>
* Vòng tròn<circle>
* Hình elip<ellipse>
* Hàng<line>
* Đa tuyến<polyline>
* Đa giác<polygon>
* Đường dẫn<path>

Dựa trên các hình dạng và thông số kỹ thuật này, các khu vực chức năng của SVG như sau.

**Đường dẫn** - Đường dẫn được sử dụng để thể hiện các đường viền hình dạng đơn giản cũng như phức hợp. Mã hóa được sử dụng để xác định bản chất của hoạt động. Ví dụ: M được sử dụng để Di chuyển đến, L được sử dụng cho Đường đến, Z được sử dụng để đóng một đường dẫn, v.v.

**Hình dạng cơ bản** - Có thể vẽ các đường thẳng và đường dẫn được tạo thành từ một loạt các đoạn thẳng được kết nối (polylines), cũng như đa giác khép kín, hình tròn và hình elip. Hình chữ nhật và hình chữ nhật góc tròn cũng là các yếu tố tiêu chuẩn.

**Văn bản** - Trình bày văn bản được thể hiện dưới dạng dữ liệu ký tự XML trong đó có thể áp dụng nhiều hiệu ứng hình ảnh cho văn bản. Các thông số kỹ thuật cho phép xử lý văn bản hai chiều, văn bản dọc và ký tự dọc theo đường cong.

**Vẽ tranh** - Hình dạng có thể được tô và/hoặc viền bằng màu, dải màu hoặc hoa văn, cho phép khả năng làm cho hình dạng mờ đục hoặc có bất kỳ mức độ trong suốt nào. Các tính năng kết thúc dòng như đầu mũi tên hoặc biểu tượng xuất hiện ở các đỉnh của đa giác được biểu thị bằng Điểm đánh dấu.

**Màu** - Thông số kỹ thuật SVG cho phép áp dụng màu cho tất cả các thành phần SVG hiển thị, trực tiếp hoặc thông qua tô, nét và các thuộc tính khác. Các mã màu khác nhau có thể được sử dụng để chỉ định như đen hoặc xanh lam, biểu diễn hex, thập phân hoặc dưới dạng phần trăm của biểu mẫu RGB.

**Đường chuyển màu và mẫu** - Hình dạng trong tệp SVG có thể được tô hoặc viền bằng màu đồng nhất, chuyển màu hoặc mẫu lặp lại.

**Hiệu ứng bộ lọc** - Đây thực sự là một loạt các thao tác đồ họa được áp dụng cho đồ họa véc tơ nguồn đã cho để tạo ra kết quả đã sửa đổi.

**Tính tương tác** - Người dùng có thể tương tác với các tệp SVG bằng cách thay đổi tiêu điểm, nhấp chuột, cuộn hoặc phóng to hình ảnh. Tương tác cho phép hình ảnh SVG tương tác với người dùng theo nhiều cách khác nhau như đã nói ở trên.

**Liên kết** - Hình ảnh SVG có thể có siêu liên kết đến các tài liệu khác. Điều này đạt được thông qua Ngôn ngữ liên kết XML hoặc XLink. Điều này cho phép tạo các trạng thái chế độ xem cụ thể được sử dụng để phóng to/thu nhỏ một khu vực cụ thể hoặc để giới hạn chế độ xem đối với một phần tử cụ thể.

**Scripting** - Tương tự như HTML, tất cả các khía cạnh của tài liệu SVG đều có thể truy cập được để thao tác bằng cách sử dụng script. Các đối tượng SVG DOM cung cấp hướng dẫn để đạt được điều này bằng cách sử dụng phần tử và thuộc tính SVG. Các tập lệnh được đặt trong các phần tử thẻ `script` và có thể chạy để phản hồi các sự kiện về con trỏ, bàn phím hoặc tài liệu theo yêu cầu.

**Hoạt ảnh** - Các phần tử DOM<animate> ,<animateMotion> và<animateColor> cho phép bạn bao gồm hoạt ảnh cho nội dung SVG. Tất nhiên, điều này không thể đạt được nếu không sử dụng tập lệnh và bộ hẹn giờ tích hợp. Các hoạt ảnh này có thể liên tục và có thể được lặp lại cũng như lặp lại đồng thời phản hồi các sự kiện của người dùng.

**Phông chữ** - Văn bản trong SVG có thể tham chiếu các tệp phông chữ bên ngoài, chẳng hạn như phông chữ hệ thống. Trong trường hợp không có các phông chữ như vậy, văn bản trong SVG sẽ không được hiển thị ở đầu ra. Điều này có thể được khắc phục bằng cách kết hợp các nét tượng trưng cần thiết trong một tệp như vậy dưới dạng phông chữ, sau đó được hiển thị bằng cách sử dụng<text> yếu tố.

## Ví dụ ##
Các dòng sau đây cho biết cách một Vòng kết nối được biểu diễn bằng cách sử dụng tập lệnh SVG.

```
<html>
<body>

<h1>My first SVG</h1>

<svg width#"100" height#"100">
  <circle cx#"50" cy#"50" r#"40" stroke#"green" stroke-width#"4" fill#"yellow" />
</svg>

</body>
</html>
```

Các dòng mã sau đây cho thấy cách sử dụng<text> khối để hiển thị văn bản thành SVG.

```
<svg height#"30" width#"200">
  <text x#"0" y#"15" fill#"red">I love SVG!</text>
</svg>
```

## Người giới thiệu ##

* [Thông số SVG của W3C](https://www.w3.org/TR/SVG2/Overview.html)
* [SVG - Wikipedia](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics)

