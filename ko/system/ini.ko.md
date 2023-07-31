{
  "date" : "2021-07-07",
  "keywords" :[ "INI", "확장자", "파일", "형식", "시스템", "초기화", "디렉토리 확장명", "프로그램", "컴퓨터", "응용 프로그램"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"INI - 시작 파일 형식",
  "description":"INI 파일을 만들고 열 수 있는 INI 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "INI",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## .INI 파일이란? ##

INI 파일은 프레임워크 및 문법에서 속성을 구성하는 특성 및 섹션에 대한 공개 키를 포함하는 컴퓨터 프로그램에 대한 메시지 구성 문서입니다. 이러한 시스템 파일 형식 구성 문서는 MS-DOS 운영 체제의 디렉토리 확장자 INI에서 이름을 가져옵니다. 이는 초기화를 의미합니다. 이 형태의 소프트웨어 설정을 대중화했습니다. 다른 소프트웨어 응용 프로그램의 많은 프로그램은 CONF 및 [CFG](/ko/system/cfg/)와 같은 다양한 파일 이름 추가를 사용하지만 많은 구성 상황에서 형식이 비공식 표준을 설정했습니다.

## INI 파일의 간략한 역사##

처음에 Windows의 주요 프로그램 구성 기술은 섹션으로 나누어진 한 줄에 중요한 쌍이 있는 텍스트 줄로 구성된 텍스트 파일 형식이었습니다. 장치 드라이버, 서체 및 시작 런처가 모두 이 형식으로 저장되었습니다. 개별 설정도 일반적으로 앱에서 INI 파일에 저장했습니다.
Windows 3.1x까지 형식은 16비트 Microsoft Windows 플랫폼에서 지원되었습니다. Windows 95부터 Microsoft는 개발자가 구성을 위해 INI 파일 대신 Windows 레지스트리를 사용하도록 권장하기 시작했습니다.

## INI 파일 - 파일 형식 사양

### 키/속성 ###

키/속성은 INI 파일의 가장 기본적인 요소입니다. 등호(=)는 각 키의 이름과 값을 구분합니다. 등호 왼쪽에는 이름이 표시됩니다. 등호와 세미콜론은 Windows 시스템에서 눈에 띄지 않는 문자이므로 키에 사용할 수 없습니다. 값에는 모든 문자를 사용할 수 있습니다.

```
name=value
```

### 섹션 ###

섹션 주석은 한 줄에 대괄호([])로 표시됩니다. 섹션 정의 후 모든 키가 해당 섹션에 연결됩니다. 섹션은 바로 다음 섹션 지정 또는 문서의 끝에서 끝납니다. 특정 "섹션 끝" 구분 기호가 없습니다. 섹션은 쌓을 수 없습니다. 이름은 한 번만 지정할 수 있으며 연결할 필요가 없습니다.

```
[section]
a=a
b=b
```

### 기능 변경 ###

INI 파일 형식에는 전역적으로 허용되는 정의가 없습니다. 많은 컴퓨터 응용 프로그램에는 이미 언급한 기능 외에도 기능이 포함되어 있습니다. 아래 목록에는 개별 프로그램에 포함되거나 포함되지 않을 수 있는 몇 가지 일반적인 특성이 포함되어 있습니다.

* 코멘트
* 이스케이프 문자
* 중복된 이름


## INI 예제 ##

샘플 INI 파일은 다음과 같습니다.

```
[Settings]
 
#======================================================================
 
# Set detailed log for additional debugging info
 
DetailedLog=1
 
RunStatus=1
 
StatusPort=6090
 
StatusRefresh=10
 
Archive=1
 
# Sets the location of the MV_FTP log file
 
LogFile=/opt/ecs/mvuser/MV_IPTel/log/MV_IPTel.log
 
#======================================================================
 
Version=0.9 Build 4 Created July 11 2004 14:00
 
ServerName=Unknown

```

## 참조 ##

* [DMP - 마이크로소프트](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

