{
  "date" : "2019-10-11",
  "keywords" :[ "tệp mpx", "định dạng tệp mpx", "tệp mpx là gì", "tệp", "ví dụ mpx", "phần mở rộng tệp mpx","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPX - Định dạng tệp Microsoft Project Exchange",
  "description":"Tìm hiểu về định dạng tệp MPX và API có thể tạo và mở tệp MPX.",
  "linktitle" : "MPX",
  "menu" : {
    "docs" : {
      "parent" : "project-management"
}
},
  "lastmod" : "2021-05-07"
}

## Tệp MPX là gì? ##

Tệp có phần mở rộng .mpx là Định dạng tệp Microsoft Exchange. Định dạng tệp MPX được Microsoft Project (MSP) phát triển để hỗ trợ trao đổi thông tin dự án giữa MSP và các ứng dụng khác hỗ trợ định dạng tệp MPX, bao gồm Primavera Project Planner, Sciforma và Timerline Precision Estimating. Sử dụng các tệp MPX, bạn có thể chuyển tất cả các loại thông tin từ một dự án sang một hệ thống khác, chẳng hạn như thông tin phân công tài nguyên chi tiết, thông tin lịch hoặc thông tin từ hộp thoại Thông tin dự án.

Microsoft Project 4.0 đã giới thiệu hỗ trợ tạo và đọc định dạng tệp MPX tiếp tục được sử dụng thông qua Microsoft Project 98. Tuy nhiên, hỗ trợ tạo tệp MPX đã ngừng phát hành Microsoft Project 2000 và các phiên bản cho đến Microsoft Project 2010 chỉ hỗ trợ đọc MPX. Định dạng tệp MPX không được hỗ trợ trong các phiên bản sau MSP 2010.

## Định dạng tệp MPX ##

Tổng quan về thông số kỹ thuật của tệp MPX được đưa ra trong phần này. Bạn có thể tìm thấy thông số kỹ thuật hoàn chỉnh trong [Cơ sở kiến thức] này(https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae) bài báo và có thể được giới thiệu để biết chi tiết.

### Hồ sơ ###

Bản ghi của tệp MPX bao gồm thông tin cho dự án. Có nhiều loại bản ghi khác nhau trong đó mỗi bản ghi có thứ tự riêng. Mỗi loại bản ghi được xác định bởi số bản ghi của nó. Đối với tệp MPX, cần phải chứa loại bản ghi Tạo tệp. Các loại hồ sơ khác không bắt buộc. Bảng sau đây hiển thị tất cả các loại bản ghi, số bản ghi của chúng và số lượng bản ghi mà mỗi loại có thể chứa trong tệp MPX. Việc đưa bản ghi vào tệp MPX phải tuân theo thứ tự bảng, với các nhận xét được chèn vào bất kỳ đâu.

|Tên bản ghi|Số bản ghi|Số bản ghi tối đa
---|---|---|
|Tạo tệp (bắt buộc)|không có|1
|Cài đặt tiền tệ|10|1
|Cài đặt mặc định|11|1
|Cài đặt ngày giờ|12|1
|Định nghĩa lịch cơ sở|20|250
|Giờ theo lịch cơ sở|25| 7 trên mỗi bản ghi Định nghĩa Lịch Cơ sở
|Ngoại lệ lịch cơ sở|26| 250 cho mỗi bản ghi Định nghĩa Lịch Cơ sở
|Tiêu đề dự án|30|1
|Định nghĩa bảng tài nguyên văn bản|140|1- (Hoặc bạn có thể sử dụng bản ghi Định nghĩa bảng tài nguyên số)
|Định nghĩa bảng tài nguyên số|41|1
|Tài nguyên|50|9,999
|Ghi chú Tài nguyên|51| 1 mỗi bản ghi Tài nguyên
|Định nghĩa lịch tài nguyên|55| 1 mỗi bản ghi Tài nguyên
|Tài nguyên Giờ Lịch|56| 7 mỗi Lịch tài nguyên
|Ngoại lệ lịch tài nguyên| 57|250 mỗi Lịch tài nguyên
|Định nghĩa bảng nhiệm vụ văn bản|60|1 (Hoặc bạn có thể sử dụng bản ghi Định nghĩa bảng nhiệm vụ số)
|Định nghĩa bảng nhiệm vụ số|61|1
|Nhiệm vụ|70|9
|Ghi chú Nhiệm vụ|71| 1 mỗi bản ghi Nhiệm vụ
|Nhiệm vụ định kỳ|72| 1 mỗi bản ghi Nhiệm vụ
|Phân công tài nguyên|75| 100 mỗi bản ghi Nhiệm vụ
|Các trường của nhóm làm việc được gán|76| 1 mỗi bản ghi Bài tập
|Tên dự án|80|500
|Liên kết Máy khách DDE và OLE|81|500
|Nhận xét|0|không giới hạn

### Cấu trúc tệp ###

Tệp MPX bao gồm các bản ghi được đề cập ở trên được sắp xếp theo cách đặt trước bên trong tệp. Chi tiết về các loại bản ghi này được thảo luận như sau:

**Bản ghi tạo tệp (FCR):** Đây là bản ghi bắt buộc nhằm mục đích xác định:

* Định dạng tệp (MPX)
* Liệt kê ký tự phân cách được sử dụng trong tệp
* Số chương trình và phiên bản được sử dụng để tạo tệp
* Số phiên bản của định dạng tệp MPX được sử dụng trong tệp
* Trang mã được sử dụng để tạo tệp

Đây phải là bản ghi đầu tiên trong tệp. Khi xuất từ Microsoft Project, ký tự phân tách danh sách được chỉ định trong mục Cài đặt khu vực trong Bảng điều khiển Windows. Bản ghi FCR bao gồm các trường sau:

* MPX ngay sau ký tự ngăn cách danh sách
* Tên/Số nhận dạng chương trình
* Số phiên bản của tệp
* Trang Mã (850, 437, MAC, ANSI)

Ví dụ: bản ghi có thể chứa thông tin **MPX, Microsoft Project, 3.0**, chỉ định rằng dấu phẩy được sử dụng làm ký tự phân cách danh sách trong tệp MPX này. Phiên bản của định dạng MPX được sử dụng trong tệp được xuất từ Microsoft Project phiên bản 3.0.

**Cài đặt tiền tệ** Bản ghi này, có bản ghi số 10, chỉ định cài đặt cho các tùy chọn tiền tệ trong hộp thoại Tùy chọn. Nếu bản ghi này không được bao gồm, cài đặt hiện tại trong hộp thoại Tùy chọn sẽ được sử dụng. Dấu phân cách Hàng nghìn và Số thập phân được chỉ định trong mục Cài đặt Khu vực trong Bảng Điều khiển Windows.
Các trường có trong bản ghi này là:

* Ký hiệu tiền tệ
* Vị trí ký hiệu (0 # sau, 1 # trước, 2 # sau có dấu cách, 3 # trước có dấu cách)
* Chữ số tiền tệ (0,1,2)
* Dấu phân cách hàng nghìn
* Phân số thập phân

**Ví dụ:** 10,$,1,2,",".
Ví dụ này chỉ định rằng các giá trị tiền tệ bao gồm ký hiệu đô la ($) trước chúng, hai chữ số được bao gồm sau dấu thập phân, dấu phẩy được sử dụng để phân tách hàng nghìn và dấu chấm được sử dụng làm dấu thập phân. Vì ký tự phân cách danh sách được bao gồm trong trường Dấu phân cách hàng nghìn, nên trường này được bao quanh bởi dấu ngoặc kép.

**Cài đặt mặc định:** Bản ghi này, có bản ghi số 11, chỉ định cài đặt cho các tùy chọn mặc định trong hộp thoại Tùy chọn. Nếu thời lượng không được chỉ định, Đơn vị thời lượng mặc định cần được đặt để tính toán đơn vị thời lượng chính xác. Nếu bản ghi này không được bao gồm, cài đặt hiện tại trong hộp thoại Tùy chọn sẽ được sử dụng.
Các trường có trong bản ghi này là:

* Đơn vị thời lượng mặc định (0 # phút, 1 # giờ, 2 # ngày, 3 # tuần)
* Loại thời lượng mặc định (0 # không cố định, 1 # cố định)
* Đơn vị công việc mặc định (0 # phút, 1 # giờ, 2 # ngày, 3 # tuần)
* Giờ/Ngày mặc định
* Số giờ/Tuần mặc định
* Tỷ lệ tiêu chuẩn mặc định
* Tỷ lệ làm thêm giờ mặc định
* Đang cập nhật trạng thái tác vụ Cập nhật trạng thái tài nguyên (0 # không, 1 # có)
* Tách nhiệm vụ đang thực hiện (0 # không, 1 # có)

**Cài đặt Ngày và Giờ:** Bản ghi này, có bản ghi số 12, chỉ định cài đặt cho tùy chọn ngày và giờ trong hộp thoại Tùy chọn và tùy chọn Định dạng Ngày Văn bản Thanh trong hộp thoại Bố cục. Nếu bản ghi này không được bao gồm, cài đặt hiện tại trong hộp thoại Tùy chọn sẽ được sử dụng.
\\Các trường có trong bản ghi này là:

* Thứ tự ngày (0 # tháng/ngày/năm, 1 # ngày/tháng/năm, 2 # năm/tháng/ngày)
* Định dạng thời gian (0 # 12 giờ, 1 # 24 giờ)
* Thời gian mặc định (số phút sau nửa đêm)
* Dấu tách ngày
* Dấu phân cách thời gian
* 0:00 đến 11:59 Văn bản
* 12:00 đến 23:59 Văn bản
* Định dạng ngày (0 -14)*
* Định dạng ngày văn bản thanh (0 -194)*

**Định nghĩa lịch cơ sở:** Những bản ghi này, có bản ghi số 20, xác định lịch cơ sở và các ngày làm việc cũng như không làm việc của chúng trong tuần. Cài đặt mặc định được sử dụng nếu không có mục nào trong một ngày. Cài đặt mặc định là từ Thứ Hai đến Thứ Sáu cho những ngày làm việc và Thứ Bảy và Chủ Nhật cho những ngày không làm việc. Trong bản ghi này, trường Tên là bắt buộc. Đối với mỗi ngày, mục nhập 0 cho biết ngày đó là ngày không làm việc và mục nhập 1 cho biết ngày đó là ngày làm việc.
Các trường có trong bản ghi này là:

* Tên
* Chủ nhật
* Thứ hai
* Thứ ba
* Thứ Tư
* Thứ năm
* Thứ sáu
* Thứ bảy

**Giờ theo lịch cơ sở:** Các bản ghi này, có số bản ghi 25, chỉ định giờ làm việc cho các ngày trong tuần nếu chúng khác với cài đặt mặc định. Giờ làm việc mặc định là 8:00 sáng đến 12:00 chiều và 1:00 chiều đến 5:00 chiều Mỗi bản ghi Giờ Lịch Cơ sở đề cập đến bản ghi Định nghĩa Lịch Cơ sở trước đó. Tối đa bảy bản ghi trong số này có thể theo sau mỗi bản ghi Định nghĩa Lịch Cơ sở.

* Ngày trong tuần (1 - 7, trong đó 1 # Chủ nhật và 7 # Thứ bảy)
* Từ lần 1
* Đến giờ 1
* Từ lần 2
* Đến Giờ 2
* Từ lần 3
* Đến Giờ 3

**Ngoại lệ Lịch Cơ sở:** Những bản ghi này, có số bản ghi 26, xác định các ngoại lệ đối với ngày và giờ được chỉ định trong hai loại bản ghi trước đó. Tối đa 250 bản ghi trong số này có thể theo sau mỗi bản ghi Định nghĩa Lịch Cơ sở. Những hồ sơ này phải được liệt kê theo thứ tự thời gian. Nếu trường hợp ngoại lệ là một ngày, bạn có thể để trống trường Đến Ngày. Nếu không có thời gian nào được chỉ định, thời gian mặc định là 8:00 sáng đến 12:00 trưa và 1:00 chiều đến 5:00 chiều sẽ được sử dụng.
Các trường có trong bản ghi này là:

* Từ ngày
* Đến nay
* Không hoạt động/Hoạt động (0 # không hoạt động, 1 # hoạt động)
* Từ lần 1
* Đến giờ 1
* Từ lần 2
* Đến Giờ 2
* Từ lần 3
* Đến Giờ 3

**Tiêu đề dự án:** Bản ghi này, có giá trị bản ghi 30, đặt các trường dự án chung, chẳng hạn như ngày bắt đầu dự án và ngày kết thúc dự án. Các trường trong bản ghi này tương ứng với thông tin trong hộp thoại Thông tin dự án và Thống kê.
Các trường và tab có trong bản ghi này là:

* Mục dự án
* Công ty
* Người quản lý
* Lịch (Sử dụng tiêu chuẩn nếu không có mục)
* Ngày bắt đầu (trường này hoặc trường tiếp theo được tính cho một tệp đã nhập, tùy thuộc vào cài đặt Lịch trình từ)
* Ngày kết thúc
* Lịch trình Từ (0 # bắt đầu, 1 # kết thúc)
* Ngay hiện tại*
* Bình luận
* Phí tổn
* Chi phí cơ bản
* Chi phí thực tế
* Công việc
* Công việc cơ bản
* Công việc thực tế
* Công việc
* Khoảng thời gian*
* Thời lượng cơ sở *
* Thời lượng thực tế
* Hoàn thành toàn bộ
* Bắt đầu cơ bản
* Kết thúc cơ bản
* Bắt đầu thực tế
* Kết thúc thực tế
* Bắt đầu phương sai
* Kết thúc phương sai
* Môn học
* Tác giả
* Từ khóa

**Định nghĩa bảng tài nguyên văn bản**: Bản ghi này liệt kê các trường tài nguyên, theo thứ tự, đang được nhập hoặc xuất. Đối với các tệp đã nhập, tên phải khớp với tên trường được sử dụng trong Microsoft Project. Đối với các tệp đã xuất, bản ghi này đến từ bảng Xuất tài nguyên. Phải sử dụng bản ghi này hoặc bản ghi Định nghĩa bảng tài nguyên số. Khi xuất từ Microsoft Project, cả hai bản ghi này đều được bao gồm.

**Định nghĩa bảng tài nguyên số:** Sử dụng số thay vì tên, bản ghi này liệt kê các trường tài nguyên, theo thứ tự, đang được nhập hoặc xuất. Đây là một phương pháp thay thế để xác định các trường tài nguyên có trong mỗi bản ghi Tài nguyên và rất hữu ích khi xác định tệp MPX được tạo bởi một sản phẩm tiếng nước ngoài.

**Tài nguyên:** Những bản ghi này chứa thông tin cho từng tài nguyên được nhập hoặc xuất. Mỗi bản ghi Tài nguyên mô tả một tài nguyên. Khi bạn nhập thông tin, các trường được bao gồm sẽ được xác định bởi bản ghi Định nghĩa Bảng Tài nguyên Văn bản hoặc bản ghi Định nghĩa Bảng Tài nguyên Số. Khi bạn xuất thông tin, các trường được bao gồm là những trường được liệt kê trong bảng Xuất tài nguyên.

**Ghi chú tài nguyên:** Những bản ghi này chứa các ghi chú về bản ghi tài nguyên ngay trước đó. Đối với một dòng mới trong ghi chú, ký tự ASCII 127 được sử dụng. Nếu ghi chú bao gồm ký tự phân tách danh sách, hãy đặt ghi chú trong dấu ngoặc kép.

**Định nghĩa Lịch Nguồn lực:** Những bản ghi này xác định ngày làm việc cho nguồn lực được chỉ định trong bản ghi Nguồn lực ngay trước đó. Đối với các tệp đã nhập, nếu không có mục nhập nào cho trường Tên Lịch Cơ sở, Tiêu chuẩn sẽ được sử dụng. Không có mục nào cho ngày cụ thể cho biết rằng ngày được đặt thành mặc định (2). Nếu không có bản ghi Định nghĩa Lịch Nguồn lực, Tiêu chuẩn được sử dụng làm lịch cơ sở cho nguồn lực, với mặc định được sử dụng cho các ngày. Đối với mỗi ngày, mục nhập 0 cho biết ngày đó là ngày không làm việc, 1 cho biết ngày đó là ngày làm việc và 2 chỉ định rằng giá trị mặc định được sử dụng.

**Giờ theo lịch của nguồn lực:** Những bản ghi này xác định giờ làm việc cho nguồn lực khác với lịch cơ sở được nguồn lực sử dụng. Các bản ghi này áp dụng cho bản ghi Định nghĩa lịch tài nguyên ngay trước bản ghi này. Tối đa bảy bản ghi trong số này có thể theo sau mỗi bản ghi Định nghĩa Lịch Nguồn lực.

**Ngoại lệ lịch tài nguyên:** Những bản ghi này xác định các ngoại lệ đối với ngày và giờ được chỉ định trong hai loại bản ghi trước đó. Tối đa 250 bản ghi trong số này có thể theo sau mỗi bản ghi Định nghĩa Lịch Nguồn lực. Những hồ sơ này phải được liệt kê theo thứ tự thời gian. Nếu ngoại lệ chỉ là một ngày, bạn có thể để trống trường Đến Ngày. Nếu không có thời gian nào được chỉ định, thời gian mặc định là 8:00 sáng đến 12:00 trưa và 1:00 chiều đến 5:00 chiều sẽ được sử dụng.

**Định nghĩa bảng tác vụ văn bản:** Bản ghi này liệt kê các trường tác vụ, theo thứ tự, đang được nhập hoặc xuất. Đối với các tệp đã nhập, tên phải khớp với tên trường được sử dụng trong Microsoft Project. Nếu tệp đang được xuất, bản ghi này đến từ bảng Xuất nhiệm vụ. Khi xuất từ Microsoft Project, cả hai bản ghi này đều được bao gồm. Các trường được tính toán bởi Microsoft Project, chẳng hạn như Bắt đầu theo lịch trình và Kết thúc theo lịch trình, sẽ bị bỏ qua nếu được nhập. Nếu bạn có ngày bắt đầu hoặc kết thúc nhiệm vụ cố định, hãy sử dụng các trường Loại ràng buộc và Ngày ràng buộc.

**Định nghĩa bảng nhiệm vụ số:** Sử dụng số thay vì tên, bản ghi này liệt kê các trường nhiệm vụ, theo thứ tự, đang được nhập hoặc xuất. Đây là một phương pháp thay thế để xác định các trường tác vụ có trong mỗi bản ghi Tác vụ và rất hữu ích khi xác định tệp MPX được tạo bởi một sản phẩm tiếng nước ngoài.

**Tác vụ:** Những bản ghi này chứa thông tin cho từng tác vụ được nhập hoặc xuất. Mỗi bản ghi Nhiệm vụ mô tả một nhiệm vụ. Khi bạn nhập thông tin, các trường được bao gồm sẽ được xác định bởi bản ghi Định nghĩa Bảng Tác vụ Văn bản hoặc bản ghi Định nghĩa Bảng Tác vụ Số. Khi bạn xuất thông tin, các trường được bao gồm là những trường được liệt kê trong bảng Xuất nhiệm vụ.

**Ghi chú Nhiệm vụ:** Những bản ghi này chứa các ghi chú về bản ghi Nhiệm vụ ngay trước đó. Sử dụng ký tự ASCII 127 để chỉ ra một dòng mới trong ghi chú. Nếu ghi chú bao gồm ký tự phân tách danh sách, hãy đặt ghi chú trong dấu ngoặc kép.

**Chỉ định tài nguyên**: Những bản ghi này liệt kê thông tin về các tài nguyên được chỉ định cho nhiệm vụ đã được xác định trong bản ghi Tác vụ trước đó. Nếu bạn đang hợp nhất các tệp và bạn muốn giữ lại thông tin gán tài nguyên, bạn cần đưa thông tin vào tệp MPX. Nếu bạn hợp nhất, tất cả các bài tập hiện có trên các nhiệm vụ đã hợp nhất sẽ bị xóa. Nếu bạn đang hợp nhất các tệp dựa trên ID duy nhất, tài nguyên sẽ được chỉ định bằng cách sử dụng ID duy nhất của tài nguyên thay vì ID.

**Trường nhóm làm việc chỉ định tài nguyên:** Các bản ghi này liệt kê thông tin được lưu trữ với mỗi nhiệm vụ cho các tính năng nhóm làm việc của Microsoft Project 4.0 và 4.1. Nếu bạn đang sử dụng các tính năng của Nhóm làm việc, bạn cần đưa vào bản ghi này để đảm bảo rằng không có thông tin nào bị mất.

**Tên dự án:** Những bản ghi này liệt kê tất cả các tên liên kết DDE được lưu trữ trong dự án.

**DDE và OLE Client Links:** Những bản ghi này liệt kê các liên kết DDE vào dự án.

**Nhận xét:** Những bản ghi này có thể được sử dụng để thêm nhận xét vào tệp và có thể xuất hiện ở bất kỳ vị trí nào trong tệp. Mỗi bản ghi Nhận xét phải bắt đầu bằng số "0".

## Sự cố khi mở tệp MPX ##

Dưới đây là danh sách một số vấn đề phổ biến có thể phát sinh và khiến định dạng MPX hoạt động sai:

* Không có phần mềm hỗ trợ
* Tập tin bị hỏng
* Tập tin bị nhiễm virus
* Không có quyền truy cập ngay trong hệ thống để mở tệp
* Ổ đĩa lỗi thời trong hệ thống của bạn
* Phần mở rộng của tệp được đổi tên

## Người giới thiệu ##

* [MPX - Cơ sở tri thức Microsoft](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae)

