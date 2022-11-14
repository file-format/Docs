{
  "date" : "2021-03-18",
  "author" : {
    "display_name" : "Muhammad Umar",
	"keywords" :[ "QGD", "QGIS 프로젝트의 Sqlite 데이터베이스", "확장자", "형식", "QGIS", "보조 데이터베이스", "QGD 파일이란"]
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGD - QGIS 프로젝트의 Sqlite 데이터베이스",
  "description":"QGIS 프로젝트의 sqlite 데이터베이스인 QGD와 QGD 파일을 생성하고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "QGD",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## .QGD 파일이란?

확장자가 .QGD 파일인 파일은 실제로 프로젝트의 보조 데이터를 수용하는 **QGIS** 프로젝트의 관련 sqlite 데이터베이스입니다. 프로젝트에 대한 보조 데이터가 없는 경우 QGD 파일은 비어 있는 상태로 유지됩니다.

## QGD 파일 형식에 대한 세부 정보

클래식 모드에서 보조 데이터베이스는 xml 파일과 함께 확장자가 .qgd인 파일로 저장됩니다. **보조 데이터베이스** 시스템을 사용하면 대체 방법으로 시스템의 데이터를 읽고 쓸 수 있습니다. 압축된 컨테이너인 QGZ를 만들 때 .qgd 파일은 .qgz에 포함됩니다.

## 보조 데이터베이스란 무엇입니까?
보조 데이터베이스는 실제로 대상 데이터베이스의 복제에 대한 응답으로 생성되는 대기 db 시스템입니다. 보조 데이터베이스는 실제로 복제 데이터베이스가 복제 대상 데이터베이스인 경우입니다. 예를 들어 중복 데이터베이스를 사용하여 대기 데이터베이스를 설정하는 경우 소스 데이터베이스가 대상이 되고 대기 데이터베이스가 보조 데이터베이스로 알려집니다.


## 참고문헌

* [QGZ – QGIS의 새로운 기본 프로젝트 파일 형식](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [QGIS 파일 형식](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

