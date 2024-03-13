{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EML - E-poçt mesajı",
  "description": "EML faylları yarada və aça bilən EML fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "EML",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-em-azl"
}
},
  "lastmod": "2019-09-16"
}

## EML faylı nədir?

EML fayl formatı Outlook və digər müvafiq proqramlar vasitəsilə saxlanılan e-poçt mesajlarını təmsil edir. Demək olar ki, bütün e-poçt müştəriləri bu fayl formatını RFC-822 İnternet Mesaj Format Standartına uyğunluğu üçün dəstəkləyir. Microsoft Outlook EML mesaj növlərini açmaq üçün standart proqramdır. EML faylları həm diskdə saxlamaq, həm də rabitə protokollarından istifadə edərək alıcılara göndərmək üçün istifadə edilə bilər.

## EML-nin qısa tarixi

EML fayl formatının spesifikasiyası [RFC 822](https://www.ietf.org/rfc/rfc0822.txt) Standart Format üzrə mövcuddur. RFC-822-dən əvvəl, RFC-733 şəbəkə mesajlarının mübadiləsi qaydalarını 1982-ci ilə qədər idarə edirdi, birincisi ARPA standartlarını təyin etməklə yanal üçün təkmilləşdirmə kimi yaradılmışdır. Eyni zamanda, Microsoft öz e-poçt müştərisinin, yəni Outlook Express-in inkişafı üçün öz COM modullarını yaratdı. Microsoft açıq standartdan kənara çıxdıqda və e-poçtların yüksək strukturlaşdırılmış verilənlər bazası formatında saxlandığı [PST](/email/pst/) fayl formatını yaratdıqda, RFC-822 mülkiyyət formatı kimi müəyyən edilmək yolunu tutdu. Bu, e-poçtlar Microsoft Outlook-dan yönləndirilərkən Microsoft olmayan e-poçt müştərilərinin istifadəçiləri üçün problemlərlə nəticələndi.

2001-ci ildə 822 standartı MIME RFC-822 formatında EML mesajlarının yaradılması, oxunması və göndərilməsi üçün hazırda istifadə edilən 2822 - İnternet Mesaj Formatına çevrildiyi zaman idi.

## EML Fayl Formatının Xüsusiyyətləri

EML faylları iki fərqli bölmədən ibarətdir:

* **Başlıqlar** - Mesaj başlığı haqqında məlumat ehtiva edir

* **Mesaj Gövdəsi** - Mesaj məzmunu, daxil edilmiş şəkillər və qoşmalar daxil ola biləcək bir sıra məlumatları ehtiva edir


### Başlıq Məlumatı ###

EML faylı Başlıq məlumatından və isteğe bağlı olaraq mesaj gövdəsindən ibarətdir. EML-dəki hər başlıq sətirində iki nöqtə : ilə ayrılmış iki hissə var. Birincisi Başlıq Adı adlanır və iki nöqtədən sonra gələn başlıq gövdəsidir. Məsələn, belə başlıqlara aşağıdakılar daxildir:

* Göndərənin e-poçt ünvanı

* Alıcının e-poçt ünvanı

* E-poçtun mövzusu

* Mesajın vaxtı və tarixi möhürü


**Nümunə Başlıq**

```
From: <John@bmw.eml.light.com>

To: <Andy@fileformat.com>

Date: Thu, 8 Mar 2018 10:43:37 +0100

Subject: bmw eml light
```

### Mesaj Məqsədi ###

EML mesajı mətn, hiperlink və əlavələr şəklində e-poçtun əsas məlumatlarını ehtiva edir. E-poçt mətni sadə oxunaqlı mətndən ibarət ola bilər, lakin bu lazım deyil. Bu halda, mesaj gövdəsi boş ola bilər və ya kodlanmış qoşma məlumatlarını ehtiva edə bilər.

Mesaj mətninin məzmunu onun Məzmun Növü ilə təsvir olunur ki, bu da oxu proqramlarına məlumatı müvafiq formatlarda oxumağa imkan verir. O, əslində sənədin xarakterini və formatını təmsil edir. MIME növünün və ya məzmun növünün strukturu çox sadədir; o, bir növ və alt tipdən, '/' ilə ayrılmış iki sətirdən ibarətdir. Heç bir yerə icazə verilmir. Növ kateqoriyanı təmsil edir və diskret və ya çoxhissəli tip ola bilər. `Alt tip` hər bir növ üçün spesifikdir. Məzmun Tipi kateqoriyasına daxil olan növlərin siyahısı uzundur, lakin bəzi vacib məzmun növləri aşağıdakılardır:


|**Növ**|**Təsvir**|**Alt Növlərə Nümunə**
---|---|---|
|mətn|İnsan tərəfindən oxuna bilən formatı təmsil edir|mətn/düz, mətn/html, mətn/css, mətn/javascript
|şəkil|Videolar istisna olmaqla istənilən növ şəkli təmsil edir|şəkil/bmp, şəkil/png, şəkil/jpg, şəkil/gif
|audio|İstənilən audio fayl formatını təmsil edir|audio/mdi, audio/wav
|tətbiq|İstənilən növ ikili məlumatı təmsil edir|tətbiq/oktet-axın, application/vnd.mspowerpoint, application/xhtml+xml, application/xml, application/pdf

### Əlavənin EML Bədənində Təmsil edilməsi

EML gövdəsi tərkibində olan hər bir məzmun növü üçün sərhədləri ehtiva edir. Mesaj gövdəsindəki qoşma aşağıdakı nümunədə göstərildiyi kimi onun Məzmun Növü və Məzmun Yeri ilə müəyyən edilir:

Məzmun növü: mətn/düz; charset#windows-1252; ad#apple app store.txt
Məzmun-Dispozisiya: əlavə; fayl adı #apple app store.txt
Məzmun ötürülməsi-kodlaşdırma: base64
X-Qoşma-ID: f_jkhztmd02

Göründüyü kimi, əlavəyə təyin edilmiş Məzmun-Dispozisiya oxu proqramlarına əlavə fayl adı və köçürmə kodlaşdırması kimi əlavə məlumatlarını əldə etməyə imkan verir. Qoşma başlığı məlumatının ardınca oxunmalı olan kodlanmış qoşma məzmunu gəlir.

#### Əlavə kimi elektron cədvəl nümunəsi

Məzmun növü: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet; ad#english_spodr.xlsx
Məzmun-Dispozisiya: əlavə; fayl adı #english_spodr.xlsx
Məzmun ötürülməsi-kodlaşdırma: base64
X-Qoşma-Id: f_jkhztmd43

## EML faylını necə açmaq olar

EML fayllarını müxtəlif e-poçt proqramlarından istifadə edərək aça bilərsiniz, məsələn:

 * **macOS-da Apple Mail**
 * **Mozilla Thunderbird**
 * **Microsoft Outlook**

EML faylları düz mətn formatında saxlanılır və siz həmçinin bu EML fayllarını macOS-da **TextEdit** və Windows ƏS-də **Microsoft Notepad** kimi məşhur mətn redaktorları ilə aça bilərsiniz.

## EML faylını necə çevirmək olar

Siz Apple Mail və Microsoft Outlook kimi proqramlarla EML fayllarını bir neçə başqa formata çevirə bilərsiniz.

Məsələn, Microsoft Outlook EML faylını aşağıdakı formatlara çevirə bilər:

**[.MSG](/eml/msg/)** - Microsoft Outlook Mesaj Formatı
**[.PDF](/pdf/)** - Daşınan Sənəd Formatı

## İstinadlar

* [RFC 822](https://www.ietf.org/rfc/rfc0822.txt)


