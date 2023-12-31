{
  "date" : "2022-04-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AML Dosyası - ACPI Makine Dili Dosyası",
  "description":"ACPI AML dosya formatı ve AML dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier" : "system-aml",
      "parent" : "system"
}
},
  "lastmod" : "2022-04-12"
}

## AML dosyası nedir?

AML dosyası, donanım özelliklerini yapılandırmak için kullanılan Gelişmiş Yapılandırma ve Güç Arabirimi (ACPI) diliyle oluşturulmuş bir sistem dosyasıdır. Bir bilgisayarı kapatmak gibi basit işlemler için bile donanımı yapılandırmak için kullanılan makineden bağımsız bayt kodunu içerir. AML dosyaları, makineye kurulma amacına bağlı olarak talimatlar içerebilir. ACPI standartlarının uygulanması, güç yönetimi işlevselliğini ve P55 anakartları gibi anakart cihazlarını yapılandırmak için sağlam bir arabirimi geliştirmenize olanak tanır.

## ACPI AML Dosya Biçimi

AML dosyaları, bayt kodunda yazılmış içeriklerle diske ikili dosyalar olarak kaydedilir. ACPI standardının dosya biçimi belirtimleri [uefi](https://uefi.org/) adresinde mevcuttur. Dil, uygulama yığınının daha az yeniden yazılmasını veya yeniden oluşturulmasını gerektirecek şekilde kararlılık ve geriye dönük uyumluluk sunacak şekilde tasarlanmıştır.

## AML Dosya Biçimi Özellikleri

Bir AML dosyası, DSDT ve SSDT tablolarından oluşur. AML bayt kodu, bu tabloların her birinin başından itibaren okunur ve ayrıştırılır. Bu, ACPI ad alanındaki aygıtların ve nesnelerin tanımları hakkında bilgi verir. AML yorumlayıcısı bu bilgiyi kullanarak sistemde bulunan tüm cihazların ve bunların desteklenen özelliklerinin ve işlevlerinin bir listesini oluşturabilir.

### Bir DSDT için Örnek ASL Kodu

Bir DSDT için ASL kodunun bir örneği aşağıdaki gibidir.

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

## Referanslar

* [ACPI AML](https://wiki.osdev.org/AML)
* [DSDT](https://wiki.osdev.org/DSDT)
* [SSDT](https://wiki.osdev.org/SSDT)

