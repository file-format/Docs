{
  "date" : "2021-07-28",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QBL - QuickBooks 라이센스 파일",
  "description":"QBL 파일 형식과 QBL 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "QBL",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-07-28"
}

## .QBL 파일이란?

확장자가 .qbl인 파일은 사용자가 구매한 사본에 대한 라이선스 정보가 포함된 QuickBooks 라이선스 파일입니다. 일반적으로 QuickBooks가 설치된 후 'license.qbl'이라는 이름으로 로컬 시스템에 저장되며 소프트웨어를 처음 실행할 때 사용자가 소프트웨어에 라이선스 정보를 입력합니다. QBL은 QuickBooks 라이선스 정보를 저장하는 데 사용된 이전 파일 형식이었습니다. 이것은 이제 QuickBooks `qbregisteration.dat` 파일로 대체되었으며 사용자의 확인 이메일, 구매한 DVD 또는 기타 구매 수단을 통한 정보로 채워집니다. QBL 파일은 Windows 메모장, Apple TextEdit, 메모장++, Github Atom 편집기 등과 같은 모든 텍스트 편집기에서 열 수 있습니다.

## QBL 파일 형식 - 추가 정보

QBL 파일은 일반 텍스트 파일로 생성 및 저장됩니다. 이러한 파일의 정보는 사람이 읽을 수 있으며 이러한 파일을 텍스트 편집기에서 열 때 편집/업데이트할 수 있습니다. 라이선스 및 사용자 등록 정보는 QuickBooks 소프트웨어 시작을 위해 이 파일에 복사할 수 있습니다. QBL 파일은 일반적으로 Windows 운영 체제의 Program Files\Intuit\QuickBooks\INET 디렉토리에 저장됩니다.

QBL 파일에는 두 가지 유형의 정보가 포함됩니다.

* `QuickBooks 버전 정보:` 설치된 QuickBooks 버전을 말하며 xx.x와 같은 형식입니다.
* `라이선스 키:` 000-000 0000-0000-0000-000 000073adbf3f 형식의 텍스트. 여기서 000-000 0000-0000-0000-000은 사용자의 qb등록 키로 대체됩니다.

## 참고문헌

* [인튜이트의 퀵북스](https://quickbooks.intuit.com/)
* [QuickBooks - qbregistration.dat 파일 생성](https://quickbooks.intuit.com/learn-support/en-us/license-information/create-or-re-create-the-qbregistration-dat-file/ 00/186082)

