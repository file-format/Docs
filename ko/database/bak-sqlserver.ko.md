{
"날짜": "2023-06-12",
  "keywords": [
"박",
"박 파일",
"Microsoft SQL Server 데이터베이스 백업",
"bak 파일이 무엇인가요?",
"박 파일을 여는 방법",
"파일",
"박 파일 확장자",
"확대"
],
  "author": {
"display_name": "샤킬 파이즈"
},
"draft": "false",
"toc": true,
"title": "BAK 파일 형식 - Microsoft SQL Server 데이터베이스 백업",
  "description":"BAK SQL Server 백업 형식과 BAK 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
"linktitle": "BAK SQL Server",
  "menu": {
    "docs": {
      "identifier": "database-bak-sqlserver",
"parent" : "database"
}
},
"lastmod": "2023-06-12"
}

## .BAK 파일이란?

Microsoft SQL Server와 관련하여 ".bak" 파일은 SQL Server 데이터베이스의 복사본을 저장하는 데 사용되는 백업 파일 형식입니다. 이러한 파일에는 스키마, 데이터 및 기타 관련 정보를 포함하여 특정 시점의 데이터베이스 스냅샷이 포함되어 있습니다. 이는 SQL Server에 내장된 백업 및 복원 기능을 사용하여 생성되며 다음과 같은 몇 가지 중요한 목적으로 사용됩니다.

1. **데이터 복구:** .bak 파일은 데이터 손실, 손상 또는 기타 문제가 발생한 경우 데이터베이스를 복구하는 수단을 제공합니다. .bak 파일에서 데이터베이스를 복원하면 데이터베이스를 이전 상태로 되돌려 가동 중지 시간과 데이터 손실을 최소화할 수 있습니다.

2. **마이그레이션 및 복제:** 백업 파일은 서버 간에 데이터베이스를 마이그레이션하거나 테스트, 개발 또는 보고 목적으로 데이터베이스 복사본을 만드는 데 자주 사용됩니다. 이는 환경 간에 데이터베이스를 이동하는 일관되고 효율적인 방법을 제공합니다.

3. **특정 시점 복구:** SQL Server에서는 .bak 파일을 사용하여 특정 시점 복구를 수행할 수 있습니다. 즉, 데이터베이스를 특정 시점으로 복원할 수 있으며 이는 규정 준수 또는 데이터 감사에 매우 중요할 수 있습니다.

4. **재해 복구:** .bak 파일은 재해 복구 계획의 중요한 부분입니다. 하드웨어 오류, 자연 재해 또는 기타 재난이 발생한 경우 데이터가 안전하고 신속하게 복원될 수 있도록 보장합니다.

## SQL Server에서 .BAK 파일 만들기

SQL Server에서 .bak 파일을 만들려면 일반적으로 BACKUP DATABASE 또는 BACKUP LOG와 같은 SSMS(SQL Server Management Studio) 또는 T-SQL(Transact-SQL) 명령을 사용합니다. 다음은 T-SQL을 사용하여 데이터베이스 백업을 만드는 방법에 대한 간단한 예입니다.

```
BACKUP DATABASE YourDatabaseName
TO DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## SQL Server에서 .BAK 파일 복원

.bak 파일에서 데이터베이스를 복원하려면 RESTORE DATABASE 명령을 사용할 수 있습니다.

```
RESTORE DATABASE YourRestoredDatabaseName
FROM DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## SQL Server에서 BAK 파일을 여는 방법은 무엇입니까?

".bak" 파일에 저장된 데이터를 열고 액세스하려면 일반적으로 해당 데이터를 Microsoft SQL Server 인스턴스로 복원해야 합니다. SSMS(SQL Server Management Studio)를 사용하여 ".bak" 파일을 여는 일반적인 단계는 다음과 같습니다.

1. **SQL Server Management Studio 실행**: 컴퓨터에서 SSMS를 엽니다. 일반적으로 시작 메뉴에서 찾거나 "SQL Server Management Studio"를 검색하여 찾을 수 있습니다.

2. **SQL Server 인스턴스에 연결**: SSMS에서 데이터베이스를 복원하려는 SQL Server 인스턴스에 연결합니다. 이 작업을 수행하려면 필요한 권한이 필요합니다.

3. **데이터베이스 복원**:

ㅏ. 왼쪽 개체 탐색기 창에서 SQL Server 인스턴스를 확장합니다.

비. "데이터베이스" 노드를 확장합니다.

씨. "데이터베이스"를 마우스 오른쪽 버튼으로 클릭하고 "데이터베이스 복원"을 선택합니다.

4. **소스 및 대상 지정**:

ㅏ. "데이터베이스 복원" 대화 상자의 "일반" 페이지에서 "데이터베이스로" 필드에 새 데이터베이스의 이름을 입력합니다. 이는 복원된 데이터베이스의 이름이 됩니다.

비. "소스" 섹션에서 백업 미디어 유형으로 "장치"를 선택합니다.

씨. "장치" 필드 옆에 있는 "..." 버튼을 클릭하여 복원하려는 ".bak" 파일을 찾습니다.

디. 열고 싶은 ".bak" 파일을 선택하고 "확인"을 클릭하세요.

5. **복원 옵션**: 필요에 따라 복원 옵션을 검토하고 구성합니다. 기존 데이터베이스 덮어쓰기 여부, 복구 옵션 설정 등을 지정할 수 있습니다. 요구 사항에 따라 이러한 옵션을 설정하십시오.

6. **복원 시작**: 복원 옵션을 구성한 후 "데이터베이스 복원" 대화 상자에서 "확인" 버튼을 클릭합니다. SQL Server가 복원 프로세스를 시작합니다.

7. **복원된 데이터베이스 액세스**: 성공적인 복원 후에는 다른 데이터베이스와 마찬가지로 SQL Server Management Studio에서 복원된 데이터베이스에 액세스할 수 있습니다. 쿼리를 실행하고, 테이블을 보고, 데이터베이스 내의 데이터로 작업할 수 있습니다.

## 기타 BAK 파일

**.bak** 파일 확장자를 사용하는 다른 파일 형식은 다음과 같습니다.

**데이터 베이스**
- [BAK - 데이터베이스 백업 파일](/ko/database/bak/)
- [BAK - Swiftpage Act! 데이터베이스 백업](/ko/database/bak-act/)

**게임**
- [BAK - Terraria 월드 또는 플레이어 백업](/ko/game/bak-terraria/)

**기타**
- [BAK - 백업 파일](/ko/misc/bak-backup/)
- [BAK - Chromium 북마크 백업](/ko/misc/bak-chromium/)
- [BAK - Finale 2012 점수 백업](/ko/misc/bak-finale/)
- [BAK - MobileTrans 백업](/ko/misc/bak-mobiletrans/)
- [BAK - VEGAS 비디오 프로젝트 백업](/ko/misc/bak-vegas/)

**설정**
- [BAK - 홀로 런처 백업](/ko/settings/bak-holo/)

## 참고자료
* [Backup and restore a SQL Server database with SSMS](https://learn.microsoft.com/en-us/sql/relational-databases/backup-restore/quickstart-backup-restore-database?view=sql-server-ver16&tabs=ssms)
