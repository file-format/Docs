{
  "date" : "2020-11-11",
  "keywords" :[ "BCP", "uzantı", "dosya", "dosya biçimi", "Veritabanı Dosya Türü", "Veritabanı Dosya Biçimi", "Veritabanı Dosyaları" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"BCP dosya formatı ve BCP dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"BCP - SQL Server Toplu Kopya Dosya Formatı",
  "linktitle" : "BCP",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## BCP dosyası nedir?

BCP (Bulk Copy Format), içe/dışa aktarma için farklı veritabanı veri türü değerlerini depolamak üzere veri yapılarını tanımlayan Microsoft SQL Server'ın teknik veri biçimidir. Biçim, veri dosyasında belirtilen değerler kümesinin okunabilmesi için her bir veri sütununun yorumlanmasını tam olarak tanımlar. [BCP](https://docs.microsoft.com/en-us/previous-versions/sql/sql-server-2008-r2/ms162802(v=sql.105)) yardımcı programı, okumak için BCP dosya biçimini kullanır böyle bir dosyadan veri ve onu tanımlayın.


## BCP Dosya Biçimi

BCP biçim dosyası, sütun sırasını, adını ve veri türünü tanımlayan bir XML belgesidir. Kullanıcıların bu alanları belirterek veri dosyasından büyük miktarda veri içe/dışa aktarmasına olanak tanır. Bu, veri dosyalarından veri değerlerinin toplu içe aktarılmasında yardımcı olur. Veri dosyasındaki veri alanlarının sayısı ve sırası, hedef tablo sütunlarındakinden farklı olabilir. Bu, BCP veri formatı dosyasının, verileri içe aktarmak için sütunların sırasını ve türünü belirterek yardıma geldiği zamandır.

Biçim dosyasının yapısı aşağıdaki biçimde temsil edilir.

```
<BCPFORMAT ...>
    <RECORD>
       <FIELD ID = "fieldID" xsi:type = "fieldType" [...] />
    </RECORD>
    <ROW>
       <COLUMN SOURCE = "fieldID" NAME = "columnName" xsi:type = "columnType" [...]  />
    </ROW>
 </BCPFORMAT>
```

### BCP Veri Türleri

|Veri Türü|Aralık|Gösterim|
---|---|---|
|BigInt|-263 (-9.223.372.036.854.775.808) ila 263-1 (9.223.372.036.854.775.807)|`BigInt = ["-"]1*19DIGIT`|
|İkili|1 ila 8000 bayt|onaltılık kodlu Unicode dize biçimi 'İkili = 32000OCTET'|
|Bit|0 veya 1|basit Unicode dizisi Bit = "0" / "1"|
|Karakter|1 ila 8000|Unicode Dizgi Formatı, Karakter = 16000OCTET|
|CLRUDT|VarBinary|CLRUDT = 0*nOCTET ile n = 4 x (2.147.483.647)|
|Tarih|0001-01-01 ila 9999-12-31|YYYY-AA-GG dize biçimi|
|TarihSaat|1753-01-01 00:00:00.000 - 9999-12-31 23:59:59.997| Unicode YYYY-AA-GG ss:dd:ss[.nnn] string format|
|DateTime2|0001-01-01 00:00:00.0000000 - 9999-12-31 23:59:59.9999999.| Unicode YYYY-AA-GG ss:dd:ss[.nnnnnnn] string format|
|DateTimeOffset|0001-01-01 00:00:00.0000000 ila 9999-12-31 23:59:59.9999999 Eşgüdümlü Evrensel Saat (UTC) saat diliminde| Unicode YYYY-AA-GG ss:dd:ss[.nnnnnnn] [{+|-}ss:dd] dize biçimi|
|Ondalık|-1038 + 1 ila 1038 – 1|Unicode dize biçimi `Ondalık = ["-"] 0*38DIGIT ["."0*38DIGIT]`|
|Kayan|-1.79E+308 ila -2.23E-308; 0; 2.23E-308'den 1.79E+308'e|Unicode dize biçimi|
|Görüntü|0 ile 231 – 1 (2.147.483.647) arasında değişen bayt dizisi|onaltılık kodlanmış Unicode dize biçimi|
|Int|-231 (-2,147,483,648) ila 231 – 1 (2,147,483,647)|Unicode dize biçimi|

## Referanslar

* [BCP Biçimi - Microsoft](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)

