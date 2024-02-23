{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "XDELTA 파일 - xdelta 차등 파일 - .xdelta 파일이 무엇이며 어떻게 여나요?",
  "description" : "xdelta 차등 파일 및 여는 방법에 대해 알아보세요.",
  "linktitle" : "XDELTA",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-xdelta-ko",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## .XDELTA 파일이란?

XDELTA 파일 형식은 다른 두 파일 간의 이진 차이를 유지하며 두 파일 간의 차이를 계산하고 이러한 차이를 컴팩트 형식으로 인코딩하는 델타 인코딩용 명령줄 유틸리티인 xdelta 도구에 의해 생성됩니다. XDELTA 파일은 원본 파일과 업데이트된 파일 간의 변경 사항이나 차이점을 나타내는 이진 데이터를 저장합니다. XDELTA 파일의 이진 데이터는 한 파일(원본)을 다른 파일(업데이트 또는 패치 버전)로 변환하는 데 필요한 변경 사항을 나타냅니다.

XDELTA 파일은 게임 커뮤니티에서 비디오 게임의 수정 사항(모드)을 배포하는 데 자주 사용됩니다. 이러한 모드에는 외관상의 변경부터 게임플레이 메커니즘의 중요한 변경까지 모든 것이 포함될 수 있습니다. XDELTA 파일을 사용하면 XDELTA 파일에 지정된 변경 사항을 원본 게임 파일에 패치하여 사용자가 게임 설치에 이러한 수정 사항을 적용할 수 있습니다.

## 엑스델타

`xdelta`는 델타 인코딩 및 디코딩에 사용되는 명령줄 유틸리티입니다. 주로 두 파일 사이에 델타 패치 또는 xdelta 패치라고 불리는 바이너리 패치를 생성하고 적용하는 데 사용됩니다. 이러한 패치는 원본 파일과 수정 또는 업데이트된 버전 간의 차이점을 나타내므로 특히 대역폭이나 저장 공간이 제한된 시나리오에서 업데이트를 효율적으로 배포할 수 있습니다.

다음은 `xdelta`의 주요 기능에 대한 간략한 개요입니다.

1.  **Creating patches**: `xdelta` can generate a patch file that contains differences between two files. This patch file, often referred to as an "xdelta patch", is relatively small compared to original and updated files, as it only contains the changes between them.
    
2.  **Applying patches**: Once a patch file is created, `xdelta` can apply it to original file to produce updated file. This process involves taking original file and patch file as input and applying changes specified in patch file to generate updated file.
    
3.  **Applying reverse patches**: `xdelta` can also apply reverse patches, which revert changes made to a file. This is useful for rolling back updates or modifications.
    

xdelta'는 일반적으로 소프트웨어 업데이트 배포, 비디오 게임 패치, 내장 장치 또는 네트워크 기기의 시스템 파일 업데이트와 같은 다양한 시나리오에서 사용됩니다. 대역폭 사용량과 저장소 요구 사항을 최소화하면서 파일 업데이트를 관리하는 유연하고 효율적인 방법을 제공합니다.

## xdeltaui

xdeltaui는 XDELTA 패치를 관리하고 적용하기 위한 그래픽 사용자 인터페이스(GUI) 응용 프로그램입니다. xdelta gui는 사용자가 XDELTA 파일과 상호 작용하고 이를 해당 원본 파일에 적용하여 효과적으로 패치하거나 업데이트할 수 있는 사용자 친화적인 인터페이스를 제공합니다.

텍스트 기반 명령을 통해 작동하는 xdelta의 명령줄 버전과 달리 xdeltaui는 특히 명령줄 인터페이스에 익숙하지 않거나 그래픽 도구를 선호하는 사용자에게 XDELTA 파일을 처리하는 보다 직관적인 방법을 제공합니다.

xdeltaui를 사용하면 사용자는 일반적으로 원본 파일 선택, XDELTA 패치 파일 선택 및 패치 적용과 같은 작업을 수행하여 업데이트된 파일을 생성할 수 있습니다. 이는 비디오 게임이나 기타 소프트웨어 응용 프로그램에 대한 모드나 업데이트를 설치할 때 특히 유용할 수 있습니다.

## 엑스델타 다운로드

Linux 시스템에서는 `apt`, `yum` 또는 `dnf`와 같은 패키지 관리자를 사용하여 `xdelta`를 설치할 수 있습니다. 예를 들어 Ubuntu에서는 다음 명령을 사용할 수 있습니다.

```
sudo apt-get install xdelta3
```

## 엑스델타 사용법

`xdelta`를 사용하려면 일반적으로 다음과 같은 일반적인 단계를 따라야 합니다.

1.  **다운로드 및 설치**: 먼저 시스템에 'xdelta'가 설치되어 있는지 확인하세요. 공식 웹사이트, 패키지 관리자 또는 기타 신뢰할 수 있는 소스에서 다운로드할 수 있습니다.
    
2.  **Prepare Files**: Prepare original file (often called source or base file) and updated file (target file) that you want to create a patch for or apply a patch to.
    
3.  **패치 만들기**:
    
- 명령줄 인터페이스(터미널 또는 명령 프롬프트)를 엽니다.
- 적절한 옵션과 함께 `xdelta` 명령을 사용하여 패치를 만듭니다. 기본 구문은 다음과 같습니다.
               
````
엑스델타 델타<original_file><updated_file><patch_output_file>
````
        
` 교체<original_file> ` 원본 파일의 경로와 `<updated_file> ` 업데이트된 파일의 경로 및 `<patch_output_file> ` 원하는 패치 파일 이름으로.
- 예:
               
````
xdelta 델타 원본_파일 업데이트_파일 패치.xdelta
````
        
4.  **패치 적용**:
    
- 원본 파일과 패치 파일이 있는지 확인하세요.
- 명령줄 인터페이스를 엽니다.
- 적절한 옵션과 함께 `xdelta` 명령을 사용하여 패치를 적용합니다. 기본 구문은 다음과 같습니다.
        
      
````
xdelta 패치<original_file><patch_file><output_file>
````
        
` 교체<original_file> ` 원본 파일의 경로와 `<patch_file> ` 패치 파일 경로와 `<output_file> ` 원하는 출력 파일 이름으로.
- 예:
                
````
xdelta 패치 원본_파일 patch.xdelta 업데이트_파일
````
        
5.  **도움말 보기**: 특정 옵션이나 명령에 대한 도움이 필요한 경우 `--help` 옵션과 함께 `xdelta` 명령을 사용하여 사용 정보 및 사용 가능한 옵션을 표시할 수 있습니다.
    
## XDELTA 파일을 여는 방법

XDELTA 파일은 직접 열 수 없습니다. XDELTA 패치를 게임이나 다른 파일에 적용하려는 경우, 여러 플랫폼에서 호환되는 xdelta 또는 Windows 사용자를 위해 특별히 설계된 xdelta UI를 사용할 수 있습니다.

## 참고자료
* [엑스델타](https://en.wikipedia.org/wiki/Xdelta)


