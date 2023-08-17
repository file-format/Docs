{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp CRL - Danh sách thu hồi chứng chỉ",
  "description":"Tìm hiểu về định dạng tệp CRL và API có thể tạo và mở tệp CRL.",
  "linktitle" : "CRL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-01"
}

## Tệp CRL là gì?

Tệp CRL (Danh sách thu hồi chứng chỉ) là danh sách đen các chứng chỉ kỹ thuật số X.509 mà cơ quan cấp chứng chỉ (CA) thu hồi trước ngày thu hồi được chỉ định. Nó chứa thông tin về sự cố và ngày thu hồi cho phép quản trị viên bảo mật chặn các chứng chỉ kỹ thuật số bị ảnh hưởng. CRL không bao gồm các chứng chỉ đã hết hạn vì mục đích chính của nó là thông báo về các chứng chỉ không đáng tin cậy và không hợp lệ.

Các ứng dụng có thể **mở tệp CRL** bao gồm OpenSSL, Microsoft IIS Server và Citrix NetScaler.

## Định dạng tệp CRL - Thông tin khác

Các tệp CRL chứa thông tin trong tiêu chuẩn X.509 cũng xác định ngữ nghĩa của nó để chia sẻ thông tin khóa công khai. Các thông tin khác có trong tệp CRL có thể bao gồm giới hạn thời gian mà chứng chỉ đã bị thu hồi, lý do thu hồi, số sê-ri của chứng chỉ bị thu hồi và dấu thời gian.


### Lý do hàng đầu khiến chứng chỉ được thêm vào CRL

Có thể có một số lý do khiến chứng chỉ trang web của bạn bị thu hồi và được thêm vào CRL. Một số trong số họ có thể;

1. Khóa riêng của chứng chỉ của bạn đã bị xâm phạm
1. Chứng chỉ của bạn không hợp lệ hoặc do CA cấp sai
1. Chi tiết tổ chức liên quan đến chứng chỉ được thay đổi và CA cấp chứng chỉ mới
1. Bất kỳ lý do bất khả kháng nào khác khiến chứng chỉ bị thu hồi

## Người giới thiệu

* [Viện Tiêu chuẩn và Công nghệ Quốc gia (NIST)](https://csrc.nist.gov/glossary/term/CRL)
* [Lực lượng đặc nhiệm kỹ thuật Internet (IETF) RFC 5280](https://tools.ietf.org/html/rfc5280)
* [Danh sách thu hồi chứng chỉ](https://en.wikipedia.org/wiki/Certificate_revocation_list)

