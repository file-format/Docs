{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFX - オープン金融取引所ファイル形式",
  "description":"OFX ファイル形式と,OFX ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## OFX ファイルとは何ですか?

OFX (Open Financial Exchange) ファイルは、ソフトウェア プログラムと金融機関の間で財務情報を交換するために使用される財務ファイル形式です。社内財務会計簿記のためのソフトウェア ソリューションの進化に伴い、銀行に接続し、銀行と財務データをインポートまたはエクスポートできるソフトウェア プログラムが開発されました。これには、取引、アカウント情報、請求書の支払いなどの財務データが含まれます。 QuickBooks、Microsoft Money、Intuit、Quicken などのソフトウェア プログラムは、インポートされたデータを OFX ファイルとして保存します。

OFX ファイル形式のインターネット メディア タイプは application/x-ofx です。

## OFX ファイル形式

OFX ファイルは XML (Extensible Markup Language) ファイル形式で保存され、タグを使用してデータを構造化します。 [XML](/ja/web/xml/) ファイルは人間が判読できる形式で保存され、メモ帳、メモ帳++、Apple TextEdit などのテキスト エディタで開いて編集できます。 OFX ファイル内に保存されているデータは、**SGML (Standard Generalized Markup Language)** 標準に基づいています。 OFX ファイル内に保存されるデータには通常、次のものが含まれます。

※銀行に関する情報
* クレジットカードおよびデビットカード情報
* アカウントおよび投資情報
* その他の金融取引

### OFX ファイル形式の例

以下は、サンプル OFX ファイルの内部データ構造とサンプル データです。

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

この OFX ファイルの例には、次の情報が含まれています。

※銀行名、口座番号、残高などの銀行口座情報
* 各取引の日付、種類、金額を含む取引のリスト

このすべての情報を個人財務ソフトウェア プログラムにインポートして、口座取引と支出を追跡できます。

## 参考文献 ##

* [オープン金融取引所 - Wikipedia](https://en.wikipedia.org/wiki/Open_Financial_Exchange)
* [電子データ交換に関する ISO 規格](https://en.wikipedia.org/wiki/ISO_20022)

