{
"날짜": "2023-06-08",
  "keywords": [
"vmx 파일",
"vmx 파일이 무엇인가요?",
"vmx 파일 예",
"vmx 파일을 여는 방법",
"vmx 파일에는 무엇이 포함되어 있나요?",
"vmx 파일의 형식은 무엇입니까",
"파일",
"VMX 파일 확장자",
"확대"
],
  "author": {
"display_name": "샤킬 파이즈"
},
"draft": "false",
"toc": true,
"title": "VMX 파일 형식 - VMware 가상 머신 구성 파일",
  "description":"VMX 파일을 생성하고 열 수 있는 VMX 형식과 API에 대해 알아보세요.",
"linktitle": "VMX",
  "menu": {
    "docs": {
      "identifier": "settings-vmx",
"parent": "설정"
}
},
"lastmod": "2023-06-08"
}

## VMX 파일이란 무엇입니까?

가상 머신 구성 파일이라고도 알려진 VMX 파일은 VMware 가상화 소프트웨어에서 가상 머신(VM)의 설정 및 구성을 정의하는 데 사용되는 일반 텍스트 파일입니다. VMX 파일에는 VM의 하드웨어 구성, 가상 디스크 매핑, 네트워크 설정 및 기타 매개변수와 같은 정보가 포함되어 있습니다.

## VMX 파일 예

다음은 VMX 파일의 모양에 대한 예입니다.

```
# version for configuration
config.version = "8"
# version for virtual machine (Regular version is 4)
virtualHW.version = "7"
# enable vnc
RemoteDisplay.vnc.enabled = "TRUE"
RemoteDisplay.vnc.port = "5900"
VMware, Inc. 3

# type of guest os
guestOS = "linux"
# display name for the VI Client/WebCenter
displayName = "RHEL3"
# scsi controller 0
scsi0.present = "true"
scsi0.virtualDev = "lsilogic"
# scsi hard drive
scsi0:0.present = "true"
scsi0:0.fileName = "/volumes/your-path/passthru.vmdk"
scsi0:0.deviceType = "scsi-hardDisk"
scsi0:0.redo = ""
# IDE CD drive
ide0:0.present ="true"
ide0:0.startConnected = "TRUE"
ide0:0.fileName = "/volumes/your-path/your-iso-image"
ide0:0.deviceType = "cdrom-image"
memsize = "512"
sched.mem.max = "512"
sched.mem.minsize = "512"
sched.swap.derivedName = "/volumes/your-path/passthru-12345.vswp"
svga.vramSize = "16777216"
```

## VMX 파일에는 무엇이 포함되어 있습니까?

VMX 파일에는 가상 머신(VM)에 대한 다양한 구성 설정이 포함되어 있습니다. VMX 파일에서 일반적으로 발견되는 설정 중 일부는 다음과 같습니다.

- `.encoding:` 파일에 사용되는 문자 인코딩을 지정합니다.
- `config.version:` VMX 파일 형식의 버전을 나타냅니다.
- `virtualHW.version:` VM의 가상 하드웨어 버전을 지정합니다.
- `guestOS:` VM에 설치된 게스트 운영 체제를 지정합니다.
- `memSize:` VM에 할당된 메모리 양을 정의합니다.
- `displayName:` VM의 표시 이름 또는 레이블을 설정합니다.
- `powerType:` 다양한 작업(전원 끄기, 전원 켜기, 재설정, 일시 중지)에 대한 전원 동작을 정의합니다.
- `floppyX:` 존재 여부, 파일 매핑 등 플로피 드라이브와 관련된 구성 설정입니다.
- `numvcpus:` VM에 할당된 가상 CPU 수를 지정합니다.
- `scsiX:` SCSI 컨트롤러 및 관련 가상 디스크에 대한 구성 설정입니다.
- `ethernetX:` 가상 장치 유형, 네트워크 이름 및 주소 유형을 포함한 네트워크 어댑터에 대한 구성 설정입니다.
- `ideX:` IDE 컨트롤러 및 관련 가상 디스크에 대한 구성 설정입니다.
- `usbX:` 존재 여부 및 연결 세부정보와 같은 USB 장치에 대한 구성 설정입니다.
- `sound:` 가상 사운드 어댑터에 대한 구성 설정입니다.
- `tools.syncTime:` 호스트 시스템과의 시간 동기화가 활성화되어 있는지 여부를 나타냅니다.
- `uuid.bios:` VM의 BIOS UUID를 지정합니다.
- `uuid.location:` VM의 위치 UUID를 지정합니다.

## VMX 파일을 여는 방법?

VMX 파일을 수동으로 여는 것은 권장되지 않습니다. VMware Fusion을 사용하여 가상 머신을 실행하면 소프트웨어가 자동으로 VMX 파일의 정보를 로드합니다.

그러나 VMX 파일을 수동으로 편집하려면 메모장(Windows) 또는 TextEdit(Mac)과 같은 텍스트 편집기를 사용하여 편집할 수 있습니다.

## VMX 파일의 형식은 무엇입니까?

VMX 파일은 특정 형식의 일반 텍스트 파일입니다. 형식은 각 줄이 별도의 구성 옵션을 나타내는 키-값 쌍 구조를 따릅니다.

VMX 파일의 일반적인 형식은 다음과 같습니다.

```
key1 = value1
key2 = value2
key3 = value3
```

각 줄은 키, 등호(=) 및 해당 값으로 구성됩니다. 키는 특정 구성 설정을 나타내고 값은 해당 설정에 할당된 값을 나타냅니다.

예를 들어 VMX 파일의 `memSize = "8192"`는 가상 머신 메모리 제한이 8192MB RAM임을 지정합니다.

VMX 파일 형식에는 줄 시작 부분에 파운드 기호(#)로 표시되는 주석이 포함될 수도 있습니다. 이 주석은 파일을 구문 분석할 때 VMware 소프트웨어에서 무시됩니다. 설명은 특정 설정에 대한 추가 정보나 설명을 제공하는 데 자주 사용됩니다.

## 참고자료
* [샘플 VMX 파일](https://www.vmware.com/pdf/vsp_4_vmdirectpath_host.pdf)




