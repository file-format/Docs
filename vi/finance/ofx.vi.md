{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFX - Định dạng tệp trao đổi tài chính mở",
  "description":"Tìm hiểu về định dạng tệp OFX và các API có thể tạo và mở tệp OFX.",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## Một tập tin OFX là gì?

Tệp OFX (Trao đổi tài chính mở) là định dạng tệp tài chính được sử dụng để trao đổi thông tin tài chính giữa các chương trình phần mềm và tổ chức tài chính. Với sự phát triển của các giải pháp phần mềm ghi sổ kế toán tài chính nội bộ, các chương trình phần mềm đã được phát triển có thể kết nối với ngân hàng của bạn và nhập hoặc xuất dữ liệu tài chính với ngân hàng. Điều này bao gồm dữ liệu tài chính như giao dịch, thông tin tài khoản và thanh toán hóa đơn. Các chương trình phần mềm như QuickBooks, Microsoft Money, Intuit và Quicken lưu dữ liệu đã nhập dưới dạng tệp OFX.

Loại phương tiện Internet cho định dạng tệp OFX là application/x-ofx.

## Định dạng tệp OFX

Các tệp OFX được lưu ở định dạng tệp XML (Ngôn ngữ đánh dấu mở rộng) và sử dụng các thẻ để cấu trúc dữ liệu. Các tệp [XML](/vi/web/xml/) được lưu trữ ở định dạng mà con người có thể đọc được và có thể mở và chỉnh sửa bằng bất kỳ trình soạn thảo văn bản nào như Notepad, Notepad++ hoặc Apple TextEdit. Dữ liệu được lưu trữ bên trong các tệp OFX dựa trên tiêu chuẩn **SGML (Ngôn ngữ đánh dấu tổng quát tiêu chuẩn)**. Dữ liệu được lưu trữ bên trong tệp OFX thường bao gồm:

* Thông tin liên quan đến ngân hàng
* Thông tin thẻ tín dụng và thẻ ghi nợ
* Thông tin tài khoản và đầu tư
* bất kỳ giao dịch tài chính nào khác

### Ví dụ về định dạng tệp OFX

Sau đây là cấu trúc dữ liệu nội bộ và dữ liệu mẫu của tệp OFX mẫu.

```
<?xml version="1.0" encoding="UTF-8" standalone="no"?>
<?OFX OFXHEADER="200" VERSION="211" SECURITY="NONE" OLDFILEUID="NONE" NEWFILEUID="12345678901234567890123456789012"?>
<OFX>
  <SIGNONMSGSRSV1>
    <SONRS>
      <STATUS>
        <CODE>0</CODE>
        <SEVERITY>INFO</SEVERITY>
        <MESSAGE>Successful Sign On</MESSAGE>
      </STATUS>
      <DTSERVER>20230510120000</DTSERVER>
      <LANGUAGE>ENG</LANGUAGE>
      <FI>
        <ORG>BANK NAME</ORG>
        <FID>123456789</FID>
      </FI>
    </SONRS>
  </SIGNONMSGSRSV1>
  <BANKMSGSRSV1>
    <STMTTRNRS>
      <TRNUID>1000000001</TRNUID>
      <STATUS>
        <CODE>0</CODE>
        <SEVERITY>INFO</SEVERITY>
        <MESSAGE>Successful Transaction</MESSAGE>
      </STATUS>
      <STMTRS>
        <CURDEF>USD</CURDEF>
        <BANKACCTFROM>
          <BANKID>987654321</BANKID>
          <ACCTID>123456789</ACCTID>
          <ACCTTYPE>CHECKING</ACCTTYPE>
        </BANKACCTFROM>
        <BANKTRANLIST>
          <DTSTART>20230501000000</DTSTART>
          <DTEND>20230510000000</DTEND>
          <STMTTRN>
            <TRNTYPE>DEBIT</TRNTYPE>
            <DTPOSTED>20230503000000</DTPOSTED>
            <TRNAMT>-100.00</TRNAMT>
            <FITID>1000000001</FITID>
            <NAME>Grocery Store</NAME>
          </STMTTRN>
          <STMTTRN>
            <TRNTYPE>CREDIT</TRNTYPE>
            <DTPOSTED>20230505000000</DTPOSTED>
            <TRNAMT>2000.00</TRNAMT>
            <FITID>1000000002</FITID>
            <NAME>Paycheck</NAME>
          </STMTTRN>
        </BANKTRANLIST>
        <LEDGERBAL>
          <BALAMT>5000.00</BALAMT>
          <DTASOF>20230510000000</DTASOF>
        </LEDGERBAL>
      </STMTRS>
    </STMTTRNRS>
  </BANKMSGSRSV1>
</OFX>
```

Tệp OFX ví dụ này chứa thông tin sau:

* Thông tin tài khoản ngân hàng như tên ngân hàng, số tài khoản và số dư
* Danh sách các giao dịch bao gồm ngày, loại và số tiền của mỗi giao dịch

Tất cả thông tin này có thể được nhập vào chương trình phần mềm tài chính cá nhân để theo dõi các giao dịch và chi phí tài khoản.

## Người giới thiệu ##

* [Sàn giao dịch tài chính mở - Theo Wikipedia](https://en.wikipedia.org/wiki/Open_Financial_Exchange)
* [Tiêu chuẩn ISO về trao đổi dữ liệu điện tử](https://en.wikipedia.org/wiki/ISO_20022)

