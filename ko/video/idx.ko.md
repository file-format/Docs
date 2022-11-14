{
  "date" : "2022-07-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IDX - 고효율 비디오 코덱",
  "description":"IDX 파일 형식과 IDX 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "IDX",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-12"
}

## .IDX 파일이란?

IDX 파일은 .sub(VobSub 자막) 파일 내의 자막에 대한 메타데이터 정보 목록을 가리키는 자막 색인 파일입니다. 사용자가 DVD에서 자막을 추출하고 SUB 파일에 덤프할 수 있는 VobSub 소프트웨어 응용 프로그램에서 만들고 사용합니다. IDX 파일에는 모든 단일 자막을 가리키는 데 사용되는 타임스탬프와 바이트 오프셋이 포함되어 있습니다. VobSub는 항상 해당 SUB 파일과 함께 IDX 파일을 생성합니다.

## IDX 파일 형식 - 추가 정보

IDX 파일은 모든 텍스트 편집기에서 열 수 있는 일반 텍스트 파일로 생성 및 저장됩니다. IDX 파일에는 화면에 표시할 자막 텍스트의 색상, 화면에서 자막 텍스트의 위치와 같은 매개변수를 읽기 위해 미디어 플레이어가 읽는 정보가 포함되어 있습니다.

### IDX 자막 설정

일반적인 IDX 파일은 파일 시작 부분에 이 메타데이터 정보를 저장합니다. 자막 설정은 **#**로 시작합니다. 타임스탬프와 이미지 참조는 이러한 모든 자막 설정 뒤에 추가되며 **timestamp:**로 시작합니다.

## IDX 파일 형식 예

```
# VobSub index file, v7 (do not modify this line!)
#
# To repair desyncronization, you can insert gaps this way:
# (it usually happens after vob id changes)
#
#	 delay: [sign]hh:mm:ss:ms
#
# Where:
#	 [sign]: +, - (optional)
#	 hh: hours (0 <= hh)
#	 mm/ss: minutes/seconds (0 <= mm/ss <= 59)
#	 ms: milliseconds (0 <= ms <= 999)
#
#	 Note: You can't position a sub before the previous with a negative value.
#
# You can also modify timestamps or delete a few subs you don't like.
# Just make sure they stay in increasing order.


# Settings

# Original frame size
size: 720x576

# Origin, relative to the upper-left corner, can be overloaded by aligment
org: 0, 0

# Image scaling (hor,ver), origin is at the upper-left corner or at the alignment coord (x, y)
scale: 100%, 100%

# Alpha blending
alpha: 100%

# Smoothing for very blocky images (use OLD for no filtering)
smooth: OFF

# In millisecs
fadein/out: 50, 50

# Force subtitle placement relative to (org.x, org.y)
align: OFF at LEFT TOP

# For correcting non-progressive desync. (in millisecs or hh:mm:ss:ms)
# Note: Not effective in DirectVobSub, use "delay: ... " instead.
time offset: 0

# ON: displays only forced subtitles, OFF: shows everything
forced subs: OFF

# The original palette of the DVD
palette: 000000, 828282, 828282, 828282, 828282, 828282, 828282, ffffff, 828282, bababa, 828282, 828282, 828282, 828282, 828282, 828282

# Custom colors (transp idxs and the four colors)
custom colors: OFF, tridx: 1000, colors: 000000, bababa, 828282, 000000

# Language index in use
langidx: 0

# English
id: en, index: 0
# Decomment next line to activate alternative name in DirectVobSub / Windows Media Player 6.x
# alt: English
# Vob/Cell ID: 1, 1 (PTS: 0)
timestamp: 00:01:25:880, filepos: 000003800
timestamp: 00:01:46:160, filepos: 000008000
timestamp: 00:02:08:880, filepos: 00000c800
# Vob/Cell ID: 1, 2 (PTS: 222840)
timestamp: 00:03:58:800, filepos: 000011000
timestamp: 00:04:00:680, filepos: 000016800
timestamp: 00:04:04:640, filepos: 00001d800
```

## IDX 파일을 사용하는 방법?

영화에 대한 Sub 및 IDX 파일이 있는 경우 이러한 자막이 생성된 영화와 함께 이러한 자막을 재생할 수 있습니다. VLC, GOM Player, PotPlayer 또는 PowerDVD와 같은 많은 응용 프로그램에는 이러한 SUB 및 IDX 파일을 로드하고 영화와 함께 재생할 수 있는 기능이 있습니다. 소프트웨어 응용 프로그램은 [.mkv](/ko/video/mkv/) 파일에 SUB 및 IDX 자막 파일을 포함할 수도 있습니다.

## IDX를 SRT로 변환

[SRT](/ko/video/srt/)(SubRip 파일 형식)는 SubRip 파일 형식으로 저장된 간단한 자막 파일입니다. VobSub 파일 형식에 비해 더 일반적으로 사용됩니다. 따라서 SUB/IDX 파일을 SRT 파일 형식으로 변환하려는 경우 이를 달성하는 데 사용할 수 있는 타사 도구가 있습니다. SubtitleTools.com에서 사용할 수 있는 SUB/IDX to SRT 변환기는 SUB 및 IDX 파일을 입력으로 사용하고 이러한 VobSub 자막을 SRT 파일로 변환하는 도구 중 하나입니다.

## 참고문헌

* [VobSub](https://www.videohelp.com/software/VobSub)
* [VOBsub - 위키 멀티미디어](https://wiki.multimedia.cx/index.php?title=VOBsub)

