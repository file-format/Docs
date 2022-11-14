{
  "date" : "2021-08-11",
  "keywords" :[ "vdi 파일", "vdi 파일 형식", "vdi 파일이란", "파일", "vdi 예제", "vdi 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"VDI 파일 형식과 VDI 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"VDI - VirtualBox 가상 디스크 이미지 파일",
  "linktitle" : "VDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## .VDI 파일이란?
확장자가 .vdi인 파일은 가상 디스크 이미지입니다. VirtualBox라고 하는 Oracle의 오픈 소스 데스크탑 가상화 프로그램에만 해당됩니다. VDI 파일은 VirtualBox 가상 머신을 시작하는 데 사용됩니다. VM을 통해 사용자는 단일 컴퓨터에서 추가 운영 체제 또는 프로그램을 실행할 수 있습니다. 따라서 VDI 파일의 이점은 사용자가 이러한 디스크 이미지 파일을 하드 디스크에 저장할 수 있고 필요할 때마다 에뮬레이터를 사용하여 실행할 수 있다는 것입니다.

## VDI 파일 형식
VDI(가상 디스크 이미지)는 엔터프라이즈급 가상화 제품인 VirtualBox로 알려진 활발하게 개발된 오픈 소스 Oracle VM의 기본 디스크 파일 형식입니다. VDI 파일 형식은 다른 가상화 프로그램을 사용하여 쉽게 실행할 수 있는 휴대용 디스크 이미지를 만들 수 있도록 설계되었습니다. 동적으로 할당된 스토리지와 고정 크기 스토리지를 모두 지원합니다. 이미 데이터가 포함된 경우에도 생성된 후 이미지 파일을 확장할 수 있습니다.

### 디스크 가상화
시스템은 VDI 디스크 이미지 형식의 하드 디스크를 에뮬레이트합니다. VirtualBox VM은 Microsoft Virtual PC 또는 VMware에서 만든 이전 디스크와 고유한 형식을 사용할 수 있습니다. VirtualBox는 또한 가상 하드 디스크로 사용하여 호스트의 iSCSI 대상 및 원시 파티션에 연결할 수 있습니다. VirtualBox는 IDE(PIIX4 및 ICH6 컨트롤러), SATA(ICH8M 컨트롤러), 하드 드라이브를 연결할 수 있는 SAS 컨트롤러 및 SCSI를 에뮬레이트합니다.

VirtualBox 버전 2.2.0부터 OVF(Open Virtualization Format)에 대한 지원이 제공됩니다. 호스트에 연결된 물리적 장치와 ISO 이미지는 모두 CD 또는 DVD 드라이브로 마운트할 수 있습니다.
기본적으로 VirtualBox는 VESA 호환 맞춤형 가상 그래픽 카드를 통해 그래픽을 지원합니다.

### 이더넷에 대한 가상화 지원
VirtualBox는 이더넷 네트워크 어댑터에 대해 다음 네트워크 인터페이스 카드를 가상화합니다.
- AMD PCnet PCI II(Am79C970A)
- AMD PCnet-Fast III(Am79C973)
- Intel Pro/1000 MT 데스크탑(82540EM)
- Intel Pro/1000 MT 서버(82545EM)
- 인텔 Pro/1000 T 서버(82543GC)
- 반가상화 네트워크 어댑터(virtio-net)

에뮬레이트된 네트워크 카드를 사용하면 게스트 OS의 일부로 사용할 수 있으므로 네트워킹 하드웨어용 드라이버를 검색하고 설치할 필요 없이 게스트 OS를 실행할 수 있습니다. 특수 반가상화 네트워크 어댑터는 특정 하드웨어 인터페이스와 일치해야 할 필요성을 줄여 네트워크 성능을 향상시킵니다. 따라서 게스트에서 특별한 드라이버 지원이 필요합니다.


## 참고문헌

* [VirtualBox - 위키피디아 제공](https://en.wikipedia.org/wiki/VirtualBox#VirtualBox_Disk_Image)


