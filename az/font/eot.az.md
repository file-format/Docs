{
  "date": "2020-08-20",
  "keywords": [
"eot faylı",
"eot fayl formatı",
"eot faylı nədir",
"fayl",
"eot misal",
"eot fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EOT - TrueType Şrift Fayl Formatı",
  "description": "EOT faylları yaratmaq və açmaq üçün EOT Fayl Format və API haqqında məlumat əldə edin.",
  "linktitle": "EOT",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-eo-azt"
}
},
  "lastmod": "2020-10-21"
}

## EOT faylı nədir?

.eot uzantılı fayl sənədə daxil edilmiş OpenType şriftdir. Bunlar əsasən veb səhifə kimi veb fayllarında istifadə olunur. O, Microsoft tərəfindən yaradılmışdır və PowerPoint təqdimatı [.pps](/presentation/pps/) faylı daxil olmaqla Microsoft Məhsulları tərəfindən dəstəklənir. Fayl əsas istifadə üçün deyil və bir növ əsas sənəd və ya veb səhifə ilə müşayiət olunan sənəddir. OTF şriftlərinə bənzər olaraq, EOT qliflər üçün həm Postscript, həm də TrueType konturlarını dəstəkləyir. EOT faylları LZ sıxılması ilə sıxıldığı üçün ölçüsü daha kiçikdir. EOT mövcud TTF/OTF şriftlərindən şrift yaratmaq üçün Microsoft alətindən istifadə edir.

## Qısa tarix

EOT şrifti 2007-ci ildə CSS3-ün bir hissəsi kimi W3C-yə təqdim edilmişdir, lakin onun rədd edilməsinə səbəb onun daimi olaraq uzaq sistemdə quraşdırılması tələbləri olmuşdur. 2008-ci ilin martında yenidən təqdim edildi, lakin W3C nəticədə o zaman standartlaşdırılan [Web Font Format](/font/woff/) (WOFF) seçdi.

## EOT fayl formatı

