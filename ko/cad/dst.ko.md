{
  "date" : "2022-01-04",
  "keywords" :[ ".dst", "파일", "형식", "확장자", "API", "AutoCAD 시트 세트" ],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DST - AutoCAD 시트 세트 파일",
  "description" :".dst 파일과 DST 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "DST",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2022-01-04"
}

## .DST 파일이란?

DST 파일은 시트 세트를 정의하기 위한 연관 및 정보가 포함된 AutoCAD 파일입니다. 이러한 파일은 기본 시트 세트 저장 폴더인 AutoCAD 시트 세트에 저장됩니다. DST 파일에는 실제 도면 레이아웃이 포함되어 있지 않지만 이러한 시트 세트와 연관된 선택된 [DWG](/ko/cad/dwg/) 및 [DWT](/ko/cad/dwt/) 파일에서 이를 참조합니다. 네트워크 환경에서 모든 팀 구성원은 이러한 관련 파일에 대한 네트워크 액세스 권한이 있어야 합니다. DST 파일은 [XML](/ko/web/xml/) 파일 형식으로 디스크에 저장됩니다.

## DST 파일 형식 - 추가 정보

DST 파일은 AutoDesk Sheet Set Manager(SSM) 도구로 생성됩니다. 팀의 누군가가 파일에 액세스하면 DST 파일이 잠시 열린 다음 업데이트된 정보와 함께 다시 저장됩니다. 동일한 DST 파일에 대한 동시 액세스는 파일이 액세스 중일 때 잠금 아이콘을 표시하는 SSM 도구에 의해 관리됩니다.

특정 시간에 시트 상태는 다음 상태 중 하나일 수 있습니다.

* 시트는 편집이 가능합니다.
* 시트가 잠겨 있습니다.
* 시트가 없거나 예상치 못한 폴더 위치에서 발견되었습니다.

## 참고문헌

* [DST 시트 세트 사용 정보](https://help.autodesk.com/view/ACDLT/2017/ENU/?guid=GUID-577D8EA0-85F2-4829-B4F9-8CAD6F7AAACC)
* [시트 세트에 대해 알아보기](https://help.autodesk.com/view/ACDLT/2017/ENU/?guid=GUID-34D889BC-19AD-4CD1-ADB1-F359D9B515FB)
* [AutoCAD 시트 세트 마스터링](https://damassets.autodesk.net/content/dam/autodesk/www/cad-manager-center/articles/Mastering-AutoCAD-Sheet-Sets_Preview_EN.pdf)

