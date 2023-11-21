{
"날짜": "2023-06-12",
  "keywords": [
"박",
"박 파일",
"BAK 크롬 북마크",
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
"title": "BAK 파일 형식 - Chromium 북마크 백업",
  "description":"BAK 파일을 만들고 열 수 있는 BAK Chromium 북마크 형식과 API에 대해 알아보세요.",
"linktitle": "BAK 크롬 북마크",
  "menu": {
    "docs": {
      "identifier": "misc-bak-chromium",
"parent": "기타"
}
},
"lastmod": "2023-06-12"
}

## .BAK 파일이란?

Google Chrome 및 Microsoft Edge와 같은 Chromium 기반 웹 브라우저의 컨텍스트에서 .bak 파일은 기본적으로 북마크의 백업 파일입니다. 이러한 북마크는 일반 텍스트 목록으로 저장되며 사용되는 파일 형식은 JSON입니다. 이러한 .bak 파일의 목적은 실수로 삭제하거나 손실한 경우 복원할 수 있는 백업을 제공하여 북마크를 보호하는 것입니다.

Google Chrome을 포함한 Chromium 기반 브라우저는 정기적으로 이러한 백업 파일을 생성하고 일반적으로 "Bookmarks.bak"라는 이름을 지정합니다. 이는 기본적으로 특정 시점의 북마크 스냅샷입니다.

## .bak 파일을 사용하여 북마크를 복원하는 방법

1. **백업 파일 찾기:** 일반적으로 Chromium 프로필과 연결된 특정 폴더에 있습니다. 정확한 위치는 운영 체제에 따라 다를 수 있습니다.

Windows의 경우: `C:\Users\를 확인하세요.<YourUsername> \AppData\Local\Chromium\User Data\Default\Bookmarks.bak`.

macOS: `~/Library/Application Support/Chromium/Default/Bookmarks.bak`에서 검색하세요.

Linux: `~/.config/chromium/Default/Bookmarks.bak`를 확인하세요.

3. Chromium 브라우저가 닫혀 있는지 확인하세요.
4. ".bak" 확장자를 제거하여 "Bookmarks.bak" 파일의 이름을 바꾸십시오. 그러면 간단히 "Bookmarks"라고 됩니다.
5. 크롬을 시작합니다.

.bak 파일 이름을 '북마크'로 바꾸면 Chromium은 이를 현재 북마크 파일로 사용하며 이전 북마크를 복원해야 합니다.

## Chromium 북마크 백업

Chromium 북마크를 백업하는 것은 저장된 중요한 웹 페이지와 URL을 잃지 않도록 하는 현명한 예방 조치입니다. Chromium은 Google Chrome 및 Microsoft Edge와 같은 다른 브라우저의 기반 역할을 하는 오픈 소스 브라우저입니다. Chromium 북마크를 백업하려면 다음 단계를 따르세요.

## 방법 1: 수동 백업

1. **Chromium 열기**: 컴퓨터에서 Chromium 브라우저를 실행합니다.

2. **북마크 액세스**: 브라우저 창 오른쪽 상단에 있는 세 개의 수직 점(메뉴 아이콘)을 클릭합니다. 드롭다운 메뉴에서 '북마크' 위로 마우스를 가져가면 북마크 하위 메뉴가 표시됩니다.

3. **북마크 내보내기**: 북마크 하위 메뉴에서 '북마크 관리자'를 클릭하세요. 북마크를 표시하는 새 탭이 열립니다.

4. **북마크 내보내기**: 북마크 관리자 탭에서 세 개의 수직 점(보통 오른쪽 상단에 있음)을 다시 클릭하여 북마크 관리자 메뉴를 엽니다. 이 메뉴에서 '북마크 내보내기'를 선택하세요.

5. **위치 선택**: 컴퓨터에서 내보낸 북마크 파일을 저장할 위치를 선택합니다. 기본 파일 이름은 "bookmarks.html"이지만 원하는 경우 변경할 수 있습니다. 기억할 수 있는 위치에 저장하세요.

6. **저장**: 북마크를 HTML 파일로 저장하려면 "저장" 또는 "내보내기" 버튼을 클릭하세요.

이제 북마크가 HTML 파일로 백업되었습니다. 안전하게 보관하기 위해 이 파일을 외부 드라이브나 클라우드 저장소에 복사할 수 있습니다.

## 방법 2: Google 계정과 동기화(해당하는 경우)

Chromium에서 Google 계정에 로그인한 경우 내장된 동기화 기능을 사용하여 북마크를 안전하게 유지하고 여러 기기에서 동기화할 수도 있습니다. 이렇게 하면 북마크가 Google 계정에 자동으로 백업됩니다.

1. **Chromium 열기**: Chromium 브라우저를 실행하고 Google 계정에 로그인했는지 확인하세요.

2. **동기화 활성화**: 브라우저 창 오른쪽 상단에 있는 세 개의 수직 점(메뉴 아이콘)을 클릭하고 '설정'으로 이동합니다.

3. **동기화 및 Google 서비스**: 설정 탭의 왼쪽 사이드바에서 '동기화 및 Google 서비스'를 클릭합니다.

4. **데이터 동기화**: '동기화'에서 '북마크'가 켜져 있는지 확인하세요. 그러면 북마크가 Google 계정과 동기화됩니다.

이제 북마크가 자동으로 백업되고 Google 계정과 동기화됩니다. Chromium이나 Google 동기화를 지원하는 다른 브라우저를 사용하는 모든 기기에서 Google 계정에 로그인하여 액세스할 수 있습니다.

특히 Google 계정 동기화에만 의존하지 않는 로컬 복사본을 원하는 경우 정기적으로 북마크를 수동으로 백업하는 것을 잊지 마세요.

## BAK 파일을 여는 방법

북마크 백업의 원시 데이터를 탐색하려면 Microsoft Visual Studio Code(여러 플랫폼에서 사용 가능), Microsoft 메모장(Windows 사용자용), Apple TextEdit과 같은 다양한 텍스트 편집기를 사용하여 "Bookmarks.bak" 파일을 열 수 있습니다. (Mac 사용자의 경우) 또는 원하는 다른 텍스트 편집기. 그렇게 하면 파일에 포함된 북마크와 메타데이터를 볼 수 있습니다.

다양한 텍스트 편집 소프트웨어와 코드 편집기를 사용하여 "Bookmarks.bak" 파일을 열고 해당 내용을 볼 수 있습니다. 다음은 일반적으로 사용되는 몇 가지 옵션입니다.

1. 비주얼 스튜디오 코드(VS Code)
2. 메모장(윈도우)
3. 텍스트편집(맥)
4. 숭고한 텍스트
5. 메모장++
6. 아톰
7. nano와 Vim(리눅스)
8. 워드패드(윈도우)

## 기타 BAK 파일

**.bak** 파일 확장자를 사용하는 다른 파일 형식은 다음과 같습니다.

**데이터 베이스**
- [BAK - 데이터베이스 백업 파일](/ko/database/bak/)
- [BAK - Swiftpage Act! 데이터베이스 백업](/ko/database/bak-act/)
- [BAK - Microsoft SQL Server 데이터베이스 백업](/ko/database/bak-sqlserver/)

**게임**
- [BAK - Terraria 월드 또는 플레이어 백업](/ko/game/bak-terraria/)

**기타**
- [BAK - 백업 파일](/ko/misc/bak-backup/)
- [BAK - Finale 2012 점수 백업](/ko/misc/bak-finale/)
- [BAK - MobileTrans 백업](/ko/misc/bak-mobiletrans/)
- [BAK - VEGAS 비디오 프로젝트 백업](/ko/misc/bak-vegas/)

**설정**
- [BAK - 홀로 런처 백업](/ko/settings/bak-holo/)

## 참고자료
* [Chromium Bookmarks](https://www.chromium.org/user-experience/bookmarks/)
