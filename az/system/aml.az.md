{
  "date" : "2022-04-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AML Faylı - ACPI Maşın Dili Faylı",
  "description":"ACPI AML fayl formatı və AML faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier" : "system-aml-az",
      "parent" : "system"
}
},
  "lastmod" : "2022-04-12"
}

## AML faylı nədir?

AML faylı aparat xüsusiyyətlərini konfiqurasiya etmək üçün istifadə olunan Qabaqcıl Konfiqurasiya və Güc İnterfeysi (ACPI) dili ilə yaradılmış sistem faylıdır. O, kompüterin bağlanması kimi sadə əməliyyatlar üçün belə aparatı konfiqurasiya etmək üçün istifadə edilən maşından asılı olmayan bayt kodu ehtiva edir. AML fayllarında onun maşında quraşdırılması məqsədindən asılı olaraq təlimatlar ola bilər. ACPI standartlarının tətbiqi enerji idarəetmə funksionallığını və P55 ana plataları kimi anakart cihazlarını konfiqurasiya etmək üçün möhkəm interfeysi təkmilləşdirməyə imkan verir.

## ACPI AML Fayl Formatı

AML faylları ikili fayllar kimi bayt kodu ilə yazılmış məzmunu olan diskdə saxlanılır. ACPI standartının fayl formatı spesifikasiyası [uefi](https://uefi.org/) üzərində mövcuddur. Dil sabitlik və geriyə uyğunluq təklif etmək üçün nəzərdə tutulmuşdur, tətbiq yığınının daha az yenidən yazılmasını və ya yenidən qurulmasını tələb edir.

## AML Fayl Formatının Xüsusiyyətləri

AML faylı DSDT və SSDT cədvəllərindən ibarətdir. AML bayt kodu bu cədvəllərin hər birinin əvvəlindən oxunur və təhlil edilir. Bu, ACPI ad məkanındakı cihazların və obyektlərin tərifləri haqqında məlumat verir. Bu məlumatdan istifadə edərək, AML tərcüməçisi sistemdə mövcud olan bütün cihazların və onların dəstəklənən xassələrinin və funksiyalarının siyahısını yarada bilər.

### DSDT üçün ASL kodu nümunəsi

DSDT üçün ASL kodunun nümunəsi aşağıdakı kimidir.

```
DefinitionBlock ("test.aml", "DSDT", 1, "OEMID ", "TABLEID  ", 0x00000000)
{
    Scope (_SB)
    {
        Device (PCI0)
        {
            Name (_HID, EisaId ("PNP0A03"))
    }
}
}
```

## İstinadlar

* [ACPI AML](https://wiki.osdev.org/AML)

* [DSDT](https://wiki.osdev.org/DSDT)

* [SSDT](https://wiki.osdev.org/SSDT)


