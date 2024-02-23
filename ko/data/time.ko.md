{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "TIME 파일 - .time 파일이란 무엇입니까? Linux에서 파일이 생성된 시간",
  "description" : "TIME 파일에 대해 알아보고 Linux에서 파일이 생성된 시간을 알아보세요.",
  "linktitle" : "TIME",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-time-ko",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## .TIME 파일이란?

TIME 파일 형식은 LIGHT라는 웹 시스템에서 사용되어 사용자가 자신의 삶을 기록하고 정리하고 공유하는 데 도움이 되었습니다. 기본적으로 이는 게시물 모음을 저장하고 시스템 내 사용자 라이프 페이지의 폴더를 나타냅니다.

## Linux에서 파일이 언제 생성되었는지 확인하는 방법

Linux에서는 `stat` 명령을 사용하여 파일이 생성된 시기를 확인할 수 있습니다. 방법은 다음과 같습니다.

터미널을 열고 다음 명령을 입력하십시오.

```
stat <file_path>
```

` 교체<file_path> ` 관심 있는 파일의 경로를 입력하세요. 예:

```
stat /path/to/your/file.txt
```

이 명령은 생성 시간을 포함하여 파일에 대한 다양한 정보를 표시합니다. Birth 또는 File:으로 시작하는 줄을 찾으세요. 생성 시간은 파일 시스템에서 파일이 생성된 시간을 나타냅니다.

다음은 출력 결과의 예입니다.

```
  File: /path/to/your/file.txt
  Size: 1024       	Blocks: 8          IO Block: 4096   regular file
Device: 801h/2049d	Inode: 1643318     Links: 1
Access: (0644/-rw-r--r--)  Uid: ( 1000/   user)   Gid: ( 1000/   user)
Access: 2024-01-31 12:34:56.789012345 +0000
Modify: 2024-01-31 12:34:56.789012345 +0000
Change: 2024-01-31 12:34:56.789012345 +0000
 Birth: 2024-01-31 12:34:56.789012345 +0000
```

이 예에서 생성 시간은 파일이 생성된 시간을 나타냅니다.

