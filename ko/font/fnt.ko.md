{
  "date" : "2020-08-20",
  "keywords" :[ "fnt 파일", "fnt 파일 형식", "fnt 파일이란", "파일", "fnt 예", "fnt 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FNT - Windows 글꼴 파일",
  "description":"FNT 파일 형식과 FNT 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "FNT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## .FNT 파일이란?

확장자가 .fnt인 파일은 Windows 운영 체제에서 일반 글꼴 정보를 저장하는 글꼴 파일입니다. FNT 파일은 대부분 TrueType(.TTF) 및 OpenType(.OTF) 파일 형식으로 대체되었으며 현재는 사용되지 않는 글꼴 파일 형식입니다. 이러한 파일은 단일 평가자 또는 벡터 글꼴을 저장할 수 있습니다. 모든 장치 드라이버는 Windows 2.x 글꼴을 지원합니다. 그러나 모든 장치 드라이버가
Windows 3.0 버전을 지원합니다.

## FNT 파일 형식

FNT 파일은 단일 래스터 또는 벡터 글꼴을 저장할 수 있습니다. 벡터 형식은 각 헌장의 글리프가 작은 비트맵을 사용하여 정의되는 래스터에 비해 GDI에서 더 자주 사용됩니다. .fnt를 .ttf 및 .otf로 대체한 명백한 이유는 래스터 형식 때문입니다.

### 글꼴 파일 헤더
래스터 및 벡터 글꼴 파일의 시작은 공통적이며 각 파일 유형에 대해 다른 정보가 뒤따릅니다. Windows 3.0용 글꼴 파일 헤더에는 다음과 같은 6개의 새 필드가 포함되어 있으며, 이 필드는 이후 버전의 Windows와의 호환성을 보장하기 위해 0으로 설정됩니다.

* dFlags
* dfAspace
* dfBspace
* dfC스페이스
* df컬러포인터
* df예약1

Windows 3.0 및 2.0용 헤더에 대한 자세한 내용은 [Microsoft 기술 자료 아카이브](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)를 참조하십시오.

## 참고문헌
* [글꼴 파일 형식](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)
* [Windows에서 글꼴을 설치하거나 제거하는 방법](https://support.microsoft.com/en-us/windows/how-to-install-or-remove-a-font-in-windows-f12d0657-2fc8-7613-c76f-88d043b334b8)

