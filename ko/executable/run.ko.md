{
  "date" : "2023-01-31",
  "keywords" :["실행 파일", "실행 파일이란 무엇입니까", "파일", "실행 파일 여는 방법", "실행 파일 확장자","확장자"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"RUN 파일 형식과 RUN 파일을 생성하고 열 수 있는 API에 대해 알아보세요.",
  "title" :"RUN 파일 형식 - Linux 실행 파일",
  "linktitle" : "RUN",
  "menu" : {
    "docs" : {
      "identifier":"executable-run",
      "parent" : "executable"
}
},
  "lastmod" : "2023-01-31"
}

## .RUN 파일이란 무엇입니까?

.run 파일 형식은 Linux 환경에서 소프트웨어 또는 응용 프로그램 설치 프로그램을 배포하는 데 일반적으로 사용됩니다. 소프트웨어를 설치하려면 파일을 실행 가능하게 만들어야 하며 다음 명령을 사용하여 수행할 수 있습니다.

```bash
chmod +x file_name.run 
```

그런 다음 다음 명령을 사용하여 파일을 실행할 수 있습니다.

```bash
./file_name.run 
```

설치 프로세스는 설치하려는 특정 파일 및 프로그램에 따라 다를 수 있습니다.

.run 파일 형식은 Linux 환경에서 소프트웨어 또는 응용 프로그램 설치 프로그램을 배포하는 데 사용되는 일종의 셸 스크립트입니다. 바이너리 파일, 라이브러리 및 구성 파일을 포함하여 소프트웨어를 설치하는 데 필요한 모든 것이 포함된 독립형 패키지입니다.

.run 파일에는 악성 코드도 포함될 수 있으므로 파일을 실행하기 전에 항상 파일 소스를 확인하고 바이러스를 검사하는 것이 좋습니다.

또한 일부 .run 파일을 실행하고 설치하려면 루트 권한이 필요할 수 있으므로 "sudo" 명령을 사용하여 높은 권한으로 파일을 실행해야 할 수도 있습니다.

```bash
sudo ./filename.run
```

## RUN 파일 여는 방법?

.run 파일을 열려면 해당 파일을 실행 가능하게 만들어야 하며 "chmod" 명령을 사용하여 수행할 수 있습니다.

```bash
chmod +x filename.run 
```

파일이 실행 가능해지면 다음을 입력하여 실행할 수 있습니다.

```bash
./filename.run
```

.run 파일을 실행하는 것은 텍스트 편집기에서 여는 것과 다릅니다. .run 파일을 실행하면 프로그램 설치부터 스크립트 실행까지 모든 명령이 실행됩니다. .run 파일의 내용을 보려면 nano 또는 vim과 같은 텍스트 편집기에서 파일을 열어야 합니다.

```
nano filename.run
```
또는
```
vim filename.run
```

## 참고자료
* [Ubuntu에서 .bin 및 .run 파일을 실행하는 방법](https://vitux.com/how-to-execute-bin-and-run-files-in-ubuntu/)


