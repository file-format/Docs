{
"날짜": "2023-08-03",
  "keywords": [
"usr",
"usr 파일",
"usr 파일이 무엇인가요?",
"usr 파일을 여는 방법",
"파일",
"usr 파일 확장자",
"확대"
],
  "author": {
"display_name": "샤킬 파이즈"
},
"draft": "false",
"toc": true,
"title": "USR 파일 형식 - Lowrance GPS 데이터 파일",
  "description":"USR 파일을 만들고 열 수 있는 USR 형식과 API에 대해 알아보세요.",
"linktitle": "USR",
  "menu": {
    "docs": {
      "identifier": "gis-usr",
"parent": "기스"
}
},
"lastmod": "2023-08-03"
}

## .USR 파일이란?

".usr" 파일 확장자는 Lowrance GPS 장치와도 관련이 있습니다. 특히, Lowrance GPS 장치에서 사용되는 "사용자 데이터 형식"(USR 형식)으로 알려진 형식으로 GPS 데이터를 저장하는 데 사용됩니다.

Lowrance GPS 장치를 사용할 때 웨이포인트, 트랙 및 경로를 ".usr" 파일로 저장할 수 있습니다. 이러한 파일에는 일반적으로 위도, 경도, 고도, 타임스탬프 및 GPS 활동과 관련된 기타 데이터와 같은 정보가 포함되어 있습니다.

Lowrance GPS 장치에서 .usr 파일을 사용하는 일반적인 용도는 다음과 같습니다.

- **웨이포인트:** 웨이포인트는 명소, 즐겨 찾는 낚시 장소, 관심 지점 등 GPS에 표시된 특정 위치입니다. 이러한 위치를 .usr 파일로 저장할 수 있으며 가져오거나 내보내거나 다른 Lowrance GPS 사용자와 공유할 수 있습니다.

- **트랙:** 트랙은 GPS 이동의 기록된 경로를 나타냅니다. 트랙 로그를 .usr 파일로 저장할 수 있으므로 나중에 경로를 검토 및 분석하거나 다른 사람과 공유할 수 있습니다.

- **경로:** 경로는 GPS 장치에 만들고 저장할 수 있는 사전 정의된 경로입니다. 이러한 경로는 나중에 사용하거나 공유하기 위해 .usr 파일로 저장할 수도 있습니다.

Lowrance GPS 장치에서 .usr 파일을 관리하려면 일반적으로 Lowrance의 "Insight Planner" 또는 "Lowrance GPS Utility"와 같은 소프트웨어를 사용하여 GPS 데이터를 가져오고 내보내고 조작합니다.

## USR 파일 형식 - 추가 정보

Lowrance iFinder GPS 장치에서는 .usr 파일이 생성되어 장치에 삽입된 MMC(MultiMediaCard) 메모리 카드에 저장됩니다. 이러한 파일에는 웨이포인트, 트랙 및 경로와 같은 사용자 데이터가 포함되어 있습니다.

.usr 파일을 MMC에서 컴퓨터로 전송하려면 다음 단계를 따르세요.

- **MMC 제거:** Lowrance iFinder GPS 장치에서 MultiMediaCard(MMC)를 조심스럽게 제거합니다.

- **컴퓨터에 MMC 삽입:** 적절한 MMC 카드 리더기를 사용하여 메모리 카드를 컴퓨터의 카드 리더 슬롯에 삽입합니다.

- **.usr 파일 찾기:** 컴퓨터에서 MMC를 인식하면 MMC에 저장된 파일에 액세스할 수 있습니다. GPS 데이터가 포함된 .usr 파일을 찾으세요.

- **GPSBabel을 사용한 변환:** .usr 파일을 다른 GPS 형식으로 변환하려면 다양한 GPS 파일 형식 작업을 위한 무료 오픈 소스 도구인 GPSBabel을 사용할 수 있습니다. GPSBabel은 다양한 입력 및 출력 형식을 지원하므로 .usr 파일을 다른 GPS 소프트웨어 또는 장치와 호환되는 형식으로 변환할 수 있습니다.

GPSBabel은 공식 홈페이지(http://www.gpsbabel.org/)에서 다운로드하여 컴퓨터에 설치하시면 됩니다. 설치한 후에는 소프트웨어의 명령줄 인터페이스나 그래픽 사용자 인터페이스(사용 가능한 경우)를 사용하여 변환을 수행할 수 있습니다.

예를 들어, .usr 파일을 GPX 형식으로 변환하려면 다음과 같은 명령을 사용할 수 있습니다.

```
gpsbabel -i lowranceusr -f input.usr -o gpx -F output.gpx
```

위 명령은 GPSBabel에 Lowrance USR 형식의 입력 파일 "input.usr"을 읽고 GPX 형식의 출력 파일 "output.gpx"를 쓰도록 지시합니다.

- **변환된 파일 가져오기/사용:** 변환 후에는 GPS 데이터가 새로운 형식(예: GPX)으로 생성되며, 해당 형식을 지원하는 다른 GPS 소프트웨어나 장치에서 사용할 수 있습니다.

## USR 파일 여는 방법?

USR 파일을 열거나 참조하는 프로그램은 다음과 같습니다.

- GPS바벨(윈도우)
- GPS바벨(맥)
- GPS바벨(리눅스)

## 참고자료
* [로랜스 일렉트로닉스](https://en.wikipedia.org/wiki/Lowrance_Electronics)

