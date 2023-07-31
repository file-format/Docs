{
  "date" : "2022-07-22",
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"VHDX 파일 형식과 VHDX 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"VHDX 파일 형식 - VHDX 파일이란 무엇입니까?",
  "linktitle" : "VHDX",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-07-22"
}

## .VHDX 파일이란?

VHDX 파일은 가상 하드 디스크 v2 파일 형식의 디스크 이미지 파일입니다. 여기에는 특정 운영 체제가 필요한 소프트웨어 또는 실행 소프트웨어 테스트를 위한 일반 시스템으로 로드 및 사용할 수 있는 전체 운영 체제가 포함되어 있습니다. VHDX는 전체 디스크 이미지임에도 불구하고 단일 파일에 저장됩니다. Parallels Desktop, Windows Virtual Machine 및 Virtual Box와 같은 가상 컴퓨터 소프트웨어는 디스크 이미지를 로드하고 열 수 있습니다.

VHDX 파일은 Hyper-V Manager를 사용하여 [VHD](/ko/disc-and-media/vhd/)로 변환하거나 VirtualBox를 사용하여 [VDI](/ko/disc-and-media/vdi/)로 변환할 수 있습니다.

## VHDX 파일 형식 - 추가 정보

VHDX 파일 형식 세부 정보는 완전히 문서화되어 있으며 [VHDX 파일 형식 사양](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477)으로 온라인에서 사용할 수 있습니다. ) Microsoft 설명서에 있습니다. VHD 형식의 확장이며 향상된 기능을 포함합니다. VHDX 파일 형식은 가상 하드 디스크 및 가상 하드 디스크 파일 계층에서 사용할 수 있는 추가 기능을 제공합니다. 스토리지 하드웨어 구성 및 기능에 대해 더 최적화되고 더 나은 결과를 제공합니다. VHDX 파일을 열 수 있습니다.

### VHDX에서 가상 하드 디스크 지원

세 가지 유형의 가상 하드 디스크를 지원합니다.

1. **고정 가상 하드 디스크** - 고정 데이터 크기가 할당된 가상 하드 디스크입니다. 가상 하드 디스크의 크기는 데이터를 추가하거나 제거해도 변경되지 않습니다.

1. **동적 가상 하드 디스크** - 동적 디스크 크기의 가상 하드 디스크. 크기는 언제든지 기록된 실제 데이터 및 메타데이터만큼 큽니다. 파일 크기는 데이터가 추가되거나 제거될 때 동적으로 증가합니다.

1. **Differencing Virtual Hard Disk** - 상위 가상 하드 디스크 파일과 비교하여 수정된 블록 집합으로 가상 하드 디스크의 현재를 나타냅니다.

## 참고문헌

* [VHDX 파일 형식 사양](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477)
* [VHD - 위키피디아 제공](https://en.wikipedia.org/wiki/VHD_(file_format))

