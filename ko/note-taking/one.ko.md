{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONE - Microsoft OneNote 파일 형식",
  "description":"하나의 파일을 만들고 열 수 있는 하나의 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "ONE",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## .ONE 파일이란 무엇입니까? ##

.ONE 확장자로 표시되는 파일은 Microsoft OneNote 응용 프로그램에서 생성됩니다. OneNote를 사용하면 초안을 메모에 사용하는 것처럼 응용 프로그램을 사용하여 정보를 수집할 수 있습니다. OneNote 파일에는 문서 페이지의 고정되지 않은 위치에 배치할 수 있는 다양한 요소가 포함될 수 있습니다. 이러한 요소에는 텍스트, 디지털화된 손글씨, 이미지, 그림 및 멀티미디어(오디오/비디오) 클립을 비롯한 다른 응용 프로그램에서 복사한 개체가 포함될 수 있습니다. Microsoft는 이제 인터넷을 통해 다른 OneNote 사용자와 노트를 공유할 수 있는 Office365의 일부로 온라인 버전의 OneNote를 제공합니다.

## .ONE 파일 형식 사양 ##

OneNote 파일 형식은 디지털 노트를 섹션 및 페이지의 계층적 집합으로 나타내는 효과적인 방법을 제공합니다. 각 페이지에는 파일 형식 DOM(문서 개체 모델)으로 표시하기 위한 특정 구조의 사용자 정의 콘텐츠가 포함되어 있습니다. 이 형식의 데이터 모델은 다음과 같습니다.

### 구조 개요 ###

OneNote 파일 형식의 데이터 모델에 나와 있는 것처럼 OneNote 문서는 다양한 요소로 구성됩니다.

#### 부분 ####

섹션은 다음과 같은 다양한 요소를 추가로 포함하는 OneNote 파일의 최상위 컨테이너입니다.

* 페이지
* 메타데이터
* 속성

메타데이터 및 속성에는 섹션 이름, 섹션에 포함된 페이지 식별 및 해당 페이지가 표시되는 순서가 포함됩니다. "섹션"이라는 용어는 섹션에 있는 모든 페이지와 파일 이름 확장명이 .one인 OneNote® 개정 저장소 파일의 해당 데이터 표현을 나타냅니다.

#### 페이지 ####

OneNote 문서의 사용자 정의 콘텐츠는 페이지 안에 포함됩니다. 페이지 정보에는 텍스트, 목록, 표, 페이지 제목, 이미지 및 메모 태그가 포함됩니다. 페이지는 대부분의 포함된 개체가 추가되는 개요 개체로 구성됩니다. 의미 있는 표현을 위해 각 페이지에 이름을 할당할 수 있으며 개체를 페이지에 직접 추가할 수도 있습니다. 페이지는 계층적 시스템의 하위 페이지를 더 포함할 수 있습니다.

#### 속성 및 속성 집합 ####

OneNote 콘텐츠는 속성, 속성 집합 및 파일 데이터 개체로 구성됩니다. 속성 집합은 일부 콘텐츠 유형을 나타내는 속성 모음입니다. 파일 데이터 개체는 그림, 포함된 파일 또는 오디오/비디오 콘텐츠를 포함하는 이진 데이터 블록입니다.

#### OneNote 노트북 ####

노트북은 동일한 디렉토리에 저장된 섹션 파일의 모음입니다. 속성 모음은 노트북 내의 섹션 순서 및 노트북 색상과 같은 설정을 지정하는 데 사용됩니다.

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

|파일 형식|값
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile(4바이트):` 부호 없는 정수입니다. 이 파일의 파일 형식에 따라 다음 표에 있는 값 중 하나여야 합니다(MUST).

|파일 형식|값
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`fcrLegacyFreeChunkList(8바이트):` "fcrZero" 값을 가져야 하는 **FileChunkReference32** 구조입니다.

`fcrLegacyTransactionLog(8바이트):` "fcrNil"이어야 하는 **FileChunkReference32** 구조입니다.

`cTransactionsInLog(4바이트):` 트랜잭션 로그의 트랜잭션 수를 지정하는 부호 없는 정수입니다. 0이 아니어야 합니다.

`cbLegacyExpectedFileLength(4바이트):` 0이어야 하고 무시되어야 하는 부호 없는 정수입니다.

`rgbPlaceholder(8바이트):` 0이어야 하고 무시되어야 하는 부호 없는 정수입니다.

`fcrLegacyFileNodeListRoot(8바이트):` "fcrNil"이어야 하는 **FileChunkReference32** 구조입니다.

`cbLegacyFreeSpaceInFreeChunkList(4바이트):` 0이어야 하고 무시되어야 하는 부호 없는 정수입니다.

`fNeedsDefrag(1바이트):`는 무시되어야 합니다(MUST).

`fRepairedFile(1바이트):`은 무시해야 합니다.

`fNeedsGarbageCollect(1바이트):`는 무시되어야 합니다(MUST).

`fHasNoEmbeddedFileObjects(1바이트):` 0이어야 하고 무시되어야 하는 부호 없는 정수입니다.

`guidAncestor(16바이트):` 목차 파일의 **Header.guidFile** 필드를 지정하는 GUID로, 다음 표에 나와 있습니다.


|목차 파일 형식|목차 파일의 위치
--- | --- |
|섹션 파일 - .One|목차 파일은 이 파일과 같은 디렉토리에 있습니다.
|목차 파일 - .onetoc2|목차 파일은 이 파일의 상위 디렉토리에 있습니다.

GUID가 {00000000-0000-0000-0000-000000000000}인 경우 이 필드는 목차 파일을 참조하지 않습니다.

`crcName(4바이트):` 이 개정 저장소 파일 이름의 CRC 값을 지정하는 부호 없는 정수입니다. 이름은 확장자와 끝에 추가 널 문자가 있는 파일 이름의 유니코드 표현입니다. 이 CRC는 이 개정 저장소 파일 형식에 관계없이 항상 .one 파일에 대한 CRC 알고리즘을 사용하여 계산됩니다.

`fcrHashedChunkList(12바이트):` 해시된 청크 목록의 첫 번째 **FileNodeListFragment**에 대한 참조를 지정하는 **FileChunkReference64x32** 구조입니다. **FileChunkReference64x32** 구조의 값이 "fcrZero" 또는 "fcrNil"이면 해시된 청크 목록이 존재하지 않습니다.

`fcrTransactionLog(12바이트):` 트랜잭션 로그의 첫 번째 **TransactionLogFragment** 구조에 대한 참조를 지정하는 **FileChunkReference64x32** 구조입니다. **fcrTransactionLog** 필드의 값은 "fcrZero"가 아니어야 하고 "fcrNil"이 아니어야 합니다(MUST NOT).

`fcrFileNodeListRoot(12바이트):` 루트 파일 노드 목록에 대한 참조를 지정하는 **FileChunkReference64x32** 구조입니다. **fcrFileNodeListRoot** 필드의 값은 "fcrZero"가 아니어야 하고 "fcrNil"이 아니어야 합니다(MUST NOT).

`fcrFreeChunkList(12바이트):` 첫 번째 **FreeChunkListFragment** 구조에 대한 참조를 지정하는 **FileChunkReference64x32** 구조입니다. **FileChunkReference64x32** 구조의 값이 "fcrZero" 또는 "fcrNil"이면 여유 청크 목록이 존재하지 않습니다.

`cbExpectedFileLength (8 bytes):` 이 개정 저장소 파일의 크기를 바이트 단위로 지정하는 부호 없는 정수입니다.

`cbFreeSpaceInFreeChunkList(8바이트):` 여유 청크 목록에 의해 지정된 여유 공간의 크기를 바이트 단위로 지정해야 하는 부호 없는 정수입니다.

`guidFileVersion(16바이트):` GUID입니다. **cTransactionsInLog** 필드 또는 **guidDenyReadFileVersion** 필드 값이 변경되는 경우 **guidFileVersion**을 새 GUID로 변경해야 합니다(MUST).

`nFileVersionGeneration(8바이트):` 파일이 변경된 횟수를 지정하는 부호 없는 정수입니다. **guidFileVersion** 필드가 변경되면 증가해야 합니다(MUST).

`guidDenyReadFileVersion(16바이트):` GUID입니다. 파일의 **Header** 구조와 사용하지 않는 저장 블록을 제외하고 파일의 기존 내용이 변경되는 경우 **guidDenyReadFileVersion**을 새 GUID로 변경해야 합니다(MUST).

`grfDebugLogFlags(4바이트):`는 0이어야 합니다. 무시해야 합니다.

`fcrDebugLog(12바이트):` 값이 "fcrZero"여야 하는 **FileChunkReference64x32** 구조입니다. 무시해야 합니다.

`fcrAllocVerificationFreeChunkList(12바이트):` "fcrZero"여야 하는 **FileChunkReference64x32** 구조입니다. 무시해야 합니다.

`bnCreated (4 bytes):` 이 개정 저장소 파일을 만든 응용 프로그램의 빌드 번호를 지정하는 부호 없는 정수입니다. 무시해야 합니다(SHOULD).

`bnLastWroteToThisFile(4바이트):` 이 개정 저장소 파일에 마지막으로 쓴 응용 프로그램의 빌드 번호를 지정하는 부호 없는 정수입니다. 무시해야 합니다(SHOULD).

`bnOldestWritten(4바이트):` 이 개정 저장소 파일에 쓴 가장 오래된 응용 프로그램의 빌드 번호를 지정하는 부호 없는 정수입니다. 무시해야 합니다(SHOULD).

`bnNewestWritten(4바이트):` 이 개정 저장소 파일에 쓴 최신 응용 프로그램의 빌드 번호를 지정하는 부호 없는 정수입니다. 무시해야 합니다(SHOULD).

`rgbReserved(728바이트):`는 0이어야 합니다. 무시해야 합니다.

## 참조 ##

* [[MS-ONESTORE] - OneNote 파일 형식](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [마이크로소프트 원노트 - 위키피디아](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

