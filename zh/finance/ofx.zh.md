{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFX - 开放式金融交换文件格式",
  "description":"了解 OFX 文件格式以及可以创建和打开 OFX 文件的 API。",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## 什么是 .ofx 文件？

OFX（开放金融交换）文件是一种财务文件格式，用于在软件程序和金融机构之间交换财务信息。随着内部财务会计簿记软件解决方案的发展，已经开发出可以连接到您的银行并与银行导入或导出财务数据的软件程序。这包括交易、账户信息和账单支付等财务数据。 QuickBooks、Microsoft Money、Intuit 和 Quicken 等软件程序将导入的数据保存为 OFX 文件。

OFX 文件格式的 Internet 媒体类型是 application/x-ofx。

## OFX 文件格式

OFX 文件以 XML（可扩展标记语言）文件格式保存，并使用标签来构建数据。 [XML](/zh/web/xml/) 文件以人类可读的格式存储，可以在任何文本编辑器（例如记事本、Notepad++ 或 Apple TextEdit）中打开和编辑。 OFX 文件中存储的数据基于 **SGML（标准通用标记语言）** 标准。 OFX 文件中存储的数据通常包括：

* 银行相关信息
* 信用卡和借记卡信息
* 账户和投资信息
* 任何其他金融交易

### OFX 文件格式示例

以下是示例 OFX 文件的内部数据结构和示例数据。

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

此示例 OFX 文件包含以下信息：

* 银行账户信息，例如银行名称、账号、余额
* 交易列表，包括每笔交易的日期、类型和金额

所有这些信息都可以导入个人财务软件程序中，以跟踪帐户交易和费用。

## 参考 ＃＃

* [开放金融交易所 - 来自维基百科](https://en.wikipedia.org/wiki/Open_Financial_Exchange)
* [ISO 电子数据交换标准](https://en.wikipedia.org/wiki/ISO_20022)

