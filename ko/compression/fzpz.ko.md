{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FZPZ 파일 형식 - Fritzing 부품 파일",
  "description":"FZPZ 파일이 무엇이며 FZPZ 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "FZPZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-20"
}

## .FZPZ 파일이란?

FZPZ 파일은 회로 프로토타이핑 및 설계 응용 프로그램 **Fritzing**으로 만든 전자 회로 설계에 사용되는 구성 요소/부품입니다. [FZP](/ko/cad/fzp/) 파일과 Fritzing의 전체 부분을 설명하는 4개의 [SVG](/ko/page-description-language/svg/) 이미지가 포함된 압축 아카이브입니다. 이러한 파일을 사용하는 이점은 사용자가 재사용성 관점에서 FZPZ 파일을 공유할 수 있다는 것입니다. FZPZ 부품을 공유하면 회로 부품을 통합하여 더 큰 PCB 설계를 빠르게 생성하는 데 도움이 됩니다.

## FZPZ 파일 형식 - 추가 정보

FZPZ 파일은 압축된 [ZIP](/ko/compression/zip/) 아카이브로 디스크에 저장됩니다. 확장자의 이름을 .fzpz에서 .zip으로 바꾸고 WinZIP과 같은 표준 압축 해제 유틸리티를 사용하여 아카이브에서 파일을 추출할 수 있습니다.

### FZPZ 파일 구조 정보

언급했듯이 FZPZ 파일은 인쇄 회로 기판에 사용되는 부품을 표현하기 위한 여러 파일을 포함하는 아카이브 파일입니다. FZPZ에는 다음 파일이 포함되어 있습니다.

* `4개의 SVG 파일` - 부품의 브레드보드, 회로도, PCB 및 아이콘 이미지를 나타냅니다.
* `FZP 파일` - 부품의 속성, 커넥터 및 버스에 대한 정보가 포함된 XML 파일

파일 이름은 일반적으로 다음과 같습니다.

* part.file.fzp
* svg.breadboard.file.svg
* svg.icon.file.svg
* svg.pbc.file.svg
* svg.schematic.file.svg

## 참조 ##

* [fzpz 확장자가 있는 새로운 부분](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

