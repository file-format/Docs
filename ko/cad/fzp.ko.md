{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"FZP 파일 형식과 FZP 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"FZP 파일 형식 - Fritzing XML 부품 설명 파일",
  "linktitle" : "FZP",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2022-06-20"
}

## .FZP 파일이란?

FZP 파일은 [Fritzing](https://fritzing.org/) 전자 회로 프로토타이핑 및 설계 응용 프로그램에서 만든 XML 파일입니다. 여기에는 [XML](/ko/web/xml/) 파일 형식의 부품 속성, 커넥터 및 버스에 대한 정보가 포함됩니다. FPZ 파일은 Fritzing에서 독립적으로 사용할 수 없습니다. 대신 FZPZ 아카이브 파일의 일부로 가져옵니다.

## FZP 파일 형식 - 추가 정보

FZP 파일은 부품의 속성, 커넥터 및 버스에 대한 정보가 포함된 XML 파일입니다. 이 외에도 FZP 파일에는 FZP 파일의 제목, 설명, 작성자 및 게시 날짜에 대한 정보도 포함되어 있습니다. Fritzing 부품 파일을 내보낼 때 Fritzing 앱은 FZP 파일과 4개의 [SVG](/ko/page-description-language/svg/) 파일을 포함하는 [FZPZ](/ko/compression/fzpz/) 압축 아카이브를 생성합니다.

[FZP 파일 형식 사양](https://github.com/fritzing/fzp/blob/master/docs/README.md)은 Fritzing의 Github에서 확인할 수 있습니다.

## FZP 파일 구조 예

일반적인 FZP 파일은 다음과 같은 XML 구조를 갖는다.

```
<?xml version="1.0" encoding="UTF-8"?>
<module fritzingVersion="x.y.z" moduleId="mod-id-rev" referenceFile="ref.file">
  <version>x.y.z</version>
  <title>part-name</title>
  <description>some words about the part</description>
  <author>your-name</author>
  <date>yyyy-mm-dd</date>
  <url>http://part.org</url>
  <label>IC</label>
  <tags>...</tags>
  <taxonomy>...</taxonomy>
  <language>...</language>
  <family>...</family>
  <variant>...</variant>
  <properties>...</properties>
  <views>...</views>
  <connectors>...</connectors>
  <buses>...</buses>
</module>
```
## 참고문헌

* [FZP 파일 형식 사양](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [fzpz 확장자가 있는 새로운 부분](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

