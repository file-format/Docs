{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCF - 가상 연락처 파일",
  "description":"VCF 파일 형식과 VCF 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "VCF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## .VCF 파일이란?

VCF(가상 카드 형식) 또는 vCard는 연락처 정보를 저장하기 위한 디지털 파일 형식입니다. 이 형식은 널리 사용되는 정보 교환 응용 프로그램 간의 데이터 교환에 널리 사용됩니다. Windows 및 MacOS와 같은 대부분의 운영 체제에는 이러한 파일을 만들고 여는 기본 응용 프로그램이 함께 제공됩니다. 단일 VCF 파일에는 하나 이상의 연락처에 대한 연락처 정보가 포함될 수 있습니다. VCF 파일에는 일반적으로 연락처 이름, 주소, 전화 번호, 이메일, 생일, 사진 및 오디오와 같은 정보와 기타 여러 필드가 포함됩니다. 이메일 클라이언트 및 서비스에서 지원되므로 vCard 형식을 사용하여 연락처를 전송하는 동안 데이터 손실이 없습니다. VCF 파일 형식의 미디어 유형은 text/vcard입니다.

## VCF 파일 형식

VCF 파일은 본질적으로 텍스트이며 사람이 읽을 수 있습니다. Microsoft Windows의 메모장 및 MacOS의 TextEdit와 같은 텍스트 편집기에서 열 수 있습니다. 그러나 파일에 이미지가 있으면 텍스트 편집기에 표시되지 않습니다.

[Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690)은 다음을 지원합니다. VCF 파일을 열 뿐만 아니라 널리 사용되는 [MSG](/ko/email/msg/) 형식과 같은 다른 여러 형식으로 변환합니다. 버전 2.1에서 4.0으로 시간이 지남에 따라 향상된 VCF 파일 형식은 파일 형식에 자세한 정보를 추가합니다. 이 형식은 전화 연락처를 내보내고 나중에 다른 장치로 가져올 때도 사용됩니다.

{{< figure src="../VCF.png" alt="VCF 파일 형식" >}}

### VCF 2.1 예제

다음은 버전 2.1의 예입니다.

```
BEGIN:VCARD
VERSION:2.1
N:Gump;Forrest;;Mr.
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;WORK;VOICE:(111) 555-1212
TEL;HOME;VOICE:(404) 555-1212
ADR;WORK;PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;WORK;PREF;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:100 Waters Edge#0D#
 #0ABaytown\, LA 30314#0D#0AUnited States of America
ADR;HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;HOME;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:42 Plantation St.#0D#0A#
 Baytown, LA 30314#0D#0AUnited States of America
EMAIL:forrestgump@example.com
REV:20080424T195243Z
END:VCARD
```

### VCF 3.0 예제

다음은 버전 3.0의 예입니다.

```
BEGIN:VCARD
VERSION:3.0
N:Gump;Forrest;;Mr.;
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;VALUE#URI;TYPE#GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;TYPE#WORK,VOICE:(111) 555-1212
TEL;TYPE#HOME,VOICE:(404) 555-1212
ADR;TYPE#WORK,PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;TYPE#WORK,PREF:100 Waters Edge\nBaytown\, LA 30314\nUnited States of America
ADR;TYPE#HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;TYPE#HOME:42 Plantation St.\nBaytown\, LA 30314\nUnited States of America
EMAIL:forrestgump@example.com
REV:2008-04-24T19:52:43Z
END:VCARD
```

### VCF 4.0 예제

다음은 버전 4.0의 예입니다.

```
BEGIN:VCARD
VERSION:4.0
N:Gump;Forrest;;Mr.;
FN:Sheri Nom
ORG:Sheri Nom Co.
TITLE:Ultimate Warrior
PHOTO;MEDIATYPE#image/gif:http://www.sherinnom.com/dir_photos/my_photo.gif
TEL;TYPE#work,voice;VALUE#uri:tel:+1-111-555-1212
TEL;TYPE#home,voice;VALUE#uri:tel:+1-404-555-1212
ADR;TYPE#WORK;PREF#1;LABEL#"Normality\nBaytown\, LA 50514\nUnited States of America":;;100 Waters Edge;Baytown;LA;50514;United States of America
ADR;TYPE#HOME;LABEL#"42 Plantation St.\nBaytown\, LA 30314\nUnited States of America":;;42 Plantation St.;Baytown;LA;30314;United States of America
EMAIL:sherinnom@example.com
REV:20080424T195243Z
x-qq:21588891
END:VCARD
```

## 참고문헌

* [VCF - 위키피디아 작성](https://en.wikipedia.org/wiki/VCard)

