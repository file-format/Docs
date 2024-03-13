{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MSG - Microsoft Outlook E-poçt Formatı",
  "description": "MSG fayl formatı və MSG faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "MSG",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-ms-azg"
}
},
  "lastmod": "2019-09-10"
}

## MSG faylı nədir?

MSG is a file format used by [Microsoft Outlook](https://products.office.com/en-us/outlook/email-and-calendar-software-microsoft-outlook?rtc#1) and Exchange to store email messages, contact, appointment, or other tasks. Such messages may contain one or more email fields, with the sender, recipient, subject, date, and message body, or contact information, appointment particulars, and one or more task specifications. The properties that constitute the Message object, including are also a part of the MSG file.  MSG file has headers, main message body, and hyperlinks as plain ASCII text. MSG files are also suitable with the programs that need Microsoft's Messaging Applications Programming Interface (MAPI).

## MSG Fayl Strukturu

CFB_3 formatı MSG faylının əsasını təşkil edir. Paradiqma qovluqlara və fayllara olduqca yaxın olan saxlama və axın konsepsiyalarına əsaslanır. Buna görə də birincidəki əsas fərq, mürəkkəb fayl adlanan fərqli bir faylda paketlənmiş bütün iyerarxiyadır. Obyektlər mesaj fayllarını təşkil edir və tək xassədən və ya onun kolleksiyalarından ibarətdir. Bu qabiliyyət tətbiqlərə mürəkkəb, strukturlaşdırılmış məlumatları bir faylda saxlamağı asanlaşdırır. Bu format həm də çoxlu yaddaşı müəyyən edir, hər bir yaddaş əsas komponent kimi Mesaj obyektini təmsil edir. Bu anbarlar həmin komponentin xassəsini təmsil edən bir sıra axınları ehtiva edir. Saxlama yuvası da mümkündür.

## Mapi Xüsusiyyətləri

.msg faylının yuxarı səviyyəsində saxlamalarda xassələri saxlayan axınlar var. Mülkiyyətləri aşağıdakı kimi təsnif etmək olar:

* Sabit uzunluq xüsusiyyətləri

* Dəyişən uzunluq xüsusiyyətləri

* Çox dəyərli xüsusiyyətlər


Kateqoriyadan asılı olmayaraq, mülk ya etiketlənmiş və ya adlandırılmışdır. Bununla belə, xəritələşdirmə yaddaşı ilə müəyyən edilən adlandırılmış xassələr üçün uyğun xəritələşdirmə məlumatı tələb olunur.

## Anbarlar

Yaddaşlar Mesaj obyektinin əsas komponentlərini təşkil edir. MSG fayl formatı aşağıdakı yaddaşları bildirir:

## Üst Səviyyəli Struktur

Mesaj obyekti MSG fayl formatının bütün yuxarı səviyyəsini təmsil edir. Alıcı və Qoşma obyektlərinin növündən, xassələrindən, sayından asılı olaraq, mesaj obyekti müvafiq .MSG faylında müxtəlif axın yaddaşına malik ola bilər.

### Digər Strukturlarla Münasibət

Msg fayl formatı digər strukturlarla aşağıdakı əlaqələrə malikdir:

* .msg-nin əsası Mürəkkəb Fayl İkili Fayl Formatıdır.

* Mesaj və Əlavə Obyekt Protokolu tərəfindən istifadə edilən xüsusiyyətlər bu format tərəfindən istifadə olunur.


## MSG Formatlarından qaçınmaq üçün ssenarilər

Mesaj obyekti .msg fayl sistemindən istifadə edən müştərilər və ya mesaj dükanları arasında paylaşıla bilər. Mesaj obyektinin .msg fayl formatında saxlanmasının uyğun olmadığı bir neçə hal var. Misal üçün:

* Böyük bir müstəqil arxivin saxlanması halında, baxışların daha dəqiq göstərilə biləcəyi tam xüsusiyyətli formatdan istifadə etmək daha yaxşıdır.

* Əgər qəbuledici naməlumdursa, formatın qəbuledici tərəf tərəfindən dəstəklənməməsi və özəl və ya aidiyyəti olmayan formatın çatdırılması mümkündür.


## MSG fayl nümunəsi

To get an idea of how a MSG file looks like, you can download a [sample MSG file](https://products.conholdate.app/viewer/view/mL7cmq6qYbcNG329P/sample-msg-file.msg) and open on your computer to view its contents.

## İstinadlar

* [[MS-OXMSG]: Outlook MSG Fayl Formatı](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)


