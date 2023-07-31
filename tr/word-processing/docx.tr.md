{
  "date" : "2019-12-03",
  "keywords" :[ "DOCX","dosya", "biçim", "dosya türü", "uzantı","DOCX dosyası nedir?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOCX",
  "description":"DOCX dosya formatı ve DOCX dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "DOCX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## DOCX dosyası nedir? ##

DOCX, Microsoft Word belgeleri için iyi bilinen bir biçimdir. 2007'den itibaren Microsoft Office 2007'nin piyasaya sürülmesiyle tanıtılan bu yeni Belge biçiminin yapısı, düz ikiliden XML ve ikili dosyaların birleşimine değiştirildi. Docx dosyaları, Word 2007 ve yan sürümleriyle açılabilir, ancak MS Word'ün DOC dosya uzantılarını destekleyen önceki sürümleriyle açılamaz.

## Kısa Tarih ##

Microsoft, DOC dosya formatının belirtimlerini açtıktan sonra, rakiplerinin formatı tersine çevirmesi ve aynı desteği kendi uygulamalarında sağlaması kolay oldu. Ek olarak, Open Office'in Açık Belge Biçimi biçimindeki rekabeti, Microsoft'u daha açık ve geniş standartlar benimsemeye zorladı. Microsoft, **Office Açık XML** standardına uyum sağlamak için değişikliğe gitmeye karar verdiğinde 2000 yılının başlarındaydı. Bu yeni Standart kapsamındaki belgelere [.docx uzantısı](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd), "X" verildi XML için olmak. 2007 yılına gelindiğinde, bu yeni dosya biçimi Office 2007'nin bir parçası haline geldi ve Microsoft Office'in yeni sürümlerinde de sürdürülüyor. Yeni dosya türü, küçük dosya boyutları, daha az bozulma değişikliği ve iyi biçimlendirilmiş görüntülerin temsili gibi avantajlar ekledi.

## DOCX Dosya Biçimi Özellikleri - Daha Fazla Bilgi

Bir Docx dosyası, bir ZIP arşivinde bulunan bir XML dosyaları koleksiyonundan oluşur. Yeni bir Word belgesinin içeriği, içeriğini açarak görüntülenebilir. Koleksiyon, şu şekilde kategorize edilen XML dosyalarının bir listesini içerir:

* MetaData Dosyaları - arşivde bulunan diğer dosyalar hakkında bilgi içerir
* Belge - belgenin asıl içeriğini içerir

### Meta veri dosyaları ###

Microsoft Word, dosyalar arasındaki ilişkiyi bulmak ve belge içeriğini bulmak için bu dosyaları kullanır. Bir Word belge arşivi çıkarıldığında, aşağıda ayrıntıları verilen bir dizi dosya içerir.

#### İlişkiler - \_rels/.rels ####

Bu dosya, MS Word'e belge içeriğini ve diğer referansları nerede arayacağını söyleyen bilgiler içerir. Her ilişki, benzersiz bir ilişki kimliğiyle tanımlanır ve başvurulan XML dosyasını hedef olarak belirtir. Örnek bir ilişki dosyası aşağıdaki şekilde gösterilmiştir:

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"word/document.xml"/>.
```

#### İçerik Türleri ####

Bir belge, içinde resimler, temalar, kelime sanatı vb. gibi çeşitli ortam türleri içerebilir. [Content_Types].xml, belgede bulunan bu tür ortam türleri hakkında bilgi içerir. Böyle bir XML dosyasının içeriği aşağıdaki gibi gösterilir:

```
<Override PartName#"/word/document.xml" ContentType#"application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/>
```

#### Kaynaklara Referanslar - \_rels/document.xml.rels ####

Belgeye katıştırılmış resimler gibi kaynaklar hakkındaki bilgilere bu XML dosyasında başvurulur.

#### Ana Belge İçeriği ####

Bu, belgenin metin içeriğini içeren arşivin ana XML dosyasına atıfta bulunur. Bu içerik, OpenOffice XML belirtimlerine göre çeşitli düğümlerle temsil edilir. Bu dosyanın içeriği çoğunlukla Paragraflar ve Tablolardan oluşur, ancak bunlar başka düğümler de olabilir.

### Dosya Biçimi Düğümleri ###

Ana Document.xml dosyası, bir dosyanın genel içeriğinin temsili için bir düğüm koleksiyonudur. Her düğümün, diğer düğümleri veya içerikleri kapsayan bir başlangıcı ve sonu vardır. Böyle bir xml dosyasının basitleştirilmiş bir örneği aşağıdaki gibidir:

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

İçeriğin temsili için bir DOCX dosyasında bulunan bazı düğümler hakkında bilgiler aşağıdadır.

`<w:document> ` - Dosyanın ana içeriğinin kök öğesini temsil eder.

`<w:body> ` - Paragraflar, tablolar ve bölümler gibi diğer birçok öğe düğümünden oluşabilen belgenin gövdesini temsil eder.

#### Paragraflar ####

Paragraf, bir belgedeki ana içerik sahibidir. ** ile temsil edilir<w:p> ** belge içindeki öğe. Bir paragraf ayrıca bir veya daha fazla satırdan oluşur **<w:r> ** paragrafın gerçek metnini içeren. Paragraflar, çalıştırmalara ek olarak köprüler, yorumlar vb. diğer belge öğelerini de içerebilir. Örnek bir paragraf yapısı aşağıda gösterildiği gibidir:

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

## Referanslar ##

* [MS - DOCX Dosya Biçimi](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd)
* [Office Açık XML](http://officeopenxml.com/)

