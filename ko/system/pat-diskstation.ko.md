{
"날짜":"2023-11-01",
   "keywords":[
"가볍게 두드리기",
"pat 파일",
"pat diskstation 관리자 설치 파일",
"pat 파일을 여는 방법",
"파일",
"pat 파일 확장자",
"확대",
"파일"
],
   "author":{
"display_name":"샤킬 파이즈"
},
"draft":"false",
"toc":true,
"title": "PAT 파일 형식 - DiskStation Manager 설치 파일",
   "description":"PAT DiskStation Manager 설치 파일 형식과 PAT 파일을 생성하고 열 수 있는 API에 대해 알아보세요.",
"linktitle":"PAT",
   "menu":{
      "docs":{
         "identifier":"system-pat-diskstation",
"parent":"시스템"
}
},
"lastmod":"2023-11-01"
}

## .PAT 파일이란?

PAT 파일은 일반적으로 Synology NAS(Network-Attached Storage) 장치에서 사용되는 운영 체제인 **DiskStation Manager(DSM)**와 연결됩니다. PAT 파일은 Synology NAS에서 DSM을 업데이트하거나 설치하는 데 사용되는 설치 파일입니다.

## PAT 파일의 활용

일반적으로 PAT 파일을 사용하여 Synology NAS에 DSM을 설치하거나 업데이트하는 방법은 다음과 같습니다.

1. PAT 파일 다운로드: 공식 Synology 웹사이트나 기타 신뢰할 수 있는 소스에서 PAT 파일을 얻을 수 있습니다.
    







2. NAS에 로그인: 웹 브라우저에 IP 주소를 입력하여 Synology NAS의 웹 기반 사용자 인터페이스에 액세스합니다. 이 작업을 수행하려면 관리자 권한이 필요합니다.
    







3. 패키지 센터로 이동: 웹 인터페이스에서 "패키지 센터"로 이동합니다. 이곳은 NAS의 애플리케이션을 관리하고 설치하는 곳입니다.
    







4. 수동 설치: 패키지 센터에는 사용 중인 DSM 버전에 따라 "수동 설치" 또는 "설치/업데이트" 옵션이 있어야 합니다. 이 옵션을 선택하세요.
    







5. PAT 파일 찾아보기: 로컬 파일을 찾아보고 다운로드한 PAT 파일을 선택하라는 메시지가 표시됩니다.
    







6. 설치 또는 업데이트: PAT 파일을 선택한 후 화면의 지시에 따라 DSM을 설치하거나(새로 설치하는 경우) DSM을 업데이트합니다(최신 버전으로 업그레이드하는 경우).
    







7. 완료될 때까지 기다립니다. 설치 또는 업데이트 프로세스는 다소 시간이 걸릴 수 있으며 프로세스의 일부로 NAS가 재부팅될 수 있습니다. 인내심을 갖고 완료될 때까지 기다리십시오.
    







8. 설치 후 구성: 설치 또는 업데이트 후에는 원하는 대로 NAS 설정을 구성해야 할 수도 있습니다.

## DiskStation 관리자

흔히 DSM으로 축약되는 DiskStation Manager는 Synology가 NAS(Network-Attached Storage) 장치용으로 개발한 운영 체제입니다. Synology NAS 서버의 관리 및 제어 인터페이스 역할을 합니다. DiskStation Manager는 사용자가 데이터 저장소, 파일 공유, 백업 솔루션, 멀티미디어 서비스 등과 같은 NAS의 다양한 측면을 구성하고 관리할 수 있는 사용자 친화적인 웹 기반 인터페이스를 제공합니다.

DSM은 사용자가 Synology NAS에 다양한 응용 프로그램과 서비스를 설치하고 실행하여 가정 및 기업용 다목적 서버로 전환할 수 있는 다용성과 광범위한 패키지 에코시스템으로 잘 알려져 있습니다. DiskStation Manager의 일반적인 기능에는 파일 공유, 데이터 백업 및 동기화, 미디어 스트리밍, 보안 기능 및 가상화 지원이 포함됩니다.

Synology는 보안, 성능 및 기능을 강화하기 위해 DSM의 업데이트와 새 버전을 정기적으로 출시합니다. 사용자는 PAT 파일을 사용하여 DSM을 수동으로 업데이트하거나 자동 업데이트를 구성하여 NAS가 가장 안전한 최신 버전의 DiskStation Manager를 실행하도록 할 수 있습니다.

## PAT 파일을 여는 방법

DiskStation Manager를 수동으로 업데이트하려면 다음 단계에 따라 Synology 다운로드 센터에서 다운로드한 PAT 파일을 사용할 수 있습니다.

1. DiskStation Manager 제어판에 액세스합니다.
2. "업데이트 및 복원" 섹션으로 이동하여 "DSM 업데이트"를 선택합니다.
3. 여기에서 "수동 DSM 업데이트"를 선택합니다.
4. "찾아보기" 버튼을 클릭한 다음 다운로드한 PAT 파일을 찾아서 선택합니다.
5. DiskStation Manager 업데이트를 시작하려면 "적용" 버튼을 클릭합니다.

## 참고자료
* [Synology](https://en.wikipedia.org/wiki/Synology)
