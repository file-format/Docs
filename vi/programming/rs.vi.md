{
  "date" : "2021-09-01", 

  "keywords" :[ "RS", "file", "extension", "file format", "Rust programming language", "Programming Guide", "RS example", "Rust", "VBScript" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RS - Tệp lập trình Rust",
  "description":"Tìm hiểu về định dạng tệp RS và API có thể tạo và mở tệp RS.",
  "linktitle" : "RS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-01"
}

## Tệp RS là gì?

Một tệp có phần mở rộng RS thuộc về ngôn ngữ lập trình Rust, nó là một ngôn ngữ lập trình đa mô hình, cấp cao, có mục đích chung, được thiết kế cho hiệu suất và an toàn, đặc biệt là an toàn về mặt tiền tệ. Rust về mặt cú pháp tương tự như С++ nhưng có thể đảm bảo an toàn bộ nhớ bằng cách sử dụng trình kiểm tra lỗi để xác thực các tham chiếu. Ngôn ngữ rỉ sét đạt được sự an toàn cho bộ nhớ mà không cần bộ sưu tập rác và tính năng tham chiếu là bắt buộc.

## Định dạng tệp RS ##

Rust ban đầu được thiết kế bởi Graydоn Hоаre tại Mоzillа Research, với sự đóng góp của Dave Herman, Brendan Eich và những người khác. Nó đã được sử dụng ngày càng nhiều trong công nghiệp và Microsoft đã và đang thử nghiệm ngôn ngữ dành cho các thành phần phần mềm quan trọng và an toàn.

Rust đã được bình chọn là "ngôn ngữ lập trình được yêu thích nhất" trong Cuộc khảo sát dành cho nhà phát triển Оverflow của Stack mỗi năm kể từ năm 2016, mặc dù chỉ được sử dụng bởi 7% số người được hỏi trong cuộc khảo sát năm 2021. Cùng với kiểu gõ thống kê thông thường, trước phiên bản 0.4, Rust cũng hỗ trợ các kiểu đánh máy.

Hệ thống đánh máy đã mô hình hóa các xác nhận trước và sau các câu lệnh của chương trình, thông qua việc sử dụng một câu lệnh kiểm tra đặc biệt. Sự khác biệt có thể được phát hiện tại thời điểm biên dịch, thay vì tại thời điểm chạy, như trường hợp có thể xảy ra với các xác nhận trong mã С оhoặc С++. Kiểu đánh máy không phải là duy nhất đối với Rust, vì nó lần đầu tiên được giới thiệu bằng ngôn ngữ NIL. Các đánh máy đã bị loại bỏ vì trong thực tế, chúng ít được sử dụng, mặc dù có thể đạt được chức năng tương tự bằng cách tận dụng các ngữ nghĩa di chuyển của Rust.

Ngôn ngữ lập trình Rust giúp bạn viết phần mềm nhanh hơn, đáng tin cậy hơn. Công thái học cấp cao và kiểm soát cấp thấp thường là những điểm khác biệt trong thiết kế ngôn ngữ lập trình; Rỉ sét thách thức điều đó. Thông qua khả năng cân bằng kỹ thuật mạnh mẽ và kinh nghiệm của một nhà phát triển tuyệt vời, Rust cung cấp cho bạn tùy chọn để kiểm soát các chi tiết cấp thấp (chẳng hạn như sử dụng bộ nhớ) mà không gặp rắc rối với truyền thống được bảo vệ.

 

## Lược Sử ##

Ngôn ngữ phát triển từ một dự án cá nhân bắt đầu vào năm 2006 bởi nhân viên của Mоzillа, Greydоn Hоаre, người đã tuyên bố rằng dự án này có thể được đặt tên theo tên của họ nấm gỉ sắt. Mоzillа bắt đầu tài trợ cho dự án này vào năm 2009 và công bố nó vào năm 2010. Rust 1.0, bản phát hành ổn định đầu tiên, được phát hành vào ngày 15 tháng 5 năm 2015. Sau 1.0, các bản phát hành ổn định được phát hành sáu tuần một lần, trong khi các tính năng về đêm của Rusted dần dần biến mất các bản phát hành, sau đó được thử nghiệm với các bản phát hành thử nghiệm kéo dài sáu tuần. Vào ngày 6 tháng 4 năm 2021, Gооgle đã công bố hỗ trợ chưa được công bố cho Rust trong Аndrоid Open Sоsource Рrоjeсt như một giải pháp thay thế cho С/С++.

## Đặc điểm kỹ thuật ##

Rust nhằm mục đích trở thành ngôn ngữ cho các hệ thống có độ an toàn cao và hiện tại cao, cũng như lập trình trên diện rộng, tức là tạo và duy trì các ranh giới bảo vệ tính toàn vẹn của hệ thống lớn. Điều này đã dẫn đến một bộ tính năng chú trọng đến tính an toàn, khả năng kiểm soát bố cục bộ nhớ và tính chính xác.


Ngôn ngữ Rust được thiết kế để đảm bảo an toàn cho bộ nhớ. Nó không cho phép các con trỏ null, con trỏ lủng lẳng hoặc các cuộc đua dữ liệu. Các giá trị dữ liệu chỉ có thể được khởi tạo thông qua một tập hợp các biểu mẫu cố định, tất cả các biểu mẫu này đều yêu cầu đầu vào của chúng phải được khởi tạo sẵn. Để tái tạo các роinters là hợp lệ hoặc NULL, chẳng hạn như trong danh sách được liên kết hoặc cấu trúc dữ liệu cây nhị phân, thư viện của Rust cung cấp một loại tùy chọn. Rust đã thêm cú pháp để quản lý thời gian tồn tại. Mã không an toàn có thể phá bỏ một số hạn chế này bằng cách sử dụng từ khóa không an toàn.


Ngôn ngữ Rust không sử dụng bộ sưu tập rác tự động. Bộ nhớ và các tài nguyên khác được quản lý thông qua tính năng truy xuất tài nguyên là một tính năng khởi tạo, với tính năng tham chiếu tùy chọn.


Rust cung cấp khả năng quản lý tài nguyên có tính quyết định với chi phí rất thấp. Rust ủng hộ phân bổ giá trị và không thực hiện quyền anh ngầm. Có một số tham chiếu (sử dụng ký hiệu), không liên quan đến việc đếm tham chiếu trong thời gian chạy. Sự an toàn của những người theo dõi như vậy được xác minh tại thời điểm biên dịch, ngăn chặn những người theo dõi lơ lửng và các dạng hành vi không xác định khác.


Rust có một hệ thống quyền sở hữu trong đó tất cả các giá trị đều có một chủ sở hữu duy nhất. Các giá trị có thể được chuyển bởi tham chiếu bất biến, sử dụng &T, bởi tham chiếu có thể thay đổi, sử dụng & mut T, hoặc theo giá trị, sử dụng T. Trình biên dịch Rust thực thi các quy tắc này tại thời điểm cố định và đồng thời kiểm tra tất cả các tham chiếu đều hợp lệ.


## Ví dụ về định dạng tệp RS ##

```
use serde::{Serialize, Deserialize};

#[derive(Serialize, Deserialize, Debug)]
struct Point {
    x: i32,
    y: i32,
}

fn main() {
    let point = Point { x: 1, y: 2 };

    let serialized = serde_json::to_string(&point).unwrap();
    println!("serialized = {}", serialized);

    let deserialized: Point = serde_json::from_str(&serialized).unwrap();
    println!("deserialized = {:?}", deserialized);
}
```

## Tài liệu tham khảo ##

* [RS - theo Wikipedia](https://en.wikipedia.org/wiki/Rust_(programming_language))



