{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCF - 仮想連絡先ファイル",
  "description":"VCF ファイル形式と,VCF ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "VCF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## .VCF オプション番号

VCF (Virtual Card Format) または vCard は、連絡先情報を保存するためのデジタル ファイル形式です。この形式は、一般的な情報交換アプリケーション間のデータ交換に広く使用されています。 Windows や MacOS などのほとんどのオペレーティング システムには、これらのファイルを作成して開くための既定のアプリケーションが付属しています。 1 つの VCF ファイルには、1 つまたは複数の連絡先の連絡先情報を含めることができます。通常、VCF ファイルには、連絡先の名前、住所、電話番号、電子メール、誕生日、写真、音声などの情報に加えて、他の多くのフィールドが含まれています。メール クライアントとサービスでサポートされているため、vCard 形式を使用して連絡先を転送する際にデータが失われることはありません。 VCF ファイル形式のメディア タイプは text/vcard です。

## VCF ファイル形式

VCF ファイルは本質的にテキストであり、人間が判読できます。これらは、Microsoft Windows のメモ帳や MacOS の TextEdit などのテキスト エディターで開くことができます。ただし、ファイルに画像がある場合、テキスト エディターには表示されません。

[Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) は、 VCF ファイルを開くだけでなく、一般的な [MSG](/email/msg/) 形式など、他の多くの形式に変換することもできます。 VCF ファイル形式は、バージョン 2.1 から 4.0 までの時間とともに強化され、ファイル形式に詳細な情報が追加されました。この形式は、電話の連絡先をエクスポートし、後で別のデバイスにインポートするためにも使用されます。

{{< figure src="../VCF.png" alt="VCF ファイル形式" >}}

### VCF 2.1 の例

以下は、バージョン 2.1 の例です。

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

### VCF 3.0 の例

以下は、バージョン 3.0 の例です。

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

### VCF 4.0 の例

以下は、バージョン 4.0 の例です。

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

## 参考文献

* [VCF - ウィキペディアによる](https://en.wikipedia.org/wiki/VCard)

