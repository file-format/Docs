{
  "date" : "2021-06-29",
  "keywords" :[ "CUR", "확장자", "파일", "형식", "이미지", "장치 독립 비트맵", "커서 파일 형식", "커서", "Windows", "응용 프로그램" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CUR - 커서 파일 형식",
  "description":"CUR 파일 형식과 CUR 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "CUR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-06-29"
}

## .CUR 파일이란? ##

CUR 파일은 정적 Microsoft Windows 커서 파일 형식입니다. 기본적으로 확장자를 제외한 모든 면에서 ICO(아이콘) 파일과 동일한 정지 이미지입니다. CUR 및 [ICO](/ko/image/ico/)는 모두 Device-Independent Bitmap [DIB](/ko/image/dib/)(Device-Independent Bitmap) 사양을 기반으로 설정됩니다. 기본 및 Windows 운영 체제용 Windows 마우스 포인터와 같은 사용자 지정 커서는 CUR 파일에 저장됩니다. 일반적인 사용을 위한 화살표, 대기 시간을 나타내는 회전하는 모래시계 또는 텍스트 편집을 위한 I-바일 수 있습니다. CUR 파일은 Windows 커서가 사용자 정의 데스크탑 테마와 일치하도록 사용자 정의 데스크탑 테마의 설치 팩과 함께 제공됩니다.

## 기술 사양 ##

CUR 파일은 Microsoft Windows 운영 체제에서 작동하는 장치에서 찾을 수 있는 이진 시스템 파일입니다. CUR 포인터 이미지는 16×16, 32×32 등과 같은 다양한 표준 크기로 제공됩니다. CUR 파일은 ICO 파일과 매우 유사합니다. 둘 다 작은 정지 이미지로 구성됩니다. CUR과 ICO 파일의 확장자만 다릅니다. 또한 CUR 파일의 헤더에 있는 핫스팟에 대한 설명은 ICO 파일과 다릅니다. 핫스팟은 왼쪽 상단 모서리에서 마우스를 가리키는 위치까지의 픽셀 오프셋을 해석합니다. Windows 시스템은 여전히 CUR 파일을 사용하고 있지만 이제 애니메이션 커서는 일반적으로 CUR 대신 ANI 파일 확장자를 가집니다.

## 간략한 역사 ##

CUR 파일은 ICO 파일에서 만들어집니다. 최초의 CUR 파일 형식은 상업적 사용을 원활하게 하기 위해 1981년 Microsoft의 Windows 1.0 운영 체제에 통합되었습니다. 곧 더 많은 대화형 커서가 도입되어 사용자가 사용 가능한 사전 설치된 옵션에서 커서 기본 설정을 수정할 수 있습니다. 하지만, 기술적인 지식이 부족하더라도 스스로 CUR 파일을 편집하는 것은 쉽습니다.


## CUR 예 ##

CUR 파일은 *C:\Windows\Cursors*에서 찾을 수 있습니다.

{{< figure src="../cur.png" alt="CUR 파일 형식" >}}

