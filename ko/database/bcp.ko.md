{
  "date" : "2020-11-11",
  "keywords" :[ "BCP", "확장자", "파일", "파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"BCP 파일 형식과 BCP 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"BCP - SQL Server 대량 복사 파일 형식",
  "linktitle" : "BCP",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## .BCP 파일이란?

BCP(대량 복사 형식)는 가져오기/내보내기를 위해 서로 다른 데이터베이스 데이터 유형 값을 저장하기 위한 데이터 구조를 정의하는 Microsoft SQL Server의 기술 데이터 형식입니다. 형식은 데이터 파일에 지정된 값 집합을 읽을 수 있도록 각 데이터 열의 해석을 완전히 정의합니다. [BCP](https://learn.microsoft.com/en-us/previous-versions/sql/sql-server-2008-r2/ms162802(v=sql.105)) 유틸리티는 BCP 파일 형식을 사용하여 그러한 파일에서 데이터를 찾아 식별합니다.


## BCP 파일 형식

BCP 형식 파일은 열 순서, 이름 및 데이터 유형을 정의하는 XML 문서입니다. 이를 통해 사용자는 이러한 필드를 지정하는 데이터 파일에서 많은 양의 데이터를 가져오거나 내보낼 수 있습니다. 이는 데이터 파일에서 데이터 값을 대량으로 가져올 때 유용합니다. 데이터 파일의 데이터 필드 수와 순서는 대상 테이블 열의 데이터 필드와 다를 수 있습니다. BCP 데이터 형식 파일이 데이터를 가져올 열의 순서와 유형을 지정하여 도움이 되는 경우입니다.

형식 파일의 구조는 다음 형식으로 표시됩니다.

```
<BCPFORMAT ...>
    <RECORD>
       <FIELD ID = "fieldID" xsi:type = "fieldType" [...] />
    </RECORD>
    <ROW>
       <COLUMN SOURCE = "fieldID" NAME = "columnName" xsi:type = "columnType" [...]  />
    </ROW>
 </BCPFORMAT>
```

### BCP 데이터 유형

|데이터 유형|범위|표현|
---|---|---|
|BigInt|-263(-9,223,372,036,854,775,808) ~ 263-1(9,223,372,036,854,775,807)|`BigInt = ["-"]1*19DIGIT`|
|이진|1 ~ 8000바이트|16진법으로 인코딩된 유니코드 문자열 형식 `Binary = 32000OCTET`|
|비트|0 또는 1|단순 유니코드 문자열 Bit = "0" / "1"|
|Char|1 ~ 8000|유니코드 문자열 형식, Char = 16000OCTET|
|CLRUDT|VarBinary|CLRUDT = 0*nOCTET, n = 4 x (2,147,483,647)|
|날짜|0001-01-01 ~ 9999-12-31|YYYY-MM-DD 문자열 형식|
|날짜시간|1753-01-01 00:00:00.000 ~ 9999-12-31 23:59:59.997| 유니코드 YYYY-MM-DD hh:mm:ss[.nnn] 문자열 형식|
|DateTime2|0001-01-01 00:00:00.0000000 ~ 9999-12-31 23:59:59.9999999.| 유니코드 YYYY-MM-DD hh:mm:ss[.nnnnnnn] 문자열 형식|
|DateTimeOffset|0001-01-01 00:00:00.0000000 ~ 9999-12-31 23:59:59.9999999(협정 세계시) 표준시| 유니코드 YYYY-MM-DD hh:mm:ss[.nnnnnnn] [{+|-}hh:mm] 문자열 형식|
|십진수|-1038 + 1 ~ 1038 – 1|유니코드 문자열 형식 `십진수 = ["-"] 0*38DIGIT ["."0*38DIGIT]`|
|Float|-1.79E+308 ~ -2.23E-308; 0; 2.23E-308부터 1.79E+308까지|유니코드 문자열 형식|
|이미지|0에서 231 사이의 바이트 시퀀스 – 1(2,147,483,647)|16진법으로 인코딩된 유니코드 문자열 형식|
|Int|-231(-2,147,483,648) ~ 231 – 1(2,147,483,647)|유니코드 문자열 형식|

## 참고문헌

* [BCP 형식 - Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)

