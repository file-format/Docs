{
  "date" : "2022-05-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OBML 파일 형식 - Opera Mini 저장된 웹페이지 파일",
  "description" :"OBML 파일이란 무엇이며 OBML 파일을 생성하고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "OBML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-05-19"
}

## .OBML 파일이란?

OBML(Opera Binary Markup Language) 파일은 Opera Mini 모바일 웹 브라우저에서 저장한 웹페이지의 오프라인 버전입니다. 오프라인 상태에서 특정 장치에 표시하기 위해 페이지의 모든 요소를 포함하는 [HTML](/ko/web/html/) 파일의 독립형 압축 버전입니다. OBML 파일 형식은 OBML15 및 OBML16이 널리 사용되는 여러 버전으로 업그레이드되었습니다. 고려해야 할 중요한 점은 각 Opera Mini 버전은 하나의 OBML 형식과만 호환된다는 것입니다. 따라서 Opera Mini를 업그레이드하면 이전에 저장된 페이지를 읽을 수 있습니다. OBML 파일은 HTML 및 [PDF](/ko/pdf/)로 변환할 수 있습니다.

## OBML 파일 형식

OBML 파일 형식은 Opera의 독점 파일 형식으로 저장되며 해당 파일 형식 사양은 공개적으로 사용할 수 없습니다. 그러나 [OMBL 형식](https://github.com/grawity/obml-parser/blob/master/obml.md)은 다음과 같이 구조를 디코딩하도록 리버스 엔지니어링되었습니다.

### OBML 데이터 유형

리버스 엔지니어링 결과에 따라 OBML은 다음과 같은 기본 유형을 사용합니다.

* `byte` – 부호 없는 정수(1바이트)
* `short` – 부호 있는 정수(2바이트, 빅엔디안)
* `medium` – 부호 있는 정수(3바이트, 빅 엔디안)
 * `blob` – { length: short, data: byte[length] }
* `char` – ASCII 문자를 포함하는 바이트
* `string` – UTF-8로 인코딩된 텍스트를 포함하는 blob

### OBML 헤더

```
header := {
	(if version >= 15) {
		fake_file_size: medium = 0x02d355
		fake_version: byte     = 16
	}
	file_size: medium
	version: byte
	page_size: coords
	(if version == 16) {
		unknown: byte[3]      // always S\x00\x00
	}
	unknown: short                // always -1
	page_title: string
	unknown: blob
	page_url_base: string
	page_url: url
	(if version >= 15) {
		unknown: byte[6]
	}
	(if 6 < version <= 13) {
		unknown: byte[5]
	}
	(if version == 6) {
		unknown: byte[1]
	}
	metadata: chunk[]
	content: chunk[]
}
```
## 참고문헌

* [OMBL 형식](https://github.com/grawity/obml-parser/blob/master/obml.md)

