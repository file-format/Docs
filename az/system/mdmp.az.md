{
  "date": "2022-08-19",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MDMP Faylı - Windows Minidump Fayl Formatı",
  "description": "MDMP fayl formatı və MDMP fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "MDMP",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-mdm-azp"
}
},
  "lastmod": "2022-08-19"
}

## MDMP faylı nədir?

MDMP faylı Microsoft Windows-da proqramın anormal şəkildə bağlanması və ya çökməsi zamanı yaradılan proqramın yaddaş zibilidir. O, qəzanın səbəbini aradan qaldırmaq üçün istifadə edilə bilən məlumat və məlumat zibillərini ehtiva edir. MDMP faylları Java, C++, .NET və başqaları kimi istənilən platforma tərəfindən yaradılmış proqramlarda tətbiq oluna bilər. MDMP ilə yanaşı,

MDMP fayllarını aça bilən proqramlara Microsoft Visual Studio Debugger daxildir.

## MDMP fayl formatı

MDMP faylları ikili fayllar kimi diskdə saxlanılır və Microsoft Visual Studio sazlayıcı ilə açıla bilər. Qəzanın səbəbini müəyyən etməyə kömək edəcək aşağıdakı məlumatları ehtiva edir.

 * Stop mesajının təfərrüatları, onun parametrləri və digər məlumatlar
 * Yüklənmiş sürücülərin siyahısı
 * İşini dayandıran prosessor üçün prosessor konteksti (PRCB).
 * Dayanmış proses üçün proses məlumatı və nüvə konteksti (EPROCESS).
 * Dayanan mövzu üçün məlumat və nüvə kontekstini (ETHREAD) emal edin
 * Dayanan mövzu üçün nüvə rejimli zəng yığını

Bu məlumat nə baş verdiyini öyrənməyə, problemi həll etməyə və yenidən baş verməsinin qarşısını almağa kömək edir.

### Minidumpı təhlil edin

Yaddaş boşaltma faylı yaratmaq üçün Windows yükləmə həcmində paging faylı tələb edir. Peyqinq faylı yükləmə həcmində yaradılmışdır və ölçüsü ən azı 2 meqabayt (MB) olmalıdır. Dump faylı proqram qəzaya uğradıqda yaradılır. İkinci problem olduqda, əvvəlkisi saxlanılarkən ikinci kiçik yaddaş boşaltma faylı yaradılır. Hər hansı üzərinə yazılmanın qarşısını almaq üçün dump faylının adı fərqlidir.

Windows bütün yaddaş boşaltma fayllarının siyahısını %SystemRoot%\Minidump qovluğunda saxlayır. Siz MDMP fayllarını aşağıdakı addımlarda sadalandığı kimi Visual Studio Debugger-də işlətməklə təhlil edə bilərsiniz.

## Visual Studio-da MDMP faylını necə aça bilərəm?

Visual Studio-da MDMP faylını açmaq üçün aşağıdakı addımlardan istifadə edilə bilər.

 * Visual Studio-da Fayl menyusundan Aç | seçin Crash Dump.
 * Açmaq istədiyiniz dump faylına keçin.
 * Aç seçin.

## İstinad

* [Qəza baş verərsə, Windows tərəfindən yaradılmış kiçik yaddaş boşaltma faylını necə oxumaq olar](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump -fayl)


