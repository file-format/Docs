{
  "date" : "2021-08-10",
  "keywords" :[ ".ova 파일", "파일 형식", ".ova 파일이란", "파일", "파일 확장자"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :".ova 파일 형식이 무엇이며 ova 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"OVA 파일 형식 - 가상 어플라이언스 파일 열기",
  "linktitle" : "OVA",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## .OVA 파일이란?

OVA(Open Virtual Appliance) 파일은 .tar 아카이브 형식을 사용하여 아카이브로 저장된 OVF 디렉토리입니다. 가상 머신에서 실행되는 소프트웨어 배포용 파일이 포함된 가상 어플라이언스 패키지 파일입니다. OVA 패키지에는 다른 관련 파일과 함께 [.ovf](/ko/disc-and-media/ovf/) 설명자 파일, 인증서 파일, 선택적 [.mf](/ko/programming/mf/) 파일이 포함되어 있습니다. OVA 파일의 미디어 유형은 application/ovf입니다.

## OVA 파일 형식

언급했듯이 OVA 파일은 TAR 파일 형식의 OVF 디렉토리를 사용하여 생성되는 아카이브 파일입니다. 파일 자체는 바이너리 파일로 저장됩니다. VMware, Microsoft, Oracle, Citrix와 같은 대부분의 가상화 플랫폼은 가상 머신에 로드할 이미지의 세부 정보가 포함된 디스크립터 파일인 OVF 파일에서 가상 어플라이언스를 설치할 수 있습니다.

## OVA 파일의 장점

* OVA 파일은 압축되어 있어 더 빠른 다운로드가 가능합니다.
* vSphere Client는 가져오기 전에 OVA 파일의 유효성을 검사하고 의도한 대상 서버와 호환되는지 확인합니다. 어플라이언스가 선택한 호스트와 호환되지 않는 경우 가져올 수 없으며 오류 메시지가 나타납니다.
* OVA는 다중 계층 애플리케이션과 둘 이상의 가상 머신을 캡슐화할 수 있습니다.

## 참고문헌

* [OVA 파일 형식 및 템플릿](https://docs.vmware.com/en/VMware-vSphere/7.0/com.vmware.vsphere.vm_admin.doc/GUID-AE61948B-C2EE-436E-BAFB-3C7209088552.html )
* [OVF 파일 형식 사양](https://products.conholdate.app/viewer/view/3XKCLQbwAw/open-virtualization-format-specification-dsp0243_1-1-0.pdf)

