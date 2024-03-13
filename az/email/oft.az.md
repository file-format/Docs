{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OFT - Microsoft Outlook E-poçt Şablon Faylı",
  "description": "OFT fayl formatı və OFT faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "OFT",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-of-azt"
}
},
  "lastmod": "2019-09-10"
}

## OFT faylı nədir?

.oft uzantılı fayllar Microsoft Outlook istifadə edərək yaradılan şablon fayllardır. Mesaj şablonları üçün əvvəlcədən formatlaşdırılmış tərtibat daha sonra vaxta qənaət etmək üçün ümumi məlumatı olan e-poçtların göndərilməsi üçün istifadə olunur. Bu cür fayllar yeni e-poçt yaratmaq, lazımi məlumatları əlavə etmək və sonra Microsoft Outlook-dan Office Şablonu (.oft) kimi Saxla açılır menyusundan istifadə etməklə yaradıla bilər. İstifadəçilər OFT fayllarını iki dəfə klikləməklə aça bilər və o, həmin sistemdə əlaqəli proqramda açılacaq.

## OFT Fayl Strukturu ##

.OFT fayl formatı bazasında [MSG](/email/msg/) fayl formatından istifadə edir. Yeganə fərq, oft faylların CLSID_TEMPlatemessage ({0006F046-0000000000000000000046} olduğu kimi, MSG faylları CLSID_MailMessage ({00020d0B-0000000000-1000-0000000046}) kimi CLSID_Templatemessage ({0006F046-0000000000000046})

CFB_3 formatı MSG faylının əsasını təşkil edir. Paradiqma qovluqlara və fayllara olduqca yaxın olan saxlama və axın konsepsiyalarına əsaslanır. Buna görə də birincidəki əsas fərq, mürəkkəb fayl adlanan fərqli bir faylda paketlənmiş bütün iyerarxiyadır. Obyektlər mesaj fayllarını təşkil edir və tək xassədən və ya onun kolleksiyalarından ibarətdir. Bu qabiliyyət tətbiqlərə mürəkkəb, strukturlaşdırılmış məlumatları bir faylda saxlamağı asanlaşdırır. Bu format həm də çoxlu yaddaşı müəyyən edir, hər bir yaddaş əsas komponent kimi Mesaj obyektini təmsil edir. Bu anbarlar həmin komponentin xassəsini təmsil edən bir sıra axınları ehtiva edir. Saxlama yuvası da mümkündür.

### OFT Xüsusiyyətləri

.msg faylının yuxarı səviyyəsində saxlamalarda xassələri saxlayan axınlar var. Mülkiyyətləri aşağıdakı kimi təsnif etmək olar:

* Sabit uzunluq xüsusiyyətləri

* Dəyişən uzunluq xüsusiyyətləri

* Çox dəyərli xüsusiyyətlər


Kateqoriyadan asılı olmayaraq, mülk ya etiketlənmiş və ya adlandırılmışdır. Bununla belə, xəritələşdirmə yaddaşı ilə müəyyən edilən adlandırılmış xassələr üçün uyğun xəritələşdirmə məlumatı tələb olunur.

### OFT Yaddaşlar

Yaddaşlar Mesaj obyektinin əsas komponentlərini təşkil edir. MSG fayl formatı aşağıdakı saxlama yerlərini bildirir:

### Yüksək Səviyyəli Struktur

Mesaj obyekti Msg fayl formatının bütün yuxarı səviyyəsini təmsil edir. Alıcı və Qoşma obyektlərinin növündən, xassələrindən, sayından asılı olaraq, mesaj obyekti müvafiq .MSG faylında müxtəlif axın yaddaşına malik ola bilər.

#### Digər strukturlarla əlaqə

MSG/OFT fayl formatı digər strukturlarla aşağıdakı əlaqələrə malikdir:

* .msg-nin əsası Mürəkkəb Fayl İkili Fayl Formatıdır.

* Mesaj və Əlavə Obyekt Protokolu tərəfindən istifadə edilən xüsusiyyətlər bu format tərəfindən istifadə olunur.


## İstinadlar

* [[MS-OXMSG]: Outlook MSG Fayl Formatı](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)


