{
  "date": "2021-08-11",
  "keywords": [
"wim faylı",
"wim fayl formatı",
"wim faylı nədir",
"fayl",
"wim nümunəsi",
"wim fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "WIM fayl formatı və WIM faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "WIM - Windows Görüntü Format Faylı",
  "linktitle": "WIM",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-wi-azm"
}
},
  "lastmod": "2021-08-11"
}

## WIM faylı nədir?
.wim uzantıları olan fayllar ilk dəfə Windows Vista-da görüldü. WIM adətən Microsoft Windows Vista-da təqdim edilən fayl əsaslı təsvir formatına aiddir. Bu, bir disk şəklini müxtəlif kompüter platformalarında yerləşdirməyə imkan verir. WIM faylları əməliyyat sistemi şəklini yenidən yükləmədən yeniləmələr, sürücülər və komponentlər kimi faylları idarə etmək üçün istifadə olunur. AQ WIM faylı digər disk fayl formatlarına çox oxşar olan bir sıra faylları və əlaqəli metaməlumatları ehtiva edir.

## WIM fayl formatları
WIM fayl formatı VHD və ya IS kimi sektor əsaslı formatlara bənzəmir, əslində o, fayl əsaslıdır, yəni WIM-də əsas məlumat vahidi fayldır. Fayl əsaslı olmağın əsas üstünlüyü ondan ibarətdir ki, fayl sistemi ağacında bir neçə dəfə istinad edilən faylın bir instansiyalı saxlanması və hardware müstəqilliyi. Bu, müxtəlif faylların ayrı-ayrılıqda açılması və bağlanması xərclərini azaldır, çünki fayllar bir WIM-də saxlanılır. fayl. WIM faylları unikal adları və ya ədədi indeksləri ilə istinad edilən çoxsaylı disk şəkillərini saxlaya bilər.
### Sıxılma alqoritmləri üçün dəstək
WIM, azalan sürət və artan nisbətdə sıxılma alqoritmlərinin aşağıdakı ailələrini dəstəkləyir:
- XPRESS
- LZX
- LZMS
- Bərk sıxılma.
İlk üç ailə LZ77 əsaslıdır, bərk sıxılma isə WIMGAPI Windows 8 və DISM Windows 8.1-də LZMS ilə birlikdə təqdim edilmişdir.
### WIM fayl formatı üçün alətlər
Aşağıdakı alətlər adətən WIM fayl formatını dəstəkləyir:

- **ImageX**: Windows Şəkil Formatında Windows disk şəkillərini redaktə etmək, yaratmaq və yerləşdirmək üçün istifadə olunan komanda xətti aləti. Müvafiq WIMGAPI ilə yanaşı, pulsuz Windows Avtomatlaşdırılmış Quraşdırma Kitinin bir hissəsi kimi paylanır. Windows Vista ilə başlayaraq, Windows Quraşdırma Windows-u quraşdırmaq üçün WAIK API-dən istifadə edir.
- **DISM**: Windows 7 və Windows Server 2008 R2-də təqdim edilmiş alət, Windows quraşdırma təsvirində xidmətlə bağlı tapşırıqları yerinə yetirə bilər, istər onlayn şəkil, istərsə də qovluq və ya WIM faylı daxilində oflayn şəkil. bu alət şəkilləri quraşdırmaq və çıxarmaq, oflayn təsvirə cihaz drayverini əlavə etmək və oflayn təsvirdə quraşdırılmış cihaz sürücülərini sorğulamaq qabiliyyətinə malikdir.
 



## İstinadlar 

* [Windows Imaging Format - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/Windows_Imaging_Format)



