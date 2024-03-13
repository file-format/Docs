{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TNEF",
  "description": "TNEF faylları yarada və aça bilən TNEF fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "TNEF",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-tne-azf"
}
},
  "lastmod": "2019-09-10"
}

## TNEF faylı nədir?

Nəqliyyat Neytral Encapsulation Format (TNEF) Mesajlaşma Tətbiqi Proqramlaşdırma İnterfeysi (**MAPI**) əsasında e-poçt qoşmalarını əhatə etmək üçün Microsoft mülkiyyətidir. Microsoft Outlook və Microsoft Exchange Server TNEF-i tamamilə dəstəkləyir, eyni zamanda TNEF-i daha sonra MAPI-yə deşifrə edir və formatlanmış məktubları göstərir. TNEF kodlaşdırması olan e-poçt qoşmasında MIME tipli MS-TNEF var və winmail/win.dat kimi saxlanılır. Winmail .dat-dakı qoşma aşağıdakı məlumatları əhatə edir:


|Mesaj|OLE obyektləri|Outlook xüsusiyyətləri
---|---|---|
|<ul><li> Orijinal mesaj əlavələri</li><li> Orijinal formatlı versiya</li><li> şriftlər, mətn ölçüləri və mətn rəngləri</li></ul> |<ul><li> quraşdırılmış şəkillər</li><li> quraşdırılmış Office sənədləri</li></ul> |<ul><li> xüsusi formalar</li><li> səsvermə düymələri</li><li> görüş tələbləri</li></ul>


TNEF-i dəstəkləməyən digər e-poçt xidmətləri TNEF formatlı mesajlar üçün düz mətn təqdim edir. Outlook mesajın zəngin formatını TNEF fayllarına (OLE) və ya xüsusi Outlook xüsusiyyətlərinə (formalar, sorğu düymələri və konfrans sorğuları) daxil edir. Outlook e-poçt müştərisi daxilində açıq TNEF kodlamasına sanksiya tətbiq etmək mümkün deyil, lakin e-poçtun göndərilməsi üçün RTF formatının seçilməsi TNEF kodlamasını gizli şəkildə asanlaşdırır.

## TNEF fayl formatı

TNEF məlumat alqoritmi zəngin iyerarxik mesaj xüsusiyyətlərindən düzəldilmiş struktur yaradır. Bu yastı strukturlar daha sonra xüsusi xüsusiyyətlərdən ibarət serial məlumat axınını təmsil etmək üçün istifadə olunur.

Xüsusiyyətlərin qruplar halında baş verdiyi və ya bir neçə dəyərə malik olduğu bəzi hallarda, axın müəyyən məlumat uyğunlaşdırılmasını tətbiq etmək üçün saylar və dolğunluqları əhatə edə bilər. Bu alqoritmin istifadəsinin faydalı olduğu fərqli bir vəziyyət dəstəkləyici olmayan mesajlaşma mühitidir. Belə mühitlərdə zəngin mesaj xüsusiyyəti TNEF Yazıçısı tərəfindən serial məlumat axınına kodlanır. Bundan əlavə, əsas TNEF-ə aid olmayan xüsusiyyətlər ötürülmə zamanı əhatə oluna bilər. Bu kapsullaşdırılmış xassələr daha sonra müştəri tətbiqi üçün orijinal mesajın bütün xüsusiyyətlərinin mövcudluğunu təmin etmək üçün TNEF vasitəsilə deşifrə edilərək təqdim edilir.

TNEF-də bütün rəqəmsal məlumat növləri kiçik endiandır və onların ölçüsü bir baytdan böyükdür. Qeyri-az endian platformalarda bu rəqəmli dəyərlərin idarə edilməsi düzgün dəyərlər əldə etmək üçün müvafiq transformasiyaların həyata keçirilməsini tələb edir. Sətir dəyərləri [RFC5234] spesifikasiyalarına uyğun olaraq Artırılmış Backus-Naur Forması (ABNF) formatında təmsil olunur. Sətir null simvolu ilə başa çatdıqda, o da daxil edilir; məsələn, `worker@specimen.com %x00`.

{{< figure src="../TNEF.png" alt="TNEF fayl formatı" >}}

## TNEF Atributları və Emal qaydaları ##

TNEF-də məlumat axını köhnə versiya nömrəsi, imza, primitiv açar dəyəri və kod səhifəsini təmsil edən atributla başlayır. Bu kod səhifəsi kodlayıcı ANSI atributlarını və xassələrini qeyd etdikdə yaradılır. Bundan sonra, axın əvvəlcə mesaj atributlarının, sonra isə əlavə atributlarının düzüldüyü bir sıra atributlara çevrildi. Müxtəlif mesaj və əlavə xüsusiyyətləri attMsgProps, attAttachment və attRecipTable kimi xüsusi atributlarda var. TNEF axınında görünən atributlar mesaj xassələri ilə məşğul olmaq üçün lazım olan strukturu, mesaj xassələrini və çevrilmələri ehtiva edir. Hər bir atribut identifikatordan, atributun ölçüsündən və məlumatından, yoxlama məbləğindən və tətbiqinə uyğun səviyyədən ibarətdir.

## Protokollar və digər alqoritmlərlə əlaqə ##

Zəngin mesaj formatını göstərmək üçün zəif mexanizmə malik olan sistemlər nəqliyyat üçün TNEF məlumat alqoritminə ehtiyac duyur. Media tipli ms-TNEF istifadə edərək, alqoritmin çıxışı əlavə fayldan (winmail.dat) və [RFC2045]-də göstərilən MIME-nin əsas hissəsindən ibarətdir. Düz mətn mesajı mətni [MSDN-UAF] spesifikasiyasına uyğun olaraq UUENCODE istifadə edərək ötürülür və bu mesaj mətni və ya alıcının sonunda deşifrə olunan ekvivalent metod. Bundan əlavə, TNEF mesaj məlumatlarını SMTP, POP3, IMAP4 və RFC2045 standartına uyğun olaraq MIME inteqrasiyası kimi müxtəlif internet protokollarından istifadə edərək ötürə bilər.

## Uyğunluq Bəyannaməsi ##

Sadə mesaj ötürülməsinə əlavə olaraq, mesaj siniflərindən istifadə etmək və nəqliyyat protokolunda orijinal dəstəyi olmayan əlavə funksiyaları dəstəkləmək üçün TNEF-in orijinal tətbiqi yaradılmalı idi. Bu proqram zəngin mesaj xassələrinin və müasir mesajlaşma müştərilərinin hazırda istifadə etdiyi adların ötürülməsi üçün daha da təkmilləşdirilmişdir. Orijinal tətbiqə uyğunluq üçün orijinal atribut sintaksisi saxlanılır və xüsusi atribut yeni mesaj xassələrini ayrıca saxlayır.

## İstinadlar

* [Nəqliyyat Neytral Encapsulation Format](https://en.wikipedia.org/wiki/Transport_Neutral_Encapsulation_Format)

* [Exchange Server-də e-poçt ünvanları və ünvan kitabları](https://learn.microsoft.com/en-us/exchange/email-addresses-and-address-books/email-addresses-and-address-books?view# exchserver-2019)

* [[MS-OXTNEF]: Nəqliyyat Neytral Kapsülləmə Format (TNEF) Məlumat Alqoritmi](https://msdn.microsoft.com/en-us/library/cc425498(v#exchg.80).aspx)


