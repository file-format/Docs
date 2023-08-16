{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRLファイル - 証明書失効リスト",
  "description":"CRL ファイル形式と,CRL ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "CRL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-01"
}

## CRLファイルとは何ですか?

CRL (Certificate Revocation List) ファイルは、割り当てられた失効日より前に認証局 (CA) が失効する X.509 デジタル証明書のブラックリストです。これには、セキュリティ管理者が影響を受けるデジタル証明書をブロックできるようにする、問題と失効日に関する情報が含まれています。 CRL の主な目的は、信頼されていない無効な証明書について通知することであるため、期限切れの証明書は含まれません。

**CRL ファイルを開く**ことができるアプリケーションには、OpenSSL、Microsoft IIS Server、および Citrix NetScaler が含まれます。

## CRL ファイル形式 - 詳細情報

CRL ファイルには、公開鍵情報を共有するためのセマンティクスも定義する X.509 標準の情報が含まれています。 CRL ファイル内に含まれるその他の情報には、証明書が取り消された期限、取り消しの理由、取り消された証明書のシリアル番号、およびタイムスタンプが含まれる場合があります。


### 証明書が CRL に追加される主な理由

Web サイトの証明書が取り消され、CRL に追加される理由はいくつか考えられます。それらのいくつかは可能性があります。

1. 証明書の秘密鍵が侵害された
1.証明書が無効であるか、CA によって誤って発行された
1. 証明書に関連する組織の詳細が変更され、CA が新しい証明書を発行する
1. その他やむを得ない事由により証明書を取り消された場合

## 参考文献

* [国立標準技術研究所 (NIST)](https://csrc.nist.gov/glossary/term/CRL)
* [インターネット技術特別調査委員会 (IETF) の RFC 5280](https://tools.ietf.org/html/rfc5280)
* [認証失効リスト](https://en.wikipedia.org/wiki/Certificate_revocation_list)

