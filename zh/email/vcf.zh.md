{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCF - 虚拟联系人文件",
  "description":"了解 VCF 文件格式和可以创建和打开 VCF 文件的 API。",
  "linktitle" : "VCF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .vcf 文件？

VCF（虚拟卡格式）或 vCard 是一种用于存储联系人信息的数字文件格式。该格式广泛用于流行的信息交换应用程序之间的数据交换。大多数操作系统（如 Windows 和 MacOS）都带有用于创建和打开这些文件的默认应用程序。单个 VCF 文件可以包含一个或多个联系人的联系信息。 VCF 文件通常包含联系人姓名、地址、电话号码、电子邮件、生日、照片和音频等信息，以及许多其他字段。在电子邮件客户端和服务的支持下，通过使用 vCard 格式传输联系人时不会丢失数据。 VCF 文件格式的媒体类型是 text/vcard。

## VCF 文件格式

VCF 文件本质上是文本的，并且是人类可读的。这些可以在文本编辑器中打开，例如 Microsoft Windows 上的记事本和 MacOS 上的 TextEdit。但是，如果文件中有图像，它将不会显示在文本编辑器中。

[Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) 提供支持打开 VCF 文件以及转换为许多其他格式，例如流行的 [MSG](/zh/email/msg/) 格式。 VCF 文件格式随着从 2.1 版到 4.0 版的改进，为文件格式添加了详细信息。该格式还用于导出电话联系人，然后导入另一台设备。

{{< figure src="../VCF.png" alt="VCF 文件格式" >}}

### VCF 2.1 示例

以下是 2.1 版的示例。

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

### VCF 3.0 示例

以下是 3.0 版本的示例。

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

### VCF 4.0 示例

以下是 4.0 版本的示例。

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

## 参考

* [VCF - 维基百科](https://en.wikipedia.org/wiki/VCard)

