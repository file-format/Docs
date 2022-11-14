{
  "date" : "2019-10-11",
  "keywords": [ "pdb file", "pdb", "extension", "format", "What is a pdb file", "pdb file format", "PDB metadata" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PDB 파일 형식 - 프로그램 데이터베이스 파일",
  "description":"PDB 파일을 생성하고 열 수 있는 PDB 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "PDB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## .PDB 파일이란?

확장자가 .pdb인 파일은 컴파일된 실행 파일(EXE/DLL)에 대한 디버깅 정보가 포함된 프로그램 데이터베이스 파일입니다. PDB 파일은 응용 프로그램이 디버그 모드에서 컴파일될 때 Microsoft 컴파일러에 의해 생성됩니다. PDB 파일이 있으면 모듈의 모든 기호에 대한 중요한 정보가 포함되어 있으므로 실행 파일을 리버스 엔지니어링하는 데 도움이 될 수 있습니다. 이러한 이유로 이러한 파일은 최종 실행 파일과 별도로 보관됩니다. Microsoft의 [DgbHelp API](https://docs.microsoft.com/en-us/windows/win32/debug/dbghelp-functions)는 PDB 파일을 열어 공개 및 내보내기, 전역 기호, 로컬 기호, 유형 데이터, 소스 파일 및 행 번호.

## PDB 파일 형식

PDB는 Microsoft의 독점 파일 형식이며 아직 공식적으로 문서화되지 않았습니다. 그러나 시작 문서는 [여기](https://github.com/Microsoft/microsoft-pdb)에서 사용할 수 있으며 참조할 수 있습니다.

### PDB 스트림

PDB 파일은 각 스트림이 가상 개별 파일 역할을 하고 정보를 포함하는 여러 스트림으로 구성됩니다. PDB 파일 작성자는 이러한 파일에 쓸 수 있으며 명시적 커밋이 실행된 후에만 파일이 완료됩니다. 컴파일러는 PDB 파일에 계속 쓸 수 있지만 모든 사용자 코드가 성공적으로 컴파일되는 경우에만 커밋합니다. PDB 파일은 다음 스트림으로 구성됩니다.

|스트림 번호 |내용 |간단한 설명|
---|---|---|
|1| Pdb(헤더) |버전 정보 및 이 PDB를 EXE에 연결하기 위한 정보|
|2| Tpi(유형 관리자) |실행 파일에 사용된 모든 유형입니다.|
|3| Dbi(디버그 정보) |섹션 기고 및 'Mods' 목록 보유|
|4| 네임맵| 해시된 문자열 테이블 보유|
|4-(n+4)| n Mod's(모듈 정보)| 각 Mod 스트림은 하나의 compiland|에 대한 기호와 줄 번호를 보유합니다.
|n+4| 글로벌 심볼 해시| 이름으로 전역 기호를 검색할 수 있는 색인|
|n+5| 공개 기호 해시| 주소로 공용 기호를 검색할 수 있는 색인|
|n+6| 기호 레코드| 글로벌 및 공용 심볼의 실제 심볼 기록|
|n+7| 유형 해시| TPI 스트림에서 사용하는 해시입니다.|

PDB 파일의 각 스트림은 반드시 연속적으로 번호가 매겨지지 않는 여러 페이지로 구성됩니다.

### PDB 헤더

특정 형식을 식별하고 검증하기 위한 서명으로 구성된 헤더가 있는 PDB 파일입니다. 서명의 길이는 PDB 형식에 따라 다릅니다. 헤더는 단일 페이지보다 길 수 있습니다.

### PDB 메타데이터
PDB 메타데이터는 모든 구성 요소 스트림을 인식하여 각 스트림에 대한 페이지의 길이와 순서를 제공합니다. 순서는 연속적으로 스트림에 제공됩니다. 0부터 시작합니다. 일부 메타데이터를 포함하는 정렬되지 않은 루트 스트림도 있습니다.

## 참고문헌
* [PDB - 위키백과](https://en.wikipedia.org/wiki/Program_database)
* [마이크로소프트 PDB](https://github.com/Microsoft/microsoft-pdb)

