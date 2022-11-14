{
  "date" : "2022-03-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSO - Microsoft Office 매크로 참조 파일",
  "description":"MSO 파일을 만들고 열 수 있는 MSO 파일 및 API에 대해 알아보세요.",
  "linktitle" : "MSO",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-03-12"
}

## .MSO 파일이란?

MSO 파일은 Microsoft Outlook을 사용하여 HTML 메시지를 보낼 때 생성되는 데이터 컨테이너 파일 형식입니다. 이것은 주로 Microsoft Office 2000 응용 프로그램에서 발생합니다. 대부분의 경우 이메일 메시지는 **Oledata.mso** 파일이라는 이름으로 첨부됩니다. 이메일 수신자는 그러한 이메일을 열 때 동일한 소프트웨어가 설치되어 있지 않아도 파일을 올바르게 볼 수 있습니다. MSO 파일은 [Microsoft 복합 문서 파일 형식(MCDF)](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b)을 참조하십시오.

## Microsoft MSO 파일 형식

MSO 파일은 OLE(Object Linking and Embedding) 또는 COM(구성 요소 개체 모델) 구조화된 저장소 복합 파일 구현 이진 파일 형식이라고도 하는 MCDF(Microsoft 복합 문서 파일 형식)로 저장됩니다.

### MSO 파일 형식 구조

MSO 파일 형식의 내부 파일 형식 구조는 [구조](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/28488197-8193-49d7-84d8-dfd692418ccd)에 잘 정의되어 있습니다. ) MCDF 문서의 섹션. 파일 할당 테이블(FAT)은 섹터 할당 및 섹터 체인을 관리합니다. 여기에는 32비트 섹터 번호의 배열이 포함됩니다. 배열의 각 인덱스는 섹터 번호를 나타내는 반면 해당 값은 체인의 다음 섹터 또는 특수 값을 나타냅니다.

## 참고문헌

* [COM 구조화된 저장소](https://en.wikipedia.org/wiki/COM_Structured_Storage)
* [Microsoft 복합 문서 파일 형식(MCDF)](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b)

