{
  "date" : "2021-06-29",
  "keywords" :[ "com dosyası", "com dosyası nedir", "dosya", "com örneği", "com dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"COM dosya formatı ve COM dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"COM - DOS Komut Dosyası Biçimi",
  "linktitle" : "COM",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-29"
}

## COM dosyası nedir?
COM dosyaları, yalnızca bir dizi komut veya talimatı yürütmek için kullanılır. Bir COM dosyası, Windows veya MS-DOS'tan çalıştırılabilen yürütülebilir bir programdan oluşur. Bir EXE dosyası gibi, COM dosyası da ikili biçimde kaydedilir, ancak EXE dosyasından farklıdır çünkü üstbilgisi veya meta verileri yoktur ve ayrıca maksimum boyutu yaklaşık 64 KB'dir. COM dosyası 32 bit sistemde ilk kez çalıştırıldığında, NT Virtual DOS Machine (NTVDM) bileşeninin yüklenmesini ister. COM dosyası, MS-DOS ortamını destekleyen bir sanal makine ile Microsoft Windows'un 64 bit sürümünde çalıştırılabilir.

## COM dosya biçimi
COM dosya formatı, Microsoft Windows veya MS-DOS'ta kullanılan ikili yürütülebilir bir formattır. Yapısı yalnızca bir dizi talimattan oluşur; başlığı yoktur ve standart meta veri içermez. Tüm verilerini ve kodunu yalnızca bir segmentte depolar ve ikili dosyası maksimum 64 KB boyutundadır. Bu dosya biçimi, yeniden çalıştırmayı denediğinizde yerini değiştirmez. Böylece işletim sistemi onu önceden ayarlanmış bir adrese yükler. Ayrıca, her iki işletim sisteminde de yürütülecek bir COM dosyasını **fat ikili** biçiminde yapmak mümkündür. Talimat düzeyinde herhangi bir gerçek uyumluluk yoktur. Giriş noktasındaki komutlar her iki işletim sisteminde işlevsellik olarak eşit fakat farklı olacak şekilde seçilir ve programın çalışmasını sağlar, kullanılan işletim sisteminin bölümüne atlar. Temel olarak, tek bir dosyada aynı prosedüre sahip iki farklı programdır ve öncesinde kullanılacak olanı seçen kod bulunur.
### COM dosyası örneği
Bir COM dosyası yürütülürken, komutlar ilk bayttan itibaren okunur ve son komutlar bulunana kadar art arda takip edilir. İşte bir ASM kodu örneği:

```
[BITS 16]		;Set code generation to 16 bit mode
[ORG 0x0100]		;Set code start address to 0100h


[SEGMENT .text]		;Main code segment
    mov ah, 9 ; DOS print string function
    mov dx, hello
    int 21h
    ;Exit to DOS
    mov ah, 4ch
    int 21h
[SEGMENT .data]		;Initialised data segment
hello:   db   'Hello, .COM programmer!',13,10,'$'
```

## Referanslar

* [COM dosyası - Wikipewdia tarafından](https://en.wikipedia.org/wiki/COM_file)

