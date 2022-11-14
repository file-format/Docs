{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONETOC2 - Microsoft OneNote 파일 형식",
  "description":"ONETOC2 파일 형식 및 ONETOC2 파일을 생성하고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "ONETOC2",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## ONETOC2는 무엇입니까? ##

[Microsoft OneNote](https://products.office.com/en-us/onenote/digital-note-taking-app) 응용 프로그램을 사용해 본 사람들은 노트북 폴더에 .onetoc2 파일이 있음을 눈치 챘을 것입니다. Microsoft OneNote는 전자 필기장에서 여러 노트 작성 섹션의 순서에 대한 색인을 유지하기 위해 목차로 바이너리 .onetoc2 파일을 만듭니다. 노트북은 동일한 디렉토리에 저장된 섹션 파일의 모음입니다. .onetoc2 파일은 속성 모음을 사용하여 노트북 내의 섹션 순서 및 노트북 색상과 같은 설정을 지정합니다.

OneNote 2016에서 전자 필기장을 만들면 자동으로 새로운 2010-2016 파일 형식으로 저장됩니다. 수학 방정식 및 연결된 노트와 같은 OneNote 2016의 모든 기능이 제대로 작동하려면 이 형식이 필요합니다.

## ONETOC2 파일 형식 ##

.onetoc2 파일 형식은 OneNote 개정 저장소 파일 형식으로 표시되며, 상호 참조된 개체 공간으로 구성된 개정 저장소를 지정하는 구조의 모음입니다. 씁니다. .onetoc2 파일 형식에 대한 전체 사양은 [온라인](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)에서 볼 수 있으며 응용 프로그램 개발에 참조할 수 있습니다. .

### 파일 구조 ###

개정 저장소 파일은 **Header** 구조로 시작해야 합니다(MUST). 파일의 나머지 부분은 바이트 블록으로 분할되며 각 블록의 크기와 구조는 해당 블록을 참조하는 필드에 의해 지정됩니다. 블록이 **Header** 구조에서 참조되거나 도달 가능한 다른 블록의 필드에서 참조되는 경우 블록에 도달할 수 있습니다. **Header** 구조 외부의 데이터와 도달 가능한 모든 블록은 무시되어야 합니다(MUST).

모든 구조는 1바이트 경계로 정렬됩니다. 달리 지정하지 않는 한 모든 정수는 부호가 있습니다. 달리 지정되지 않는 한 모든 필드는 [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7)입니다.

#### 헤더 ####

.ONE 파일의 헤더는 다음과 같이 파일 정보를 표현하기 위한 서로 다른 고유 ID와 필드를 포함하는 청크로 구성됩니다.

`guidFileType(16바이트):` 개정 저장소 파일의 유형을 지정하는 GUID입니다. 다음 표의 값 중 하나여야 합니다(MUST).

|파일 형식|값
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile(16바이트):` 이 개정 저장소 파일의 ID를 지정하는 GUID입니다. 전역적으로 고유해야 합니다(SHOULD).

`guidLegacyFileVersion(16바이트):`은 "{00000000-0000-0000-0000-000000000000}"이어야 하며 무시되어야 합니다(MUST).

`guidFileFormat(16바이트):` 파일이 개정 저장소 파일임을 지정하는 GUID입니다. '{109ADD3F-911B-49F5-A5D0-1791EDC8AED8}'여야 합니다.

`ffvLastCodeThatWroteToThisFile(4바이트):` 부호 없는 정수입니다. 파일 유형에 따라 다음 표에 있는 값 중 하나여야 합니다(MUST).

|파일 형식|값
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHasWrittenToThisFile(4바이트):` 부호 없는 정수입니다. 이 파일의 파일 형식에 따라 다음 표에 있는 값 중 하나여야 합니다(MUST).


|파일 형식|값
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile(4바이트):` 부호 없는 정수입니다. 이 파일의 파일 형식에 따라 다음 표에 있는 값 중 하나여야 합니다(MUST).
:


|파일 형식|값
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile(4바이트):` 부호 없는 정수입니다. 이 파일의 파일 형식에 따라 다음 표에 있는 값 중 하나여야 합니다(MUST).


|파일 형식|값
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

## 참조 ##

* [[MS-ONESTORE] - OneNote 파일 형식](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [마이크로소프트 원노트 - 위키피디아](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

