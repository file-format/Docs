{
  "date": "2019-12-03",
  "keywords": [
"DOCX",
"fayl",
"format",
"fayl növü",
"uzadılması",
"DOCX faylı nədir?"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DOCX",
  "description": "DOCX faylları yarada və aça bilən DOCX fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "DOCX",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-doc-azx"
}
},
  "lastmod": "2019-12-03"
}

## DOCX faylı nədir? ##

DOCX Microsoft Word sənədləri üçün tanınmış formatdır. 2007-ci ildən Microsoft Office 2007-nin buraxılışı ilə təqdim edilən bu yeni Sənəd formatının strukturu sadə binardan XML və ikili faylların birləşməsinə dəyişdirildi. Docx faylları Word 2007 və yan versiyaları ilə açıla bilər, lakin DOC fayl uzantılarını dəstəkləyən MS Word-ün əvvəlki versiyaları ilə deyil.

## Qısa tarix ##

After Microsoft opened the specifications for the DOC file format, it was easy for its competitors to reverse engineer the format and provide the same support in their own applications. In addition, the competition from Open Office in the form of its Open Document Format, compelled Microsoft to adopt more open and wide standards. It was in early 2000 when Microsoft decided to go for the change to accommodate the standard for **Office Open XML**. Documents under this new Standard were given [.docx extension](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd), the "X" being for XML. By 2007, this new file format became part of Office 2007 and is carried on in the new versions of Microsoft Office as well. The new file type has added advantages of small file sizes, fewer changes of corruption and well-formatted images representation.

## DOCX Fayl Formatının Xüsusiyyətləri - Ətraflı Məlumat

Docx faylı ZIP arxivində olan XML faylları toplusundan ibarətdir. Yeni Word sənədinin məzmununa onun məzmununu açmaqla baxmaq olar. Kolleksiya aşağıdakı kimi təsnif edilən XML fayllarının siyahısını ehtiva edir:

* MetaData Faylları - arxivdə mövcud olan digər fayllar haqqında məlumatları ehtiva edir

* Sənəd - sənədin faktiki məzmununu ehtiva edir


### Metadata Faylları ###

Microsoft Word bu faylları fayllar arasında əlaqəni tapmaq və sənədin məzmununu tapmaq üçün istifadə edir. Word sənəd arxivi çıxarıldıqda, aşağıda ətraflı təsvir olunan bir sıra faylları ehtiva edir.

#### Əlaqələr - \_rels/.rels ####

Bu fayl MS Word-ə sənədin məzmununu və digər istinadları harada axtarmaq lazım olduğunu bildirən məlumatları ehtiva edir. Hər bir əlaqə unikal əlaqə id ilə müəyyən edilir və istinad edilən XML faylını hədəf kimi təyin edir. Nümunə əlaqə faylı aşağıdakı kimi göstərilir:

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"word/document.xml"/>.
```

#### Məzmun növləri ####

Sənəddə şəkillər, mövzular, söz sənəti və s. kimi bir neçə media növü ola bilər. [Content_Types].xml sənəddə mövcud olan media növləri haqqında məlumatı ehtiva edir. Belə bir XML faylının məzmunu aşağıdakı kimi göstərilir:

```
<Override PartName#"/word/document.xml" ContentType#"application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/>
```

#### Resurslara İstinadlar - \_rels/document.xml.rels ####

Sənədə daxil edilmiş şəkillər kimi resurslar haqqında məlumat bu XML faylında istinad edilir.

#### Əsas Sənədin Məzmunu ####

Bu, sənədin mətn məzmununu ehtiva edən arxivin əsas XML faylına aiddir. Bu məzmun OpenOffice XML spesifikasiyalarına uyğun olaraq müxtəlif qovşaqlarla təmsil olunur. Əsasən bu faylın məzmunu Paraqraflar və Cədvəllərdən ibarətdir, lakin onlar digər qovşaqlar da ola bilər.

### Fayl Format Düyünləri ###

Əsas document.xml faylı faylın ümumi məzmununu təqdim etmək üçün qovşaqlar toplusudur. Hər bir qovşağın ya sonrakı qovşaqları, ya da məzmunu əhatə edən başlanğıcı və sonu var. Belə bir xml faylının sadələşdirilmiş nümunəsi aşağıdakı kimidir:

```
<w:document>
   <w:body>
       <w:p w:rsidR#"005F670F" w:rsidRDefault#"005F79F5">
           <w:r><w:t>Example Document</w:t></w:r>
       </w:p>
       <w:sectPr w:rsidR#"005F670F">
           <w:pgSz w:w#"12240" w:h#"15840"/>
           <w:pgMar w:top#"1440" w:right#"1440" w:bottom#"1440" w:left#"1440" w:header#"720" w:footer#"720"
                    w:gutter#"0"/>
           <w:cols w:space#"720"/>
           <w:docGrid w:linePitch#"360"/>
       </w:sectPr>
   </w:body>
