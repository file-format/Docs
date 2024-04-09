{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RML - İksir Raporu Şablon Dosyası",
  "description":"RML dosyası ve RML dosyaları oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "RML",
  "menu" : {
    "docs" : {
      "identifier":"misc-rml",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Bir RML dosyası nedir?

Bir RML dosyası, [Elixir Repertoire](https://elixirtech.com/repertoire-2/) raporlama motoruna sahip bir raporlama şablon dosyasıdır. Şablon dosyası, Elixir Dosya Sistemine bağlı veri kaynağı ile raporlar oluşturmak için kullanılır. Veriler RML şablon dosyasında okunur ve doldurulur ve [PDF](/tr/pdf/), [RTF](/tr/word-processing/rtf/) ve elektronik tablo [XLS] gibi bir dizi farklı dosya biçimine dışa aktarılabilir. (/tr/spreadsheet/xls/). Elixir Repertoire raporlama motoru, çok çeşitli JDBC veri kaynaklarına bağlanabilir.

## RML Dosya Biçimi

RML dosya biçiminin dahili dosya yapısı ayrıntıları herkese açık değildir. Dosyalar, bağlı veri kaynaklarından doldurulan verilerle raporlar oluşturmak için Elixir Repertoire uygulaması tarafından dahili olarak oluşturulur ve kaydedilir. RML şablon dosyası, verilerden oluşturulacak nihai raporun genel düzenini ve yer tutucu bilgilerini içerir.

## RML Şablon Dosyası Nasıl Yapılır?

Elixir Repertuarında RML şablonu oluşturmak için aşağıdaki adımlar izlenebilir.

1. Bir JDBC veri kaynağını dosya sistemine bağlayın.
1. Rapor Şablonu Sihirbazını Başlatın
1. Veri kaynağı .ds dosyasını bulmak için yazılımı kullanın
1. Dışa aktarma seçeneği olarak tablo raporunu seçin
1. Rapor şablonuna dahil edilecek alanları seçin
1. Son olarak Bitir butonuna basıldığında First report.rml depoya eklenir ve Layout (Düzen) sekmesini gösterecek şekilde açılır.

## Referanslar

* [İksir Repertuarı](https://elixirtech.com/repertoire-2/)

