{
"날짜":"2023-07-20",
   "keywords":[
"큰 상자",
"BIN 파일",
"파일",
"BIN 파일 확장자",
"확대",
"파일"
],
   "author":{
"display_name":"샤킬 파이즈"
},
"draft":"false",
"toc":true,
"title":"BIN 파일 형식 - MacBinary 인코딩 파일",
   "description":"BIN 파일을 생성하고 열 수 있는 BIN 형식과 API에 대해 알아보세요.",
"linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"compression-bin",
"parent":"압축"
}
},
"lastmod":"2023-07-20"
}

## .BIN 파일이란?

Macintosh 컴퓨터의 경우 BIN 파일은 MacBinary 형식으로 저장된 파일을 참조할 수 있습니다. MacBinary는 인터넷, 이메일, FTP 또는 휴대용 미디어를 통해 Macintosh 파일을 전송하기 위해 특별히 설계된 파일 형식입니다. MacBinary의 목적은 단일 파일 내에서 데이터 포크와 리소스 포크를 모두 포함하여 Macintosh 파일의 전체 파일 구조와 특성을 보존하는 것입니다.

MacBinary 형식은 Macintosh HFS(계층적 파일 시스템) 리소스 포크와 데이터 포크를 압축 파일로 캡슐화하여 이를 달성합니다. 또한 파일에 대한 중요한 메타데이터가 포함된 파인더 헤더도 포함되어 있습니다. 이러한 모든 구성 요소를 하나의 파일로 결합함으로써 MacBinary는 파일의 무결성을 유지하고 다른 플랫폼 간에 쉽게 전송 및 공유할 수 있도록 보장합니다.

Apple의 파일 시스템 및 파일 전송 프로토콜이 발전함에 따라 BIN 파일 및 MacBinary 형식의 사용이 덜 일반적이 되었습니다. ZIP과 같은 파일 형식의 도입과 HFS+ 및 APFS와 같은 최신 파일 시스템으로의 전환으로 인해 MacBinary로 인코딩된 파일의 필요성이 감소했습니다. 이러한 최신 파일 시스템은 파일 속성, 리소스 포크 및 데이터 포크를 보다 효율적으로 처리하는 방법을 제공하므로 오늘날의 컴퓨팅 환경에서 MacBinary 형식의 필요성이 줄어듭니다.

## BIN 파일 형식 - 추가 정보

Macintosh 컴퓨터 초기에는 데이터 제한으로 인해 파일이 두 개의 별도 "포크"에 저장되었습니다. "리소스 포크"에는 구조화된 데이터가 포함된 반면 "데이터 포크"에는 구조화되지 않은 데이터가 포함되었습니다. Classic Mac OS는 이러한 포크를 단일 파일로 처리했지만 Mac이 아닌 시스템으로 파일을 전송하면 포크를 단일 개체로 인식하지 못하기 때문에 데이터가 손실되었습니다. 이 문제를 해결하기 위해 Dennis Brothers, Harry Chesley 및 Yves Lempereur와 같은 개인이 MacBinary 형식을 만들었습니다. MacBinary는 Mac이 아닌 시스템으로 전송하기 위해 포크를 BIN 파일이라고 하는 단일 파일로 압축하고 결합했습니다. Mac OS로 돌아가면 포크가 다시 분리됩니다. 2000년대에 포크 기반 HFS에서 벗어나면서 MacBinary 형식의 사용이 크게 감소했습니다. 오늘날 MacBinary로 인코딩된 BIN 파일을 발견하는 일은 Mac이 아닌 시스템에서 오래된 파일을 발견하거나 인터넷에서 다운로드하지 않는 한 거의 발생하지 않습니다.

MacBinary 형식은 Macintosh 시스템 및 파일 처리의 변경 사항을 수용하기 위해 시간이 지남에 따라 여러 버전을 거쳤습니다. MacBinary 형식의 다양한 버전은 다음과 같습니다.

- **MacBinary I:** 1980년대 후반에 소개된 MacBinary의 초기 버전입니다. 리소스 포크와 데이터 포크를 단일 바이너리 파일로 결합하여 Macintosh 파일의 플랫폼 간 전송을 허용합니다.

- **MacBinary II:** 1990년대 초반에 출시된 이 버전은 바이너리 파일의 헤더에 파일 유형 및 작성자 코드와 같은 추가 정보를 추가하여 원래 MacBinary 형식을 개선했습니다. 이러한 코드는 전송 중에 Macintosh 파일의 무결성과 식별을 유지하는 데 도움이 되었습니다.

- **MacBinary III:** 1990년대 중반에 도입된 MacBinary III 형식은 파일 이름, 파일 생성 및 수정 날짜와 같은 추가 메타데이터를 바이너리 파일 헤더에 포함하여 이전 버전을 더욱 향상시켰습니다. 이를 통해 전송 중에 Macintosh 파일 속성을 보다 포괄적으로 보존할 수 있었습니다.

- **MacBinary IV:** MacBinary IV는 2000년대 초반에 새롭게 등장한 Mac OS X 운영 체제와의 호환성 문제를 해결하기 위해 개발되었습니다. Mac OS X에 도입된 새로운 파일 시스템 구조와 속성에 적응하기 위한 변경 사항이 통합되었습니다.

## BIN 파일 여는 방법? .

MacBinary로 인코딩된 BIN 파일은 다양한 압축 유틸리티를 사용하여 열 수 있습니다. macOS 사용자의 경우 **Apple Archive Utility**가 적합한 옵션입니다. Windows 사용자는 **Smith Micro StuffIt Deluxe**와 같은 소프트웨어를 활용하여 MacBinary로 인코딩된 BIN 파일의 내용을 추출할 수 있습니다. macOS 사용자를 위한 또 다른 옵션은 MacBinary를 포함한 여러 파일 형식을 처리할 수 있는 다용도 도구인 **The Unarchiver**입니다.

.bin 파일 확장자는 MacBinary뿐만 아니라 다양한 파일 형식에서 사용된다는 점에 유의하는 것이 중요합니다. 따라서 앞서 언급한 유틸리티로 열 수 없는 BIN 파일이 발견되면 다른 형식으로 저장될 수 있습니다. 이러한 경우 특정 파일 형식을 식별하고 해당 형식에 맞게 설계된 적절한 소프트웨어나 유틸리티를 사용하여 파일 콘텐츠에 액세스해야 할 수도 있습니다.

## 기타 BIN 파일

**.bin** 파일 확장자를 사용하는 다른 파일 형식은 다음과 같습니다.

- [BIN - 바이너리 디스크 이미지 파일](/ko/disc-and-media/bin/)
- [BIN - Unix 실행 파일](/ko/executable/bin/)
- [BIN - BlackBerry IT 정책 파일](/ko/settings/bin/)
- [BIN - Sega Genesis 게임 ROM](/ko/game/bin/)
- [BIN - PSX PlayStation BIOS 이미지](/ko/game/bin-pcsx/)

## 참고자료

* [맥바이너리](https://en.wikipedia.org/wiki/MacBinary)

