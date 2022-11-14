{
  "date" : "2019-10-11",
  "keywords": [ "sh file", ".sh file", "extension", "format", "sh file example", "sh file format", "how to run sh file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SH - Bash 쉘 스크립트 파일",
  "description":"SH 파일 형식과 SH 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "SH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## .SH 파일이란?

확장자가 .sh인 파일은 Unix 셸에서 실행할 컴퓨터 프로그램이 포함된 스크립팅 언어 명령 파일입니다. 파일 처리, 프로그램 실행 및 기타 작업과 같은 작업을 수행하기 위해 순차적으로 실행되는 일련의 명령을 포함할 수 있습니다. 이들은 동시에 여러 작업을 수행하기 위해 사용자에 의해 또는 일괄적으로 명령줄 인터페이스에서 실행됩니다. 스크립트 파일은 메모장, 메모장++, Vim, Apple Terminal 및 Windows, MacOS 및 Linux OS의 기타 유사한 응용 프로그램과 같은 텍스트 편집기에서 열 수 있습니다.

## SH 파일 형식

SH 파일은 정의된 구문에 따라 일반 텍스트로 작성됩니다. 이러한 스크립트 파일은 다음을 지원합니다.

* `Comments` - 주석은 #으로 시작하고 쉘에서 무시됩니다.
* `바로 가기` - 짧고 쉬운 실행을 위해 명령 이름을 바꾸는 데 사용할 수 있습니다.
* `일괄 작업` - 수동으로 입력해야 하는 여러 명령을 자동으로 실행할 수 있습니다. 이렇게 하면 사용자가 시퀀스의 각 단계를 트리거할 때까지 기다릴 필요가 없습니다.
* '일반화' - 간단한 루프를 사용하여 이미지를 한 곳에서 다른 곳으로 변환하는 것과 같은 작업을 훨씬 더 일반화할 수 있습니다.

## SH 파일 예

```
$ echo '#!/bin/sh' > my-script.sh
$ echo 'echo Hello World' >> my-script.sh
$ cat my-script.sh
#!/bin/sh
echo Hello World
$ chmod 755 my-script.sh
$ ./my-script.sh
Hello World
```
## SH 파일을 실행하는 방법은 무엇입니까?
SH 파일은 일반적으로 Linux에서 실행되며 Windows에서도 sh 파일을 실행하려면 Putty와 같은 소프트웨어를 사용하여 Linux 터미널에 연결해야 합니다. 다음은 Linux 터미널에서 SH 파일을 실행하는 단계입니다.

1. Linux 터미널을 열고 SH 파일이 있는 디렉토리로 이동합니다.
2. `chmod` 명령을 사용하여 스크립트에 대한 실행 권한을 설정합니다(아직 설정하지 않은 경우).
3. 다음 중 하나를 사용하여 스크립트를 실행합니다.
1. `./파일명.sh`
2. `sh 파일 이름.sh`
3. `bash 스크립트 이름-here.sh`

## 참고문헌

* [초보자를 위한 Bashscripting](https://help.ubuntu.com/community/Beginners/BashScripting)
* [쉘스크립트](https://www.shellscript.sh/)

