{
  "date" : "2021-07-20",
  "keywords" :["MJS", "파일", "확장자", "파일 형식", "파일 확장자", "Node.js ES 모듈 파일"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MJS - Node.js ES 모듈 자바스크립트 파일",
  "description" :"MJS 파일이란 무엇이며 MJS 파일을 생성하고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "MJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-20"
}

## .MJS 파일이란?

확장자가 .mjs인 파일은 Node.js 애플리케이션에서 ECMA 모듈(ECMAScript Module)로 사용되는 JavaScript 소스 코드 파일입니다. Node.js의 natvie 모듈 시스템은 [JS](/ko/web/js/) 코드를 구성하기 위해 코드를 여러 파일로 분할하는 데 사용되는 CommonJS입니다. MJS는 모듈이 CommonJS인지 ES6인지 식별하기 위해 Node.js에서 사용하는 유일한 방법입니다. ECMAScript 모듈은 재사용을 위해 JavaScript 코드를 패키징하기 위한 표준 형식입니다. MJS 파일은 Atom, Vim, Apple xCode, Microsoft Visual Studio 및 메모장과 같은 텍스트 편집기에서 열 수 있습니다.

## MJS 파일 형식 - 추가 정보

MJS 파일은 JavaScript 구문의 일반 텍스트 형식으로 디스크에 저장됩니다. 이들은 모든 텍스트 편집기에서 열 수 있으며 사람이 읽을 수 있습니다. 2018년부터 거의 모든 주요 브라우저가 이제 ES 모듈을 지원합니다.

## ES 모듈과 CommonJS의 차이점

그렇다면 MJS 파일이 일반 JS 파일과 다른 점은 무엇입니까? ES 모듈과 CommonJS의 차이점은 다음과 같이 요약할 수 있습니다.

* 필요 없음, 내보내기 또는 module.exports
* \__filename 또는 \__dirname 없음
* JSON 모듈 로드 없음
* 기본 모듈 로드 없음
* require.resolve 없음
* NODE_PATH 없음
* require.extensions 없음
* require.cache 없음

## 참고문헌

* [Node.js ESM](https://nodejs.org/docs/latest/api/esm.html)
* [JS와 MJS의 차이점](https://nodejs.org/docs/latest/api/esm.html#esm_differences_between_es_modules_and_commonjs)

