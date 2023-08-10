{
  "date" : "2022-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"PYC 파일을 만들고 열 수 있는 PYC 파일 형식 및 API에 대해 알아보세요.",
  "title" :"PYC 파일 형식 - Python 컴파일된 파일",
  "linktitle" : "PYC",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-05-09"
}

## .PYC 파일이란?

PYC 파일은 Python 프로그래밍 언어로 작성된 소스 코드에서 생성된 컴파일된 출력 파일입니다. Python 인터프리터를 사용하여 PY 파일을 실행하면 실행을 위해 바이트 코드로 변환됩니다. 동시에 컴파일된 바이트코드도 .pyc 파일로 저장되어 해당되는 경우 나중에 캐시에서 재사용할 수 있습니다.

## PYC 파일 형식의 구조

PYC 파일은 바이트 코드이며 파일 형식 사양은 공개적으로 사용할 수 없습니다. 그러나 일부 출처의 조사에 따르면 [PYC 파일의 구조](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html)는 다음으로 구성됩니다.

* `4바이트 매직 넘버` - 마샬링 코드가 변경될 때마다 변경되는 2바이트와 0d0a의 2바이트.
* `4바이트 수정 타임스탬프` - .pyc를 생성한 소스 파일의 Unix 수정 타임스탬프로, 소스가 변경되면 다시 컴파일할 수 있습니다.
* '마샬링된 코드 개체' - 소스 파일을 컴파일한 결과인 코드 개체의 marshal.dump 출력.

## 참고문헌

* [.pyc 파일의 구조](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html)

