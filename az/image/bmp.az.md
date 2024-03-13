{
  "date": "2019-10-11",
  "keywords": [
"bmp faylı",
"bmp fayl formatı",
"bmp faylı nədir",
"fayl",
"bmp nümunəsi",
"bmp fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "BMP - Şəkil fayl formatı",
  "description": "BMP faylları yarada və aça bilən BMP fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "BMP",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-bm-azp"
}
},
  "lastmod": "2019-09-10"
}

# BMP faylı nədir? #

.BMP uzantısına malik fayllar bitmap rəqəmsal şəkilləri saxlamaq üçün istifadə olunan Bitmap Şəkil fayllarını təmsil edir. Bu təsvirlər qrafik adapterdən müstəqildir və həmçinin cihazdan müstəqil bitmap (DIB) fayl formatı adlanır. Bu müstəqillik faylın Microsoft Windows və Mac kimi bir çox platformada açılması məqsədinə xidmət edir. BMP fayl formatı məlumatları həm monoxrom, həm də müxtəlif rəng dərinliklərinə malik rəngli formatda iki ölçülü rəqəmsal şəkillər kimi saxlaya bilər.

## BMP Fayl Formatının Xüsusiyyətləri ##

Cihazdan Müstəqil Bitmaplar qurğular və tətbiqlər arasında bitmapların mübadiləsinə yardımçı kimi çıxış edir. Bu fayl formatının davamlı təkamülü səbəbindən başlıqlarda olan məlumatlar Bitmap versiyasına görə fərqli ola bilər. Tək bitmap faylı müəyyən bir ardıcıllıqla sabit, eləcə də dəyişən ölçülü strukturlardan ibarətdir.

Bitmap faylındakı strukturlar aşağıdakı ardıcıllıqla düzülür:


|Struktur|Könüllü|Ölçü|Məqsəd
---|---|---|---|
|Fayl Başlığı|No|14|Bitmap şəkil faylı haqqında ümumi məlumatı saxlamaq üçün
|DIB Başlığı|Xeyr|Sabit Ölçü|Bitmap təsviri haqqında ətraflı məlumat saxlamaq və piksel formatını təyin etmək üçün
|Əlavə Bit Maskaları|Bəli|12 və ya 16 bayt|Piksel formatını müəyyən etmək üçün
|Rəng Palitrası|Yarı-isteğe bağlı|Dəyişən ölçülü|Bitmap şəkil datası tərəfindən istifadə olunan rəngləri müəyyən etmək üçün
|Gap1|Bəli|Dəyişən ölçülü|Strukturun uyğunlaşdırılması
|Pixel Array|No|Dəyişən ölçülü|Piksel formatı DIB başlığı və ya Əlavə bit maskaları ilə müəyyən edilir.
|Gap2|Bəli|Dəyişən ölçülü|Strukturun uyğunlaşdırılması
|ICC Rəng profili|Bəli|Dəyişən ölçülü|Rəng idarə edilməsi üçün rəng profilini müəyyən etmək üçün

Bitmap təsviri yaddaşa yükləndikdə, Windows tərəfindən GDI API vasitəsilə istifadə edilən DIB strukturuna çevrilir. Fayl başlığı bu məlumat strukturunun bir hissəsi deyil. Rəng, həmçinin açıq RGB rəng tərifləri əvəzinə hazırda istinad edilən palitraya indekslər təşkil edən 16 bitlik girişlərdən ibarət ola bilər. Gəlin bunlardan bəzilərinə, xüsusən də başlıqlara ətraflı nəzər salaq.

### Bitmap Fayl Başlığı ###

Bitmap Fayl Başlığı faylı müəyyən etmək üçün istifadə olunan digər fayl başlıqlarına bənzəyir. BMP fayl formatının müxtəlif variantları olduğundan, BMP fayl formatının ilk 2 baytı ASCII kodlaşdırmasında B simvolu, sonra isə M simvoludur. Bütün tam dəyərlər kiçik endian formatında saxlanılır.

|Offset hex|Offset dec|Ölçü|Məqsəd
---|---|---|---|
|00|0|2 bytes|The header field used to identify the BMP and DIB file is 0x42 0x4D in hexadecimal, same as BM in ASCII. It can following possible values.* **BM** – Windows 3.1x, 95, NT, ... etc. * **BA** – OS/2 struktur bitmap massivi * **CI** – OS/2 struktur rəng nişanı * **CP** – OS/2 konst rəng göstəricisi * **IC** – OS/2 struktur nişanı * **PT** – OS/2 göstəricisi
|02|2|4 bayt|BMP faylının baytla ölçüsü
|06|6|2 bayt|Ehtiyatdadır; faktiki dəyər təsviri yaradan proqramdan asılıdır
|08|8|2 bayt|Ehtiyatdadır; faktiki dəyər təsviri yaradan proqramdan asılıdır
|0A|10|4 bayt|Bitmap təsvir məlumatının (piksel massivi) tapıla biləcəyi baytın ofseti, yəni başlanğıc ünvanı.

#### DIB başlığı (bitmap məlumat başlığı) ####

