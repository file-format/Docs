{
  "date" : "2022-03-21",
  "keywords" :[ "xpr 파일", "xpr 파일 형식", "xpr 파일이란", "파일", "xpr 예제", "xpr 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPR 파일 형식 - Microsoft 표현 디자인 그래픽 파일",
  "description":"XPR 파일을 만들고 열 수 있는 XPR 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "XPR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-21"
}

## .XPR 파일이란?

XPR 파일은 현재 단종된 Microsoft EGD(Expression Graphics) 소프트웨어로 만든 벡터 이미지 파일입니다. 사용자 인터페이스 목업으로 사용할 수 있는 그래픽 정보가 포함되어 있습니다. XPR 파일은 나중에 Microsoft Expression Design에서 .design 파일로 대체되었습니다. XPR 파일은 지금 꽤 오랫동안 중단된 Microsoft Expression Studio로 열 수 있습니다.

## XPR 파일 형식 취약점

XPR 파일은 Microsoft Expression Design의 취약점을 이용하여 원격 코드 실행을 허용하는 것으로 확인되었습니다. 보고된 문제에서 사용자가 DLL(동적 연결 라이브러리) 파일과 함께 네트워크 디렉터리에 있는 합법적인 .xpr 파일을 열면 Microsoft Expression Design에서 DLL 파일을 로드하고 포함된 코드를 실행할 수 있습니다. 이것은 나중에 보안 업데이트에서 Microsoft에 의해 수정되었습니다.

## 참고문헌

* [표현식 디자인의 취약점으로 인한 원격 코드 실행 문제점(2651018)](https://learn.microsoft.com/en-us/security-updates/securitybulletins/2012/ms12-022)

