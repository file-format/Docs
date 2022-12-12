{
  "date" : "2019-10-11",
  "keywords": [ "M file", "M", "extension", "format", "M file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M - Tệp mã nguồn Matlab",
  "description":"Tìm hiểu về tệp Mã nguồn Matlab .m và các API có thể tạo và mở tệp MF.",
  "linktitle" : "M",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

# M - Tệp mã nguồn Matlab

## Tệp M (Matlab) là gì?

Tệp có phần mở rộng .m là tệp mã nguồn được sử dụng bởi Matlab, một nền tảng tính toán số và lập trình được sử dụng để phân tích, phát triển thuật toán và lập mô hình mô phỏng. Giống như các định dạng tệp lập trình khác, tệp M chứa mã nguồn thực thi các lệnh Matlab để vẽ biểu đồ, chạy mô phỏng và các hoạt động toán học khác. Một mô phỏng Matlab duy nhất có thể mở rộng trên nhiều tệp .m như vậy có thể phân loại ứng dụng theo tập lệnh, lớp, hàm hoặc khai báo. Các tệp Matlab M có thể được mở bằng bất kỳ trình soạn thảo văn bản nào.

## Định dạng tệp Matlab M - Thông tin thêm

Tệp Matlab .m là tệp văn bản chứa mã lập trình bằng ngôn ngữ lập trình Matlab. Chúng có thể được mở và chỉnh sửa trong bất kỳ trình soạn thảo văn bản nào và được lưu lại để thực thi trong phần mềm Matlab. Bản thân Matlab chứa một Live Editor được sử dụng để tạo các tập lệnh là sự kết hợp của mã, đầu ra và văn bản được định dạng.

### Tệp chức năng Matlab

Giống như các ngôn ngữ lập trình khác, bạn có thể tạo một tệp .m chỉ chứa định nghĩa của một hàm chỉ thực hiện một tác vụ cụ thể. Các tệp như vậy cũng được lưu với phần mở rộng .m và chỉ thực hiện chức năng liên quan đến chức năng đó.

### Ví dụ về tệp .M

Sau đây là một ví dụ về tệp hàm Matlab tính thời gian vật rơi từ độ cao h.

```C++
function t= TimeToGround(h)  
  t=sqrt(h/4.9);
end
```

Để gọi chức năng này từ trình soạn thảo Matlab hoặc từ tệp .m khác, có thể sử dụng đoạn mã sau.
```C++
TimeToGround(100)
```

## Người giới thiệu

* [Matlab - Định dạng tệp được hỗ trợ](https://www.mathworks.com/help/matlab/standard-file-formats.html)
* [Sử dụng Matlab](https://www.maths.unsw.edu.au/sites/default/files/MatlabSelfPaced/lesson0/MatlabLesson0_Mfiles.html)

# M - Tệp triển khai Mục tiêu-C

## Tệp M (Objective-C) là gì?

Tệp M còn được gọi là tệp triển khai chứa mã nguồn của một lớp được viết bằng ngôn ngữ Objective-C, ngôn ngữ lập trình được sử dụng để viết các ứng dụng phần mềm cho OS X và iOS. Objective-C là ngôn ngữ lập trình chính được sử dụng bởi các API chính của Apple, Cocoa và Cocoa Touch, cho các nền tảng này. Một ứng dụng phần mềm duy nhất được phát triển bằng ngôn ngữ này có thể chứa nhiều tệp .m, chứa việc triển khai các lớp chương trình. Chúng có thể được mở bằng Apple XCode, jEdit và các trình soạn thảo văn bản phổ biến khác.

## Định dạng tệp Mục tiêu-C M - Thông tin khác

Các tệp M được viết ở định dạng văn bản thuần sử dụng cú pháp lập trình của Objective-C. Mọi phương thức của một lớp phải được định nghĩa với tất cả mã cần thiết của nó trong các tệp triển khai này. Các tệp M triển khai này có thể nhập một hoặc nhiều tệp tiêu đề .h theo yêu cầu. Câu lệnh nhập cho trình biên dịch biết nơi tìm tệp tiêu đề thuộc về tệp triển khai này. Câu lệnh nhập khẩu được viết như sau.

```C++
#import "network.h"
```

Sau đó, mỗi triển khai tệp M bắt đầu bằng chỉ thị `@implementation`, theo sau là tên tệp lớp triển khai. Sau đó, điều này được theo sau bởi tất cả các triển khai phương thức được khai báo trong tệp tiêu đề.

### Ví dụ định dạng tệp M

```C++
UrlConnection.m

#import "UrlConnection.h"

@implementation UrlConnection

(void)connect {
    // In here would be code to attempt a connection to the
    // specified URL, while possibly handling connection errors.
    //
}

 + (BOOL)canHandleRequest:(NSString \*)type
                   forUrl:(NSString \*)url {
    //And in here would be code to see if the given URL passed
    // in is capable of handling the HTTP request type specified
    // by the "type" parameter. It will return YES or NO.
 }

 @end
```

## Người giới thiệu
* [Giới thiệu về Mục tiêu C](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011210-CH1-SW1)
* [Hướng dẫn đối tượng-C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

