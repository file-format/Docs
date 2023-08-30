{
  "date" : "2020-11-11",
  "keywords" :[ "NDF", "확장자", "파일", "파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"NDF 파일을 만들고 열 수 있는 MDF 파일 형식과 API에 대해 알아보세요.",
  "title" :"NDF 파일 형식 - SQL Server 마스터 데이터베이스 파일",
  "linktitle" : "NDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## .NDF 파일이란?

확장자가 .ndf인 파일은 [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server)에서 사용자 데이터를 저장하는 데 사용하는 보조 데이터베이스 파일입니다. NDF는 SQL 서버가 사용자 지정 데이터를 [MDF](/ko/database/mdf/)라는 기본 저장 파일에 저장하기 때문에 보조 저장 파일입니다. NDF 데이터 파일은 선택 사항이며 기본 MDF 파일이 할당된 공간을 모두 사용하는 경우 데이터 저장소를 관리하기 위해 사용자 정의됩니다. 일반적으로 별도의 디스크에 저장되며 여러 저장 장치에 퍼질 수 있습니다. NDF 파일을 열려면 MDF 파일이 있어야 합니다.

## NDF 파일 형식

NDF 파일 형식은 [MDF](/ko/database/mdf/)와 다르지 않으며 페이지를 데이터 저장의 기본 단위로 사용합니다. 각 페이지는 다음을 포함하는 96바이트 헤더로 시작합니다.

* 페이지 ID
* 구조의 종류
* 페이지의 레코드 수
* 이전 및 다음 페이지에 대한 포인터

### NDF 파일 구조

MDF 파일의 데이터 구조는 다음과 같습니다.

* 페이지 0: 헤더
* 1페이지: 첫 번째 PFS
* 2페이지: 첫 번째 GAM
* 3페이지: 첫 번째 SGAM
* 4페이지: 미사용
* 5페이지: 미사용
* 6페이지: 첫 번째 DCM
* 7페이지: 첫 번째 BCM

#### NDF 파일 헤더

모든 파일의 페이지 번호 0에는 파일에 대한 메타데이터를 저장하는 헤더가 있습니다.

#### 페이지 여유 공간(PFS)
PFS는 할당 상태를 식별하고 여유 공간의 양을 결정합니다.

* Bit 1: 페이지 할당 여부를 나타냅니다.
* 비트 2: 페이지가 혼합 익스텐트에서 온 것인지 여부를 나타냅니다.
* 비트 3: 이 페이지가 IAM 페이지임을 나타냅니다.
* 비트 4: 이 페이지에 고스트 레코드가 포함되어 있음을 나타냅니다.
* 비트 5 ~ 7: 다음과 같이 페이지 충만도를 나타내는 결합된 3비트 값:
* 0: 페이지가 비어 있습니다.
* 1: 페이지가 1~50% 찼습니다.
* 2: 페이지가 51~80% 찼습니다.
* 3: 페이지가 81~95% 찼습니다.
* 4: 페이지가 96~100% 찼습니다.

## 데이터 파일 페이지

SQL Server 데이터 파일의 페이지는 0부터 시작하여 순차적으로 증가합니다. 각 파일은 고유한 파일 ID 번호로 인식됩니다. 파일 ID와 페이지 번호 쌍은 데이터베이스에서 페이지를 고유하게 식별합니다. 데이터베이스의 페이지 번호를 보여주는 예는 다음 이미지와 같습니다.

{{< figure src="../ndf.png" alt="NDF 데이터베이스 파일 형식" >}}

이 예는 4MB 기본 데이터 파일과 1MB 보조 데이터 파일이 있는 데이터베이스의 페이지 번호를 보여줍니다.

## 참고문헌

* [데이터베이스 파일 및 파일 그룹](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver16)
* [데이터베이스 분리 및 연결 - SQL Server](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server -ver15)
* [SQL Server 데이터 파일 분석 분석](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

