{
"ngày": "2023-06-12",
  "keywords": [
"bak",
"tập tin bak",
"Dấu trang BAK Crom",
"tập tin bak là gì",
"cách mở tập tin bak",
"tài liệu",
"phần mở rộng tập tin bak",
"sự mở rộng"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Định dạng tệp BAK - Sao lưu dấu trang trên Chrome",
  "description":"Tìm hiểu về định dạng Dấu trang BAK Crom và các API có thể tạo và mở tệp BAK.",
  "linktitle": "BAK Chromium Bookmarks",
  "menu": {
    "docs": {
      "identifier": "misc-bak-chromium",
      "parent": "misc"
}
},
"lastmod": "2023-06-12"
}

## Tập tin BAK là gì?

Tệp .bak trong bối cảnh các trình duyệt web dựa trên Chrome, như Google Chrome và Microsoft Edge, về cơ bản là tệp sao lưu dấu trang của bạn. Các dấu trang này được lưu dưới dạng danh sách văn bản thuần túy và định dạng tệp được sử dụng là JSON. Mục đích của các tệp .bak này là để bảo vệ dấu trang của bạn bằng cách cung cấp bản sao lưu có thể được khôi phục trong trường hợp vô tình bị xóa hoặc bị mất.

Các trình duyệt dựa trên Chrome, bao gồm cả Google Chrome, thường xuyên tạo các tệp sao lưu này và thường đặt tên cho chúng là "Bookmarks.bak". Về cơ bản, chúng là ảnh chụp nhanh các dấu trang của bạn tại một thời điểm cụ thể.

## Cách sử dụng tệp .bak để khôi phục dấu trang của bạn

1. **Tìm tệp sao lưu:** Tệp này thường nằm trong thư mục cụ thể được liên kết với hồ sơ Chrome của bạn. Vị trí chính xác có thể khác nhau tùy thuộc vào hệ điều hành của bạn.

Trên Windows: Tìm trong `C:\Users\<YourUsername> \AppData\Local\Chromium\Dữ liệu người dùng\Mặc định\Bookmarks.bak`.

Trên macOS: Tìm kiếm trong `~/Library/Application Support/Chromium/Default/Bookmarks.bak`.

Trên Linux: Kiểm tra `~/.config/chromium/Default/Bookmarks.bak`.

3. Đảm bảo trình duyệt Chrome của bạn đã đóng.
4. Đổi tên tệp "Bookmarks.bak" bằng cách xóa phần mở rộng ".bak", do đó, nó được gọi đơn giản là "Dấu trang".
5. Khởi động Chrome.

Bằng cách đổi tên tệp .bak thành "Dấu trang", Chrome sẽ sử dụng tệp này làm tệp dấu trang hiện tại và các dấu trang trước đó của bạn sẽ được khôi phục.

## Sao lưu dấu trang Chrome

Sao lưu dấu trang Chrome của bạn là một biện pháp phòng ngừa khôn ngoan để đảm bảo bạn không bị mất các trang web và URL quan trọng đã lưu. Chrome là trình duyệt mã nguồn mở làm nền tảng cho các trình duyệt khác như Google Chrome và Microsoft Edge. Để sao lưu dấu trang Chrome của bạn, hãy làm theo các bước sau:

## Phương pháp 1: Sao lưu thủ công

1. **Mở Chrome**: Khởi chạy trình duyệt Chrome trên máy tính của bạn.

2. **Truy cập Dấu trang**: Nhấp vào ba dấu chấm dọc (biểu tượng menu) ở góc trên bên phải của cửa sổ trình duyệt. Từ menu thả xuống, di chuột qua "Dấu trang" để hiển thị menu con dấu trang.

3. **Xuất dấu trang**: Trong menu con dấu trang, nhấp vào "Trình quản lý dấu trang". Thao tác này sẽ mở một tab mới hiển thị dấu trang của bạn.

4. **Xuất dấu trang**: Trong tab trình quản lý dấu trang, hãy nhấp lại vào ba dấu chấm dọc (thường ở góc trên bên phải) để mở menu trình quản lý dấu trang. Từ menu này, chọn "Xuất dấu trang".

5. **Chọn vị trí**: Chọn nơi bạn muốn lưu tệp dấu trang đã xuất trên máy tính của mình. Tên tệp mặc định là "bookmarks.html", nhưng bạn có thể thay đổi tên nếu muốn. Lưu nó vào một vị trí bạn sẽ nhớ.

6. **Lưu**: Nhấp vào nút "Lưu" hoặc "Xuất" để lưu dấu trang của bạn dưới dạng tệp HTML.

Dấu trang của bạn hiện đã được sao lưu dưới dạng tệp HTML. Bạn có thể sao chép tệp này vào ổ đĩa ngoài hoặc bộ lưu trữ đám mây để lưu giữ an toàn.

## Cách 2: Đồng bộ với Tài khoản Google (nếu có)

Nếu bạn đã đăng nhập vào tài khoản Google trong Chrome, bạn cũng có thể sử dụng tính năng đồng bộ hóa tích hợp để giữ dấu trang của mình an toàn và đồng bộ hóa trên các thiết bị. Bằng cách này, dấu trang của bạn sẽ được tự động sao lưu vào tài khoản Google của bạn.

1. **Mở Chrome**: Khởi chạy trình duyệt Chrome và đảm bảo bạn đã đăng nhập vào tài khoản Google của mình.

2. **Bật đồng bộ hóa**: Nhấp vào ba dấu chấm dọc (biểu tượng menu) ở góc trên bên phải của cửa sổ trình duyệt và đi tới "Cài đặt".

3. **Đồng bộ hóa và các dịch vụ của Google**: Trong tab Cài đặt, nhấp vào "Đồng bộ hóa và các dịch vụ của Google" trên thanh bên trái.

4. **Đồng bộ hóa dữ liệu của bạn**: Trong "Đồng bộ hóa", hãy đảm bảo "Dấu trang" được bật. Điều này sẽ đồng bộ hóa dấu trang của bạn với tài khoản Google của bạn.

Dấu trang của bạn bây giờ sẽ được tự động sao lưu và đồng bộ hóa với tài khoản Google của bạn. Bạn có thể truy cập chúng bằng cách đăng nhập vào tài khoản Google của mình trên bất kỳ thiết bị nào có Chrome hoặc trình duyệt khác hỗ trợ đồng bộ hóa Google.

Hãy nhớ sao lưu định kỳ dấu trang của bạn theo cách thủ công, đặc biệt nếu bạn muốn có một bản sao cục bộ không chỉ phụ thuộc vào đồng bộ hóa tài khoản Google của bạn.

## Cách mở tệp BAK

Nếu bạn muốn khám phá dữ liệu thô của bản sao lưu dấu trang của mình, bạn có thể mở tệp "Bookmarks.bak" bằng nhiều trình soạn thảo văn bản khác nhau như Microsoft Visual Studio Code (có sẵn trên nhiều nền tảng), Microsoft Notepad (dành cho người dùng Windows), Apple TextEdit (dành cho người dùng Mac) hoặc bất kỳ trình soạn thảo văn bản nào khác mà bạn chọn. Làm như vậy sẽ cho phép bạn xem dấu trang và siêu dữ liệu có trong tệp.

Bạn có thể mở tệp "Bookmarks.bak" và xem nội dung của nó bằng nhiều phần mềm chỉnh sửa văn bản và trình chỉnh sửa mã khác nhau. Dưới đây là một số tùy chọn thường được sử dụng:

1. Mã Visual Studio (Mã VS)
2. Sổ tay (Windows)
3. Chỉnh sửa văn bản (Mac)
4. Văn bản tuyệt vời
5. Sổ tay++
6. Nguyên tử
7. nano và Vim (Linux)
8. WordPad (Windows)

## Các tập tin BAK khác

Dưới đây là các loại tệp khác sử dụng phần mở rộng tệp **.bak**.

**Cơ sở dữ liệu**
- [BAK - Tệp sao lưu cơ sở dữ liệu](/vi/database/bak/)
- [BAK - Đạo luật Swiftpage! Sao lưu cơ sở dữ liệu](/vi/database/bak-act/)
- [BAK - Sao lưu cơ sở dữ liệu Microsoft SQL Server](/vi/database/bak-sqlserver/)

**Trò chơi**
- [BAK - Thế giới Terraria hoặc Sao lưu người chơi](/vi/game/bak-terraria/)

**Khác**
- [BAK - Tệp sao lưu](/vi/misc/bak-backup/)
- [BAK - Sao lưu điểm chung kết 2012](/vi/misc/bak-finale/)
- [BAK - Sao lưu MobileTrans](/vi/misc/bak-mobiletrans/)
- [BAK - Sao lưu dự án video VEGAS](/vi/misc/bak-vegas/)

**Cài đặt**
- [BAK - Sao lưu trình khởi chạy Holo](/vi/settings/bak-holo/)

## Người giới thiệu
* [Chromium Bookmarks](https://www.chromium.org/user-experience/bookmarks/)
