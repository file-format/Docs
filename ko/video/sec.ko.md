---
date: 2022-03-25
keywords: sec, .sec, sec 파일 형식, .sec 파일 형식, .sec 확장자, sec 확장자
작가:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "SEC 파일 형식과 SEC 파일을 만들고 열 수 있는 API에 대해 알아보세요."
title: SEC 파일 형식 - 삼성 보안 동영상 파일
linktitle: SEC
menu:
  docs:
    parent: "video"
lastmod: 2022-03-25
---

## .SEC 파일이란?

SEC 파일은 삼성 DVR 감시 시스템으로 생성된 동영상 파일입니다. 비디오는 감시 카메라에서 캡처되어 SEC 형식으로 디스크에 저장됩니다. 녹화된 SEC 비디오는 여러 카메라의 비디오 피드를 관리할 수 있는 삼성의 비디오 소프트웨어로 재생할 수 있습니다.

## SEC 파일 형식 - 추가 정보

SEC 파일에는 독점 파일 형식을 사용하여 내부에 h264/AVC 스트림이 포함되어 있습니다. SEC 파일의 헤더는 SRD-1670D의 모델 번호로 시작합니다. 날짜 및 시간 정보는 파일 끝에 있습니다.

### SEC 파일을 AVI로 변환

SEC 파일은 FFmpeg를 사용하여 표준 [AVI](/ko/video/avi/) 파일 형식으로 변환할 수 있습니다.

```
ffmpeg -i 0010600.sec -vcodec copy -vsync drop -fflags genpts -f avi 0010600.avi
```

## 참조 ##

- [삼성 및 SEC 파일](https://spreadys.wordpress.com/2013/07/19/samsung-and-sec-files/)