EOT fayl formatı təfərrüatları [W3 submission page](https://www.w3.org/Submission/EOT/#FileFormat) saytında tapıla bilər və bu şrift formatının istifadə etdiyi strukturu işləyib hazırlayır. EOT, hte şrift adı və dəstəklənən simvollar haqqında kifayət qədər əsas məlumat verən vahid EMBEDDEDFONT strukturundan ibarətdir. Bu məlumatın qablaşdırılması İstifadəçi Agentlərinə imkan verir ki, əgər şrift artıq maşında varsa, onu qablaşdırmadan çıxarmaq, açmaq və ya quraşdırmaqdan çəkinsin.

### EMBEDDEDFONT Strukturu
EMBEDDEDFONT strukturu hər bir revizyonla strukturun sonunda əlavə məlumatların əlavə edilməsi ilə üç reviziyadan keçmişdir. EMBEDDEDFONT strukturunun son revizyonu aşağıda göstərildiyi kimidir.

|Məlumat Tipi|Giriş Adı|Təsvir|
---|---|---|
|unsigned long|EOTSize|Baytlarla ümumi struktur uzunluğu (sətir və şrift məlumatları daxil olmaqla)|
|unsigned long|FontDataSize|OpenType şriftinin (FontData) baytla uzunluğu|
|unsigned long|Versiya|Bu formatın versiya nömrəsi - 0x00020002|
|imzasız uzun|Bayraqlar|Emal Bayraqları|
|bayt[10]|FontPANOSE|Bu şrift üçün PANOSE dəyəri - Baxın: https://learn.microsoft.com/en-us/typography/opentype/spec/os2#pan|
|bayt|Charset|Windows-da bu, TEXTMETRIC.tmCharSet-dən götürülüb. Bu dəyər şriftin simvol dəstini təyin edir. DEFAULT_CHARSET (0x01) üstünlük olmadığını göstərir. - Baxın: https://learn.microsoft.com/en-us/windows/win32/api/wingdi/ns-wingdi-textmetrica|
|bayt|İtalik|İTALIC üçün bit OS/2.fsSelection-da təyin edilibsə, dəyər 0x01 olacaq - Baxın: https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fss|
|unsigned long|Çəki|Bu şrift üçün çəki dəyəri - Baxın: https://learn.microsoft.com/en-us/typography/opentype/spec/os2#wtc|
|unsigned short|fsType|Yerləşdirmə icazələri haqqında məlumat verən bayraqları yazın - Baxın: https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fst|
|imzasız qısa|MagicNumber|EOT faylı üçün sehrli nömrə - 0x504C. Məlumatların pozulmasını yoxlamaq üçün istifadə olunur.|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1 (bit 0-31) - Baxın: https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange2|os/2.UnicodeRange2 (bit 32-63) - Baxın: https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange3|os/2.UnicodeRange3 (bit 64-95) - Baxın: https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (bit 96-127) - Baxın: https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|CodePageRange1|CodePageRange1 (bit 0-31) - Bax https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|unsigned long|CodePageRange2|CodePageRange2 (bit 32-63) - Bax https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|imzasız uzun|CheckSumAdjustment|head.CheckSumAdjustment - Bax https://learn.microsoft.com/en-us/typography/opentype/spec/head|
|unsigned long|Reserved1|Reserved - 0 olmalıdır|
|unsigned long|Reserved2|Reserved - 0 olmalıdır|
|unsigned long|Reserved3|Reserved - 0 olmalıdır|
|unsigned long|Reserved4|Reserved - 0 olmalıdır|
|unsigned short|Padding1|Uzun düzənliyi qorumaq üçün doldurma. Doldurma dəyəri həmişə 0x0000.|-a təyin edilməlidir
|imzasız qısa|FamilyNameSize|FamilyName massivi tərəfindən istifadə edilən baytların sayı|
|bayt|FamilyName[FamilyNameSize]|FamilyNameSize baytlarının uzunluğunda UTF-16 simvol massivi. Bu, şriftin ad cədvəlində tapılan İngilis dili Font Ailəsi sətridir (ad ID = 1) - Baxın: https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding2|Doldurma dəyəri həmişə 0x0000 olaraq təyin edilməlidir.|
|unsigned short|StyleNameSize|StyleName tərəfindən istifadə edilən baytların sayı|
|bayt|StyleName[StyleNameSize]|StilNameSize baytlarının uzunluğunda UTF-16 simvol massivi. Bu, şriftin ad cədvəlində tapılan İngilis dili Şrift Alt ailəsi sətridir (ad ID = 2) - Baxın: https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding3|Doldurma dəyəri həmişə 0x0000 olaraq təyin edilməlidir.|
|imzasız qısa|VersionNameSize|VersionName tərəfindən istifadə edilən baytların sayı|
|bayt|VersionName[VersionNameSize]|VersionNameSize bayt uzunluğunda UTF-16 simvol massivi. Bu, şriftin ad cədvəlində tapılan ingilis dili versiyasıdır (ad ID = 5) - Baxın: https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding4|Doldurma dəyəri həmişə 0x0000 olaraq təyin edilməlidir.|
|unsigned short|FullNameSize|TamAd tərəfindən istifadə edilən baytların sayı|
|bayt|FullName[FullNameSize]|FullNameSize bayt uzunluğunda UTF-16 simvol massivi. Bu, şriftin ad cədvəlində tapılan ingilis dilində tam ad sətridir (ad ID = 4) - Baxın: https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding5|Doldurma dəyəri həmişə 0x0000 olaraq təyin edilməlidir.|
|unsigned short|RootStringSize|RootString massivi tərəfindən istifadə edilən baytların sayı|
|byte|RootString[RootStringSize]|RootStringSize baytlarının uzunluğu olan UTF-16 simvol massivi.|
|unsigned long|RootStringCheckSum|RootString CheckSum dəyəri. Aşağıda RootStringChecksum emal etmək üçün alqoritmə baxın.|
|unsigned long|EUDCCodePage|EUDC şrift dəstəyi üçün kod səhifəsi dəyəri lazımdır.|
|unsigned short|Padding6|Doldurma dəyəri həmişə 0x0000 olaraq təyin edilməlidir.|
|unsigned short|SignatureSize|İmza massivi tərəfindən istifadə olunan baytların sayı. Hazırda rezerv edilib və 0x0000.|-a təyin edilməlidir
|bayt|İmza[SignatureSize]|Hazırda qorunur. SignatureSize 0x0000 olarsa, bu massivin uzunluğu yoxdur.|
|unsigned long|EUDCFlags|EUDC şrifti üçün bayraqlar işlənir. Tipik dəyərlər TTEMBED_XORENCRYPTDATA və TTEMBED_TTCOMPRESSED ola bilər.|
|unsigned long|EUDCFontSize|İmza massivi tərəfindən istifadə olunan baytların sayı.|
|bayt|EUDCFontData[EUDCFontSize]|EUDC şrift məlumatları üçün istifadə olunan baytların sayı. EUDCFontSize 0x00000000 olarsa, bu massivin uzunluğu yoxdur.|
|bayt|FontData[FontDataSize]|Bu EOT faylı üçün şrift datası. Məlumat emal bayraqları ilə göstərildiyi kimi sıxılmış və ya XOR şifrələnmiş ola bilər.|

## İstinadlar

 * [EOT Fayl Formatı](https://www.w3.org/Submission/EOT/)
 * [Daxil edilmiş OpenType](https://en.wikipedia.org/wiki/Embedded_OpenType)
 * [Şrift Yerləşdirmə](https://en.wikipedia.org/wiki/Font_embedding)

