{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LRC 파일 형식 - LRC 파일이란?",
  "description":"LRC 파일을 만들고 열 수 있는 LRC Lyric 파일과 API에 대해 알아보세요.",
  "linktitle" : "LRC",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## .LRC 파일이란?

LRC 파일은 오디오 노래의 가사가 포함된 텍스트 기반 가사 파일입니다. 오디오 노래가 컴퓨터의 음악 플레이어 또는 오디오 플레이어 소프트웨어로 재생되면 LRC 파일을 병렬로 읽고 시간과 함께 표시합니다. LRC 파일에는 노래가 재생될 때 가사를 표시하기 위한 큐 포인트가 포함되어 있습니다. 일반적으로 LRC 파일은 audio.mp3, audio.lrc 등 해당 오디오 파일과 이름이 같습니다. LRC 파일은 [SRT](/ko/video/srt/)와 같은 자막 파일과 유사합니다.

## LRC 파일 형식 - 추가 정보

LRC 가사 형식 파일은 일반 텍스트 파일로 저장되며 텍스트 파일에서 열고 편집할 수 있습니다. LRC 파일의 내용에는 가사 텍스트 표시를 위한 색상 정보가 포함되어 있습니다.

## LRC 형식

시간이 지남에 따라 개발된 여러 형식의 LRC 파일이 있습니다. 이것들

### 단순 LRC 형식

라인 타임 태그는 `[mm:ss.xx]` 형식으로 되어 있습니다. 여기서 mm은 분, ss는 초, xx는 1/100초입니다.

```
[00:12.00]Line 1 lyrics
[00:17.20]Line 2 lyrics
[00:21.10]Line 3 lyrics
...
mm:ss.xxlast lyrics line
```

### 단순 형식 확장

M: Male, F: Female, D: Duet을 사용하여 가사의 성별을 변경하고 지정할 수 있는 기능이 포함되어 있습니다.

```
[00:12.00]Line 1 lyrics
[00:17.20]F: Line 2 lyrics
[00:21.10]M: Line 3 lyrics
[00:24.00]Line 4 lyrics
[00:28.25]D: Line 5 lyrics
[00:29.02]Line 6 lyrics
```
### 향상된 LRC 형식

향상된 LRC 형식은 단순 LRC 형식의 확장된 버전입니다. 형식에 Word 시간 태그를 추가합니다.`<mm:ss.xx>` 이전 단어의 끝에.

```
[ar: Jade Michael]
[al: Sarah Hi]
[au: Jade Michael]
[length: 2:58]
[by: lrc-maker]
[ti: Somebody to Love]

[00:00.00] <00:00.04> When <00:00.16> the <00:00.82> truth <00:01.29> is <00:01.63> found <00:03.09> to <00:03.37> be <00:05.92> lies
[00:06.47] <00:07.67> And <00:07.94> all <00:08.36> the <00:08.63> joy <00:10.28> within <00:10.53> you <00:13.09> dies
[00:13.34] <00:14.32> Don't <00:14.73> you <00:15.14> want <00:15.57> somebody <00:16.09> to <00:16.46> love
```

## 참고문헌

* [LRC 가사 파일 형식 - Wikipedia](https://en.wikipedia.org/wiki/LRC_(file_format))

