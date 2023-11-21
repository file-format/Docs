{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFX - 개방형 금융 교환 파일 형식",
  "description":"OFX 파일 형식과 OFX 파일을 생성하고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## .OFX 파일이란?

OFX(Open Financial Exchange) 파일은 소프트웨어 프로그램과 금융 기관 간의 금융 정보 교환에 사용되는 금융 파일 형식입니다. 사내 재무 회계 장부를 위한 소프트웨어 솔루션이 발전함에 따라 은행에 연결하고 은행으로 재무 데이터를 가져오거나 내보낼 수 있는 소프트웨어 프로그램이 개발되었습니다. 여기에는 거래, 계좌 정보, 청구서 지불과 같은 금융 데이터가 포함됩니다. QuickBooks, Microsoft Money, Intuit 및 Quicken과 같은 소프트웨어 프로그램은 가져온 데이터를 OFX 파일로 저장합니다.

OFX 파일 형식의 인터넷 미디어 유형은 application/x-ofx입니다.

## OFX 파일 형식

OFX 파일은 XML(Extensible Markup Language) 파일 형식으로 저장되며 태그를 사용하여 데이터를 구조화합니다. [XML](/ko/web/xml/) 파일은 사람이 읽을 수 있는 형식으로 저장되며 메모장, Notepad++ 또는 Apple TextEdit과 같은 텍스트 편집기에서 열고 편집할 수 있습니다. OFX 파일 내부에 저장된 데이터는 **SGML(Standard Generalized Markup Language)** 표준을 기반으로 합니다. OFX 파일에 저장된 데이터는 일반적으로 다음과 같습니다.

* 은행관련 정보
* 신용카드 및 직불카드 정보
* 계좌 및 투자정보
* 기타 금융 거래

### OFX 파일 형식 예

다음은 OFX 파일 예시의 내부 데이터 구조와 샘플 데이터입니다.

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

이 예제 OFX 파일에는 다음 정보가 포함되어 있습니다.

* 은행명, 계좌번호, 잔고 등 은행계좌 정보
* 각 거래의 날짜, 유형 및 금액을 포함한 거래 목록

이 모든 정보는 개인 금융 소프트웨어 프로그램으로 가져와 계정 거래 및 비용을 추적할 수 있습니다.

## 참고자료 ##

* [개방형 금융 거래소 - Wikipedia 작성](https://en.wikipedia.org/wiki/Open_Financial_Exchange)
* [전자 데이터 교환을 위한 ISO 표준](https://en.wikipedia.org/wiki/ISO_20022)