</w:document>
```

Aşağıda məzmunun təsviri üçün DOCX faylında olan bəzi qovşaqlar haqqında məlumat verilmişdir.

`<w:document> ` - Faylın əsas məzmununun kök elementini təmsil edir.

`<w:body> ` - Paraqraflar, cədvəllər və bölmələr kimi bir çox digər element qovşaqlarından ibarət ola bilən sənədin əsas hissəsini təmsil edir.

#### Paraqraflar ####

Paraqraf sənəddə əsas məzmun sahibidir. ** ilə təmsil olunur<w:p> ** sənəd daxilində element. Bundan əlavə, paraqraf bir və ya bir neçə qaçışdan ibarətdir **<w:r> ** paraqrafın faktiki mətnini ehtiva edir. Qaçışlara əlavə olaraq, paraqraflarda hiperlinklər, şərhlər və s. kimi digər sənəd elementləri də ola bilər. Paraqraf strukturunun nümunəsi aşağıda göstərildiyi kimidir:

```
<w:p>
<w:pPr>
<w:pStyle> w:val#"MyStyle"/>
<w:spacing w:before#"120" w:after#"120"/>
</w:pPr>
<w:r>
<w:t xml"space#"preserve">A paragraph is main container in a document that further consists of a one or more runs where the text of paragraph is actually contained.</w:t>
</w:r>
</w:p>
```

## DOCX tez-tez verilən suallar

 * **DOCX fayl uzantısıdırmı?** - DOCX Microsoft Word 2007 və Word fayllarını saxlamaq üçün istifadə edilən sonrakı fayl formatlarını təmsil etmək üçün fayl uzantısı kimi istifadə olunur. O, həmçinin ƏS-nizə bildirir ki, bu DOCX faylı onu açmaq və simvolunu göstərmək üçün Microsoft Word 2007 tələb edir.
 * **DOCX Word ilə eynidir** - DOCX sənədləri Açıq XML formatında saxlamaq üçün Microsoft Word tərəfindən istifadə olunan fayl formatıdır. Word, digər tərəfdən, DOC, DOT, DOTM və başqaları kimi digər fayl formatlarını da dəstəkləyən Microsoft Office tərəfindən tətbiq olunan proqramdır.
 * **DOC və DOCX fərqi nədir** - DOC Word 2007 və əvvəlki fayl formatında saxlanılan söz faylıdır. DOCX Microsoft 2007 və sonrakı versiyalar tərəfindən dəstəklənən Açıq XML fayl formatına əsaslanır. Ətraflı məlumat üçün [DOC və DOCX arasındakı fərqləri](https://blog.fileformat.com/2022/08/11/doc-vs-docx/) yoxlayın.

## İstinadlar ##

* [MS - DOCX Fayl Format](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd)

* [Office Open XML](http://officeopenxml.com/)


