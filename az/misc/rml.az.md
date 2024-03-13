{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "RML - Elixir Hesabat Şablon Faylı",
  "description":"RML faylları yarada və aça bilən RML faylı və API-lər haqqında məlumat əldə edin.",
  "linktitle" : "RML",
  "menu" : {
    "docs" : {
      "identifier":"misc-rml-az",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## RML faylı nədir?

RML faylı [Elixir Repertoire](https://elixirtech.com/repertoire-2/) hesabat mühərriki ilə hesabat şablonu faylıdır. Şablon faylı Elixir Fayl Sisteminə qoşulmuş məlumat mənbəyi ilə hesabatlar yaratmaq üçün istifadə olunur. Data RML şablon faylında oxunur və doldurulur və [PDF](/pdf/), [RTF](/word-processing/rtf/) və [XLS](/spreadsheet/xls/) cədvəli kimi bir sıra müxtəlif fayl formatlarına ixrac edilə bilər. Elixir Repertuar hesabat mühərriki müxtəlif JDBC məlumat mənbələrinə qoşula bilər.

## RML fayl formatı

RML fayl formatının daxili fayl strukturu təfərrüatları ictimaiyyətə açıq deyil. Fayllar qoşulmuş məlumat mənbələrindən yığılmış məlumatlarla hesabatlar yaratmaq üçün Elixir Repertuar tətbiqi tərəfindən daxili olaraq yaradılır və saxlanılır. RML şablon faylı məlumatlardan yaradılacaq yekun hesabatın ümumi tərtibatını və yer tutucu məlumatlarını ehtiva edir.

## RML Şablon Faylı necə hazırlanır?

Elixir Repertuarında RML şablonu yaratmaq üçün aşağıdakı addımları yerinə yetirmək olar.

1. JDBC məlumat mənbəyini fayl sisteminə qoşun.
1. Hesabat Şablonu Sihirbazını işə salın
1. Məlumat mənbəyi .ds faylını tapmaq üçün proqram təminatından istifadə edin
1. İxrac seçimi kimi cədvəl hesabatını seçin
1. Hesabat şablonuna daxil ediləcək sahələri seçin
1. Nəhayət, Bitir düyməsini kliklədikdə, First report.rml depoya əlavə edilir və Layout nişanını göstərmək üçün açılır.

## İstinadlar

* [Eliksir Repertuarı](https://elixirtech.com/repertoire-2/)


