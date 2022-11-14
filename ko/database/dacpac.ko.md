{
  "date" : "2021-09-06",
  "keywords" :[ "dacpac", "확장자", "파일", "파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일 형식", "데이터 계층 응용 프로그램 패키지"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"DACPAC 파일을 만들고 열 수 있는 DACPAC 파일 형식 및 API에 대해 알아보세요.",
  "title" :"DACPAC - 데이터 계층 응용 프로그램 패키지",
  "linktitle" : "DACPAC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## .DACPAC 파일이란?

.dacpac(Data Tier AppliCation Package의 약자) 확장자를 가진 파일은 Microsoft SQL Server 데이터 계층 응용 프로그램으로 생성된 데이터베이스 파일로, 데이터베이스 개체 표현을 위한 데이터베이스 모델을 포함합니다. 데이터베이스의 전체 모델을 포함하므로 모델에서 사용 가능한 세부 정보에서 데이터베이스를 복원하는 데 사용됩니다. DACPAC 파일은 일반적으로 데이터베이스 복원을 위해 고객 구내에 설치하기 위해 배포 팀에 전달됩니다. 이것들은 다음과 같이 열 수 있습니다.
[마이크로소프트 SQL 서버 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019?ranMID=24542&ranEAID=4LioSo*jxMc&ranSiteID=4LioSo.jxMc-XSp30B6cXpiTS89wo0jYzw&Xpj3 =1&OCID=AID2200057_aff_7593_1243925&tduid=%28ir__gn1tqusqf0kf6whl2qniaboutn2xruqfmyy1hzec00%29%287593%29%281243925%29%284LioSo.jxMc-XSp30B6cXpiTS89wo0jYzw%29%28%29&irclickid=_gn1tqusqf0kf6whl2qniaboutn2xruqfmyy1hzec00).

## DACPAC 파일 형식 - 추가 정보

DACPAC 데이터 패키지 파일은 실제로 데이터베이스 복원에 사용되는 테이블 및 뷰와 같은 데이터베이스 모델에 대한 정보가 포함된 여러 [XML](/ko/web/xml/) 파일을 포함하는 압축된 ZIP 파일입니다. DACPAC 파일의 내용을 보려면 파일 이름을 .dacpac에서 [.zip](/ko/compression/zip/)으로 바꾸고 압축 해제 유틸리티를 사용하여 zip 아카이브를 추출합니다.

다음은 DACPAC 파일 내에서 발견되는 몇 가지 파일입니다.

* [콘텐츠 유형].xml
```
<?xml version="1.0" encoding="utf-8"?>
<Types
xmlns="http://schemas.openxmlformats.org/package/2006/content-types">
<Default Extension="xml" ContentType="text/xml" />
</Types>
```
* DacMetadata.xml

```
<?xml version="1.0" encoding="utf-8"?>
<DacType xmlns="http://schemas.microsoft.com/sqlserver/dac/Serialization/2012/02">
<Name>CRM</Name>
<Version>1.0.0.0</Version>
</DacType>
```
* 오리진.xml

* 모델.xml

DACPAC에는 DATA 및 기타 서버 수준 개체가 포함되어 있지 않습니다. 파일에는 SSDT 프로젝트에 보관될 수 있는 모든 개체 유형이 포함될 수 있습니다.

## 참고문헌

* [데이터 계층 응용 프로그램 - 이점](https://docs.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications?view=sql-server-ver15)
* [데이터 계층 애플리케이션 배포 - Microsoft](https://docs.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)
* [DACPAC 파일 생성은 어떻게 하나요?](https://sqlplayer.net/2018/10/how-to-create-dacpac-file/)

