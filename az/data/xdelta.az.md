{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "XDELTA Fayl - xdelta Diferensial Fayl - .xdelta faylı nədir və onu necə açmaq olar?",
  "description" : "Xdelta Diferensial Faylı və onu necə açmaq barədə məlumat əldə edin.",
  "linktitle" : "XDELTA",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-xdelta-az",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## XDELTA faylı nədir?

XDELTA fayl formatı iki digər fayl arasında ikili fərqləri özündə saxlayır və iki fayl arasındakı fərqləri hesablamağı və bu fərqləri kompakt formatda kodlamağı nəzərdə tutan delta kodlaşdırması üçün əmr xətti yardım proqramı olan xdelta aləti tərəfindən yaradılır. XDELTA faylları orijinal fayl və yenilənmiş fayl arasındakı dəyişiklikləri və ya fərqləri təmsil edən ikili məlumatları saxlayır. XDELTA faylındakı ikili verilənlər bir faylı (orijinal) digər fayla (yenilənmiş və ya yamaqlanmış versiya) çevirmək üçün lazım olan dəyişiklikləri təmsil edir.

XDELTA faylları tez-tez oyun icmasında video oyunları üçün modifikasiyaları (modları) yaymaq üçün istifadə olunur. Bu modlar kosmetik dəyişikliklərdən tutmuş oyun mexanikasında əhəmiyyətli dəyişikliklərə qədər hər şeyi əhatə edə bilər. XDELTA faylları istifadəçilərə XDELTA faylında göstərilən dəyişikliklərlə orijinal oyun fayllarını yamaq etməklə bu dəyişiklikləri öz oyun qurğularına tətbiq etməyə imkan verir.

## xdelta

`xdelta` delta kodlaşdırması və dekodlanması üçün istifadə edilən komanda xətti yardım proqramıdır; o, əsasən iki fayl arasında tez-tez delta yamaqları və ya xdelta yamaları adlanan ikili yamaqların yaradılması və tətbiqi üçün istifadə olunur; bu yamaqlar orijinal fayl ilə dəyişdirilmiş və ya yenilənmiş versiya arasındakı fərqləri təmsil edir, xüsusən də bant genişliyi və ya yaddaş sahəsinin məhdud olduğu ssenarilərdə yeniləmələrin səmərəli paylanmasına imkan verir.

Budur `xdelta`-nın əsas funksiyalarının qısa icmalı:

1.  **Creating patches**: `xdelta` can generate a patch file that contains differences between two files. This patch file, often referred to as an "xdelta patch", is relatively small compared to original and updated files, as it only contains the changes between them.
    
2.  **Applying patches**: Once a patch file is created, `xdelta` can apply it to original file to produce updated file. This process involves taking original file and patch file as input and applying changes specified in patch file to generate updated file.
    
3.  **Applying reverse patches**: `xdelta` can also apply reverse patches, which revert changes made to a file. This is useful for rolling back updates or modifications.
    

`xdelta` adətən proqram yeniləmələrinin paylanması, video oyunların düzəldilməsi və quraşdırılmış cihazlarda və ya şəbəkə cihazlarında sistem fayllarının yenilənməsi kimi müxtəlif ssenarilərdə istifadə olunur. O, bant genişliyi istifadəsini və saxlama tələblərini minimuma endirərkən fayl yeniləmələrini idarə etmək üçün çevik və səmərəli üsul təqdim edir.

## xdeltaui

xdeltaui XDELTA yamaqlarını idarə etmək və tətbiq etmək üçün qrafik istifadəçi interfeysi (GUI) proqramıdır. xdelta gui istifadəçilər üçün XDELTA faylları ilə qarşılıqlı əlaqədə olmaq və onları müvafiq orijinal fayllara tətbiq etmək, onları effektiv şəkildə yamaq və ya yeniləmək üçün istifadəçi dostu interfeys təqdim edir.

Mətn-əsaslı əmrlər vasitəsilə işləyən xdelta-nın komanda xətti versiyasından fərqli olaraq, xdeltaui xüsusilə komanda xətti interfeysləri ilə tanış olmayan və ya qrafik alətlərə üstünlük verən istifadəçilər üçün XDELTA fayllarını idarə etmək üçün daha intuitiv üsul təklif edir.

Xdeltaui ilə istifadəçilər adətən orijinal faylı seçmək, XDELTA yamaq faylını seçmək və yenilənmiş fayl yaratmaq üçün yamaq tətbiq etmək kimi tapşırıqları yerinə yetirə bilərlər. Bu, video oyunlar və ya digər proqram proqramları üçün modlar və ya yeniləmələr quraşdırmaq üçün xüsusilə faydalı ola bilər.

## xdelta Yüklə

Linux sistemlərində `xdelta` quraşdırmaq üçün `apt`, `yum` və ya `dnf` kimi paket menecerlərindən istifadə edə bilərsiniz. Məsələn, Ubuntu-da aşağıdakı əmrdən istifadə edə bilərsiniz:

```
sudo apt-get install xdelta3
```

## xdelta necə istifadə olunur

`xdelta` istifadə etmək üçün adətən bu ümumi addımları yerinə yetirməlisiniz:

1.  **Yükləyin və quraşdırın**: Əvvəlcə sisteminizdə `xdelta` quraşdırıldığından əmin olun. Siz onu rəsmi saytından, paket menecerlərindən və ya digər etibarlı mənbələrdən yükləyə bilərsiniz.
    
2.  **Prepare Files**: Prepare original file (often called source or base file) and updated file (target file) that you want to create a patch for or apply a patch to.
    
3.  **Patch yaradılması**:
    
- Komanda xətti interfeysinizi açın (terminal və ya əmr satırı).
- Yamaq yaratmaq üçün müvafiq seçimlərlə `xdelta` əmrindən istifadə edin. Əsas sintaksis belədir:
               
```
xdelta delta<original_file><updated_file><patch_output_file>
```
        
` ilə əvəz edin<original_file> ` orijinal faylın yolu ilə, `<updated_file> ` yenilənmiş faylın yolu ilə və `<patch_output_file> ` patch faylı üçün istədiyiniz adla.
- Misal:
               
```
xdelta delta original_fayl updated_file patch.xdelta
```
        
4.  **Yamağın tətbiqi**:
    
- Orijinal faylın və yamaq faylının mövcud olduğundan əmin olun.
- Komanda xətti interfeysinizi açın.
- Yamağı tətbiq etmək üçün müvafiq seçimlərlə `xdelta` əmrindən istifadə edin. Əsas sintaksis belədir:
        
      
```
xdelta yaması<original_file><patch_file><output_file>
```
        
` ilə əvəz edin<original_file> ` orijinal faylın yolu ilə, `<patch_file> ` patch faylının yolu ilə və `<output_file> ` çıxış faylı üçün istədiyiniz adla.
- Misal:
                
```
xdelta patch original_file patch.xdelta updated_file
```
        
5.  **Köməyə Baxış**: Xüsusi seçimlər və ya əmrlərlə bağlı köməyə ehtiyacınız varsa, istifadə məlumatını və mövcud seçimləri göstərmək üçün `--help` seçimi ilə `xdelta` əmrindən istifadə edə bilərsiniz.
    
## XDELTA faylını necə açmaq olar

XDELTA faylları birbaşa açmaq üçün nəzərdə tutulmayıb. Əgər siz XDELTA yamasını oyuna və ya başqa fayla tətbiq etmək istəyirsinizsə, ya bir neçə platformaya uyğun gələn xdelta, ya da xüsusi olaraq Windows istifadəçiləri üçün nəzərdə tutulmuş xdelta UI-dən istifadə etmək seçiminiz var.

## İstinadlar
* [xdelta](https://en.wikipedia.org/wiki/Xdelta)


