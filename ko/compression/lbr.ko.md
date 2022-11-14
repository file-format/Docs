{
  "date" : "2021-04-08",
  "keywords" :[ "mst 파일", "mst 파일 형식", "mst 파일이란", "파일", "mst 예", "mst 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
	

},
  "draft" : "false",
  "toc" : true,
  "title" :"LBR - LU 라이브러리 아카이브 파일 형식",
  "description":"LBR 파일을 만들고 열 수 있는 LBR 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "LBR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## .LBR 파일이란?

확장자가 .lbr인 파일은 LU 프로그램으로 생성된 아카이브 파일로 1980년대에 CP/M 및 DOS 운영 체제에서 사용되었습니다. 더 이상 사용되지 않으며 최신 보관 파일 형식으로 대체되었습니다. 이 형식은 멤버 파일을 압축하지 않으며 이러한 파일에 대한 컨테이너 아카이브 역할을 합니다. 보관 기능은 주로 인터넷을 통해 보관된 파일을 전송하는 데 사용되었습니다. LBR은 압축을 제공하지 않았기 때문에 SQ 또는 CRUNCH와 같은 다른 유틸리티를 사용하여 멤버 파일을 사전 아카이브하거나 아카이브 파일을 사후 아카이브하여 압축하여 크기를 줄였습니다.

## LBR 파일 형식

LBR 파일 형식은 Gary P. Novosielski가 설계했으며 공개적으로 사용할 수 있는 기술 세부 정보가 없습니다. LBR 파일은 0x00 바이트로 시작하여 11개의 공백(0x20), 2개의 0x00 바이트, 그리고 둘 다 0x00이 아닌 2개의 바이트가 따라옵니다. 컨테이너 파일 형식이므로 LU.COM 및 NULU.COM을 사용하여 추출할 수 있습니다.

## 참고문헌

* [LBR - 위키백과](https://en.wikipedia.org/wiki/LBR_(file_format))

