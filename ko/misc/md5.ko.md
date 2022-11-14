{
  "date" : "2021-07-29",
  "keywords" :[ "md5 파일", "md5 파일 형식", "md5 파일이란", "파일", "md5 예제", "md5 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MD5 - MD5 체크섬 파일",
  "description":"MD5 파일을 만들고 열 수 있는 MD5 파일과 API에 대해 알아보세요.",
  "linktitle" : "MD5",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2021-07-29"
}

## .MD5 파일이란?

MD5 파일은 파일의 무결성을 확인하는 데 사용되는 체크섬 파일입니다. 연결된 파일의 지문과 유사하며 파일의 비트 수를 사용하는 알고리즘을 사용하여 고유하게 생성됩니다. [md5sum](http://www.gnu.org/software/coreutils/manual/html_node/md5sum-invocation.html)과 같은 소프트웨어로 파일을 검증하는데 사용됩니다. MD5 파일을 사용할 때의 한 가지 이점은 다운로드한 파일이 손상되지 않았는지 확인하는 것입니다.

## MD5 파일 형식 - 추가 정보

일반적으로 MD5 파일은 원래 파일 이름과 동일한 이름으로 저장되지만 확장자는 .md5입니다. 예를 들어 연결된 파일 이름이 'abc_987_123456.grb'인 경우 해당 MD5 파일 이름은 'abc_987_123456.grb.md5'가 됩니다. MD5 파일은 수신 또는 다운로드한 파일이 손상되었거나 악성 콘텐츠의 영향을 받지 않았는지 식별하는 데 도움이 됩니다. 즉, MD5 파일은 파일의 완전성을 보장합니다.


## MD5 체크섬을 확인하는 방법?

다음과 같이 [md5sum](https://en.wikipedia.org/wiki/Md5sum) 도구를 사용하여 단일 파일에 대해 MD5를 확인/검증할 수 있습니다.

```
md5sum -c abc_987_123456.grb.md5
```

## 참고문헌

* [md5sum - 위키피디아](https://en.wikipedia.org/wiki/Md5sum)

