{
  "date" : "2020-11-11",
  "keywords" :[ "DTSX", "phần mở rộng", "tệp", "định dạng tệp", "Loại tệp cơ sở dữ liệu", "Định dạng tệp cơ sở dữ liệu", "Tệp cơ sở dữ liệu" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp DTSX và các API có thể tạo và mở tệp DTSX.",
  "title" :"Định dạng tệp DTSX - Tệp cài đặt DTS của SQL Server",
  "linktitle" : "DTSX",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Tệp DTSX là gì?

Tệp có phần mở rộng .dtsx (XML gói dịch vụ chuyển đổi dữ liệu) là tệp Dịch vụ chuyển đổi dữ liệu (DTS) được Microsoft SQL sử dụng để tham khảo các bước/quy tắc di chuyển dữ liệu để truyền dữ liệu từ cơ sở dữ liệu này sang cơ sở dữ liệu khác. Điều này bao gồm các phép biến đổi và bất kỳ bước xử lý tùy chọn nào có thể được yêu cầu trong quá trình truyền dữ liệu giữa điểm gốc và điểm đích. Dịch vụ tích hợp máy chủ SQL (SSIS), một thành phần của Microsoft SQL Server, sử dụng các tệp DTSX để xác định các bước xử lý dữ liệu giữa các máy chủ cơ sở dữ liệu. Các tệp DTSX có thể được mở bằng Microsoft SQL Server 2019.

## Định dạng tệp DTSX

Việc di chuyển dữ liệu giữa các máy chủ cơ sở dữ liệu cần có các quy tắc và các bước xử lý để đảm bảo tính toàn vẹn của dữ liệu trong quá trình vận hành này. SSIS đảm bảo rằng tất cả các hoạt động này, để di chuyển và điều chỉnh dữ liệu từ các nguồn khác nhau trong doanh nghiệp, diễn ra thuận tiện. Đó là nơi DTSX xác định các cấu trúc sẽ được SSIS sử dụng để thiết lập các bước trong đó dữ liệu có thể được xử lý khi thực hiện theo các bước này.

Luồng dữ liệu được mô tả bởi DTSX như trong hình dưới đây.

{{< figure src="../DataFlowDTSX.png" alt="Luồng dữ liệu DTSX" >}}

DTSX dựa trên [XML](/vi/web/xml/) và được ghi lại trong [MS-DTSX](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd). Việc tái cấu trúc nâng cao của DTSX XML là DTSX 2.0 bao gồm các thuộc tính mới cho cấu trúc, thay thế các thuộc tính được đặt tên làm thuộc tính XML gốc, chỉ định các giá trị mặc định cho hầu hết các giá trị thuộc tính và vị trí của các phần tử lặp lại bên trong phần tử gốc. Cấu trúc DTSX được mô tả bằng [Lược đồ XML](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/e5095968-26ea-4824-a717-153ccee642dc) này và định dạng cấu trúc là XML văn bản rõ ràng.

## Người giới thiệu

* [Định dạng DTSX - Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)
* [Định dạng DTSX 2 - Bởi Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx2/fb216aa4-62ab-41c8-a6d5-5b1002739d21)

