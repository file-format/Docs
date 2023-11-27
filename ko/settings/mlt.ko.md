{
"날짜": "2023-10-04",
  "keywords": [
"mlt",
"mlt 파일",
"mlt 샷컷 프로젝트",
"mlt 파일이 무엇인가요?",
"mlt 파일을 여는 방법",
"파일",
"mlt 파일 확장자",
"확대"
],
  "author": {
"display_name": "샤킬 파이즈"
},
"draft": "false",
"toc": true,
"title": "MLT 파일 형식 - Shotcut 프로젝트",
  "description":"MLT 파일을 생성하고 열 수 있는 MLT Shotcut 프로젝트 형식과 API에 대해 알아보세요.",
"linktitle": "MLT",
  "menu": {
    "docs": {
      "identifier": "settings-mlt",
"parent" : "settings"
}
},
"lastmod": "2023-10-04"
}

## .MLT 파일이란?

MLT 파일은 기본적으로 오픈 소스 비디오 편집기인 **Meltytech Shotcut**에서 사용하는 프로젝트 파일입니다. 실제 비디오, 오디오 또는 이미지를 저장하는 대신 프로젝트 설정을 XML 형식으로 저장합니다. 이러한 설정에는 프로젝트로 가져온 미디어 파일에 대한 세부 정보, 타임라인에서 해당 파일이 정렬되는 방식, 해당 파일에 적용한 효과, 다양한 비디오 및 오디오 속성이 포함됩니다.

간단히 말해서 MLT 파일을 Shotcut에 비디오 프로젝트를 다시 만드는 방법을 알려주는 청사진이나 지도로 생각하십시오. Shotcut에서 MLT 파일을 열면 파일 내의 지침을 읽고 모든 미디어, 편집 및 효과를 포함하여 프로젝트를 재구성하므로 작업을 계속하거나 표준 형식의 최종 비디오로 내보낼 수 있습니다.

## 멜티텍 샷컷

간단히 "Shotcut"이라고도 불리는 Meltytech Shotcut은 무료 오픈 소스 비디오 편집 소프트웨어입니다. Windows, macOS, Linux를 포함한 다양한 운영 체제에서 비디오를 편집할 수 있는 다양하고 접근 가능한 플랫폼을 사용자에게 제공하도록 설계되었습니다.

Shotcut은 타임라인에서 비디오 및 오디오 클립을 가져오고 정렬하고, 전환 및 효과를 적용하고, 오디오 레벨을 조정하고, 최종 편집된 비디오를 다양한 형식과 해상도로 내보내는 기능을 포함하여 비디오 편집을 위한 다양한 기능을 제공합니다. 비선형 편집(NLE) 접근 방식을 사용하므로 사용자는 여러 트랙으로 작업하고 미디어 요소를 쉽게 조작하여 원하는 비디오 프로젝트를 만들 수 있습니다.

## Shotcut에서 사용되는 파일 형식

Shotcut에서 지원하는 몇 가지 일반적인 파일 형식 목록은 다음과 같습니다.

**가져온 미디어 형식(비디오, 오디오 및 이미지):**

1. **비디오 형식:**
    








- [MP4](/ko/비디오/mp4/)
- [MOV](/ko/video/mov/)
- [AVI](/ko/비디오/avi/)
- [MKV](/ko/video/mkv/)
- [WebM](/ko/video/webm/)
- [MPEG](/ko/비디오/mpeg/)
- [FLV](/ko/video/flv/)
- [WMV](/ko/video/wmv/)
- 그리고 더...
2. **오디오 형식:**
    








- [MP3](/ko/오디오/mp3/)
- [WAV](/ko/오디오/wav/)
- [AAC](/ko/오디오/aac/)
- [FLAC](/ko/오디오/flac/)
- [OGG](/ko/오디오/ogg/)
- [M4A](/ko/오디오/m4a/)
- 그리고 더...
3. **이미지 형식:**
    








- [JPEG(JPG)](/ko/image/jpeg/)
- [PNG](/ko/이미지/png/)
- [BMP](/ko/이미지/bmp/)
- [TIFF](/ko/이미지/tiff/)
- [GIF](/ko/이미지/gif/)
- 그리고 더...
4. **추가 형식:**
    








- Shotcut은 자막(SRT, ASS, SSA 등) 및 재생 목록(M3U, M3U8)에 대한 다양한 형식도 지원합니다.

**내보낸 프로젝트 및 출력 형식:**

1. **비디오 형식:**
    








- [MP4(H.264 코덱)](/ko/video/mp4/)
- [WebM(VP9 코덱)](/ko/video/webm/)
- [AVI](/ko/비디오/avi/)
- [MOV](/ko/video/mov/)
- [MKV](/ko/video/mkv/)
- 그리고 더...
2. **오디오 형식:**
    








- [MP3](/ko/오디오/mp3/)
- [WAV](/ko/오디오/wav/)
- [AAC](/ko/오디오/aac/)
- [FLAC](/ko/오디오/flac/)
- [OGG](/ko/오디오/ogg/)
- [M4A](/ko/오디오/m4a/)
- 그리고 더...
3. **이미지 형식:**
    








- [JPEG(JPG)](/ko/image/jpeg/)
- [PNG](/ko/이미지/png/)
- [BMP](/ko/이미지/bmp/)
- [TIFF](/ko/이미지/tiff/)
- [GIF](/ko/이미지/gif/)
- 그리고 더...
4. **사용자 정의 내보내기 설정:**
    








- Shotcut을 사용하면 코덱 옵션, 품질, 해상도 및 프레임 속도를 포함하여 비디오 및 오디오에 대한 내보내기 설정을 사용자 정의할 수 있습니다. 이러한 유연성을 통해 특정 요구 사항에 맞게 출력을 맞춤화할 수 있습니다.

## MLT 파일을 여는 방법?

MLT 파일을 여는 프로그램은 다음과 같습니다

- (Windows, MAC, Linux)용 **Meltytech Shotcut**(무료)

## 참고자료
* [Shotcut](https://en.wikipedia.org/wiki/Shotcut)
