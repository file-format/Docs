{
  "date" : "2021-02-20",
  "keywords" :[ "WMA", "파일", "확장자", "형식", "오디오 교환 파일 형식", "음악"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"WMA 파일 형식과 WMA 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"WMA - Windows Media 오디오 파일",
  "linktitle" : "WMA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-02-20"
}

## .WMA 파일이란?

확장자가 .wma인 파일은 ASF(Advanced Systems Format) 형식으로 저장된 오디오 파일을 나타냅니다. ASF는 Windows Media Audio 9로 인코딩된 비트스트림을 포함하는 Microsoft의 독점 형식입니다. 오디오 콘텐츠 외에도 WMA 파일에는 트랙의 제목, 앨범, 아티스트 및 장르와 같은 메타데이터 개체도 포함됩니다. WMA 파일은 주로 [.mp3](/ko/audio/mp3/) 파일과 유사한 웹을 통한 스트리밍에 사용됩니다.

## WMA 파일 형식

WMA 파일은 이진 파일 형식이며 ASF 파일 형식에 포함됩니다. MP3 파일에서 사용하는 ID3 태그와 유사한 파일에 대한 메타데이터 인코딩을 지정합니다. WMA 코덱은 2008년부터 Microsoft에서 PIFF(Protected Interoperable File Format)로 사용하고 있습니다. 그러나 DECE UltraViolet 및 MPEG-DASH와 같은 관련 산업 표준에서 표준화된 오디오 코덱으로 선언되지 않았습니다.

### WMA 유형별 데이터

Windows Media 오디오 코덱에 대한 유형별 정보는 스트림 속성 개체의 유형별 데이터의 일부로 다음 형식으로 저장됩니다.

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## 참고문헌

* [ASF 개요 - Microsoft](https://docs.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format?redirectedfrom=MSDN)

