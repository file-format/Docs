{
  "date" : "2022-02-17",
  "keywords" :["gpg 파일", "gpg 파일 형식", "gpg 파일이란", "파일", "gpg 예", "gpg 파일 확장자","확장자", "형식"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPG 파일 - GNU Privacy Guard 공개 키링 파일",
  "description":"GPG 파일을 만들고 열 수 있는 API와 GPG 파일에 대해 알아보세요.",
  "linktitle" : "GPG",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-17"
}

## .GPG 파일이란?

GPG 파일은 GnuPG(GNU Privacy Guard) 암호화 프로그램에서 사용하는 암복호화 키 파일입니다. GnuPC 프로그램 자체는 RFC4880으로 정의된 OpenPGP 표준을 기반으로 하며 PGP라고도 합니다. 최신 운영 체제에서 GPG를 성공적으로 사용하는 열쇠는 다목적 키 관리 시스템입니다. GPG의 명령줄 유틸리티를 사용하면 다른 응용 프로그램과 쉽게 통합할 수 있습니다.

## GPG 파일 형식

GPG 파일은 암호화된 바이너리 파일로 저장되며 물론 사람이 읽을 수 없습니다. 암호화된 GPG 파일을 해독하려면 동일한 보안 키를 사용해야 합니다. 이것이 이러한 파일의 내부 파일 형식을 알 수 없는 이유입니다.

## Linux에서 GPG를 사용하여 파일 암호화 및 암호 해독

GPG 명령줄 유틸리티는 Linux에서 파일을 암호화하고 해독하는 데 사용할 수 있습니다.

### 파일 암호화

파일은 아래와 같이 -c(create) 옵션과 함께 gpg 명령을 사용하여 암호화할 수 있습니다.

```
gpg -c file1.txt
```
이 명령을 실행하면 원본 파일 `file1.txt`의 내용을 암호화하는 데 사용할 키 문구가 필요합니다. 그 결과 암호화된 파일 file1.txt.gpg가 생성됩니다.

### 파일 복호화 및 추출

암호화된 파일을 복호화하여 추출하기 위해 다음 명령어를 사용할 수 있습니다.

```
gpg cfile.txt.gpg
```

## 참고문헌

* [GNUPG](https://gnupg.org/)
* [HDF - 위키백과](https://en.wikipedia.org/wiki/Hierarchical_Data_Format)