Şəkil haqqında ətraflı məlumat bu başlıq ilə təmsil olunur. Bu məlumat əsasında ekranda təsviri göstərmək üçün istifadə olunacaq proqram müəyyən ediləcək. Bütün bu cür başlıqlar onların ölçüsünü təyin edən DWORD (32-bit) sahəsini ehtiva edir ki, tətbiq təsvirdə istifadə olunan başlığı asanlıqla müəyyən edə bilsin. Bu, əsasən, DIB formatının bir neçə uzantıya məruz qalması ilə bağlıdır. Aşağıda sadalanan sahələri olan DIB Başlığı verilmişdir.

#### Rəng Palitrası ####

BMP rəng palitrası displey cihazının rəng palitrasında hər bir rəngin RGB intensivlik dəyərlərini təyin edən strukturlar massividir. Bitmap verilənlərindəki hər bir piksel rəng palitrasında indeks kimi istifadə edilən tək dəyəri saxlayır. Həmin indeksdəki elementdə saxlanılan rəng məlumatı həmin pikselin rəngini təyin edir. Bitmap faylında rəng mövcudluğu aşağıdakı kimi dəyişir:

* Bir, 4 və 8 bit - həmişə rəng palitrası ehtiva etməsi gözlənilir

* On altı, 24 və 32 bit - heç vaxt rəng palitrası ehtiva etmir

* On altı və 32 bitlik BMP faylları - rəng palitrası əvəzinə bit sahələri maskası dəyərlərindən ibarətdir


#### Piksel Yaddaşı ####

Bitmap pikselləri sətirlərdə yığılmış bitlər kimi saxlanılır, burada hər bir cərgənin ölçüsü doldurulma yolu ilə 4 bayta (32 bitlik DWORD) çoxluğa qədər yuvarlaqlaşdırılır. Təsvirin piksellərini saxlamaq üçün tələb olunan baytların ümumi miqdarını yalnız bitləri saymaqla birbaşa hesablamaq mümkün deyil. Doldurma ilə bağlı olduğundan, hər bir cərgənin ölçüsünü 4 bayta qədər yuvarlaqlaşdırma effekti tələb olunur. Doldurma baytları (mütləq 0 deyil) sıraların uzunluğunu dörd bayta çatdırmaq üçün cərgələrin sonuna əlavə edilməlidir. Piksel massivi yaddaşa yükləndikdə, hər bir sətir 4-ə çox olan yaddaş ünvanından başlamalıdır.

Şəkil əslində piksel massivinin 32 bitlik DWORD təqdimatı ilə təsvir edilmişdir. Adətən piksellər aşağı sol küncdən başlayaraq, soldan sağa, sonra isə təsvirin aşağıdan yuxarıya doğru cərgə-cərgə saxlanılaraq aşağıdan yuxarıya” saxlanılır. Piksel formatları və onların təsiri aşağıda verilmişdir:

* Piksel başına 1 bit (1bpp) formatı 2 fərqli rəngi dəstəkləyir (məsələn: qara və ağ).

* Piksel başına 2 bit (2bpp) formatı 4 fərqli rəngi dəstəkləyir və 1 bayta 4 piksel saxlayır, ən soldakı piksel iki ən əhəmiyyətli bitdə olur. Hər bir piksel dəyəri 4 rəngə qədər cədvəldə 2 bitlik indeksdir.

* Piksel başına 4 bit (4bpp) formatı 16 fərqli rəngi dəstəkləyir və 1 bayta 2 piksel saxlayır, ən soldakı piksel daha əhəmiyyətli nibbledə olur. Hər bir piksel dəyəri 16 rəngə qədər cədvəldə 4 bitlik indeksdir.

* Piksel başına 8 bit (8bpp) formatı 256 fərqli rəngi dəstəkləyir və 1 bayta 1 piksel saxlayır. Hər bayt 256 rəngə qədər cədvəlin indeksidir.

* Piksel başına 16 bit (16bpp) formatı 65536 fərqli rəngi dəstəkləyir və 2 baytlıq WORD üçün 1 piksel saxlayır. Hər bir SÖZ pikselin alfa, qırmızı, yaşıl və mavi nümunələrini müəyyən edə bilər.

* 24-bit piksel (24bpp) formatı 16.777.216 fərqli rəngi dəstəkləyir və 3 bayt üçün 1 piksel dəyərini saxlayır. Hər bir piksel dəyəri pikselin qırmızı, yaşıl və mavi nümunələrini müəyyən edir (RGBAX notasiyasında 8.8.8.0.0). Xüsusilə, sıra ilə: mavi, yaşıl və qırmızı (hər nümunə üçün 8 bit).

* Piksel başına 32 bit (32bpp) formatı 4,294,967,296 fərqli rəngi dəstəkləyir və 4 baytlıq DWORD üçün 1 piksel saxlayır. Hər bir DWORD pikselin alfa, qırmızı, yaşıl və mavi nümunələrini müəyyən edə bilər.


## İstinadlar ##

* [Windows MetaFile Format](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-wmf/4813e7fd-52d0-4f42-965f-228c8b7488d2)
* [BMP Fayl Formatı](https://en.wikipedia.org/wiki/BMP_file_format)


