{
  "date" : "2021-08-24",
  "keywords" :[ "trc 파일", "trc 파일 형식", "trc 파일이란", "파일", "trc 예제", "trc 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"TRC 파일 형식과 TRC 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"TRC - SQL Server 추적 파일",
  "linktitle" : "TRC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## .TRC 파일이란?
확장자가 .trc인 파일에는 Miscrosoft SQL Server 데이터베이스 활동의 추적 결과가 포함되어 있습니다. 이러한 파일은 소프트웨어 SQL Server 프로파일러에 의해 생성됩니다. 일반적으로 Microsoft SQL Server 소프트웨어와 함께 패키지로 제공됩니다. 데이터베이스 관리자는 일련의 데이터베이스 명령문을 분석하고 어떤 종류의 오류나 경고가 의심되는 경우 추적 로그를 검토할 수 있습니다. 이러한 파일은 일반적으로 Windows 운영 체제의 Program Files 디렉터리에 있는 MSSQL의 일반적인 LOG 폴더에 있습니다.

## TRC 파일 형식
TRC 파일 형식은 SQL Server Profiler에서 MS SQL 서버에서 최근에 실행한 명령문의 새 추적을 자동으로 생성하는 데 사용됩니다. SQL Server 프로파일러는 모든 새 추적에 대해 기본 템플릿을 사용합니다. 그러나 소프트웨어에는 특정 유형의 이벤트를 모니터링하기 위한 몇 가지 미리 정의된 템플릿이 포함되어 있습니다. 또한 SQL Server 프로파일러를 사용하여 추적에 포함할 이벤트 클래스 및 데이터 열을 정의하는 템플릿을 만들 수 있습니다.

### 사전 정의된 템플릿
다음은 SQL Server 프로파일러에 포함된 미리 정의된 템플릿 목록입니다.
- **SP_Counts**: 시간 경과에 따른 저장 프로시저 실행 동작을 캡처합니다.
- **표준**: 추적 생성을 위한 일반적인 시작점입니다.
- **TSQL**: 클라이언트가 SQL Server에 제출한 모든 Transact-SQL 문과 발급된 시간을 캡처합니다.
- **TSQL_Duration**: 클라이언트가 SQL Server에 제출한 모든 Transact-SQLTransact 문과 실행 시간을 캡처하고 기간별로 그룹화합니다.
- **TSQL_Grouped**: 특정 클라이언트 또는 사용자의 쿼리를 조사하는 데 사용합니다.
- **TSQL_Locks**: 교착 상태, 잠금 시간 초과 및 잠금 에스컬레이션 이벤트 문제를 해결하는 데 사용합니다.
- **TSQL_Replay**: 벤치마크 테스트 등의 반복적인 튜닝을 수행할 때 사용합니다.
- **TSQL_SPs**: 저장 프로시저의 구성 요소 단계를 분석하는 데 사용합니다.
- **튜닝**: 데이터베이스 엔진 튜닝 관리자가 데이터베이스를 튜닝하기 위한 작업으로 사용할 수 있는 추적 출력을 생성하는 데 사용합니다.
### 추적을 Windows 성능 로그 데이터와 연결
SQL Server 프로파일러를 사용하여 Microsoft Windows 성능 로그를 열고, 추적과 연관시킬 카운터를 선택하고, MS SQL Server 프로파일러 GUI에서 추적과 함께 선택한 성능 카운터를 표시할 수 있습니다. 선택한 추적 이벤트와 상관 관계가 있는 성능 로그 데이터를 나타내기 위해 SQL Server Profiler의 시스템 모니터 데이터 창 창에 빨간색 세로 막대가 표시됩니다.


## 참조 ##

* [SQL 서버 프로파일러](https://learn.microsoft.com/en-us/sql/tools/sql-server-profiler/sql-server-profiler?view=sql-server-ver15)

