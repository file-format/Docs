{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp LOCK - Tệp khóa là gì?",
  "description":"Tìm hiểu về định dạng tệp LOCK và phần mở rộng của nó.",
  "linktitle" : "LOCK",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## Tệp KHÓA là gì?

Tệp **LOCK** là một tệp đã đổi tên được các ứng dụng và hệ điều hành sử dụng để đánh dấu một tệp hoặc một số thiết bị là bị khóa. Điều này yêu cầu các ứng dụng khác không sử dụng tệp trừ khi nó không có trong ứng dụng đang sử dụng nó. Trong hầu hết các trường hợp, các tệp khóa này trống nhưng trong các trường hợp khác, chúng có thể chứa thông tin liên quan đến khóa, chẳng hạn như thuộc tính và cài đặt.

Đôi khi, tệp .lock được .NET Framework của Microsoft sử dụng để tạo các bản sao **lockeed** của tệp cơ sở dữ liệu. Trong trường hợp này, một bản sao của tệp cơ sở dữ liệu sẽ mở với phần mở rộng .lock. Điều này không cho phép người dùng thực hiện các thay đổi đối với tệp trong khi tệp đang được người dùng khác sử dụng.

## Định dạng tệp LOCK - Thông tin khác

Một tệp LOCK được tạo bởi mỗi ứng dụng và định dạng tệp của nó dành riêng cho ứng dụng. Các tệp khóa này có thể được lưu ở cả định dạng văn bản cũng như tệp nhị phân.

Sự hiện diện của các tệp khóa ngăn truy cập đồng thời một tài nguyên vào nhiều tệp đang cố truy cập tài nguyên đó. Một bản sao của tệp gốc được tạo với phần mở rộng .lock ở sau tên của nó. Điều này báo cho các ứng dụng khác có quyền truy cập chỉ đọc vào tệp. Ví dụ: resource.dat sẽ trở thành resource.data.lock.

Đối với ngôn ngữ lập trình Ruby, bạn có thể bắt gặp tệp **gemfile.lock**. Đây là nơi Bundler ghi lại các phiên bản chính xác đã được cài đặt. Do đó, khi một dự án/thư viện được chuyển sang một máy khác, gói đang chạy sẽ xem xét Gemfile để biết chính xác phiên bản có liên quan.

## Khóa tệp trong Linux

Linux hỗ trợ hai loại khóa tệp: khóa tư vấn và khóa bắt buộc.

* **Advisory Locks**: Loại khóa không được thực thi. Trong trường hợp này, các quá trình tham gia hợp tác với nhau để có được các khóa một cách rõ ràng. Nếu điều này là không thể, khóa tư vấn sẽ bị bỏ qua.

* **Khóa bắt buộc**: Trong trường hợp Khóa bắt buộc, hệ điều hành thực thi khóa tệp bằng cách ngăn các quá trình khác đọc hoặc ghi tệp. Điều này không yêu cầu bất kỳ sự hợp tác nào giữa các quy trình.

khóa bắt buộc không yêu cầu bất kỳ sự hợp tác nào giữa các quy trình tham gia. Khi khóa bắt buộc được kích hoạt trên một tệp, hệ điều hành sẽ ngăn các quy trình khác đọc hoặc ghi tệp.

## Người giới thiệu

* [GemFile và Gemfile.lock trong Ruby](https://medium.com/never-hop-on-the-bandwagon/gemfile-and-gemfile-lock-in-ruby-65adc918b856)
* [Khóa trong Linux](https://www.baeldung.com/linux/file-locking#:~:text=File%20locking%20is%20a%20mechanism,very%20dangerous%20command%20in%20Linux.)

