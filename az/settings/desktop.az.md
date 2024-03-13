{
  "date": "2023-05-31",
  "keywords": [
"masaüstü faylı",
"masa üstü fayl nədir",
"masa üstü faylı nə ehtiva edir",
"Məsələn masa üstü faylı",
"masa üstü faylı necə açmaq olar",
"masa üstü faylın formatı nədir",
"fayl",
"masaüstü fayl uzantısı",
"uzadılması"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "DESKTOP Fayl Format - Masaüstü Giriş Faylı",
  "description": "DESKTOP faylları yarada və aça bilən DESKTOP formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "DESKTOP",
  "menu": {
    "docs": {
      "identifier": "settings-desktop-az",
      "parent": "settings"
}
},
  "lastmod": "2023-05-31"
}

## DESKTOP faylı nədir?

.desktop faylı proqram qısayollarını və işəsalma qurğularını müəyyən etmək üçün Linux iş masası mühitləri tərəfindən istifadə edilən konfiqurasiya faylıdır. O, proqramın adı, simvolu, icra əmri və digər xassələri kimi metadata təqdim edir. Bu fayllar adətən Linux əsaslı sistemlərdə proqram menyularında, masa üstü işəsalma qurğularında və ya panellərdə qısa yollar yaratmaq üçün istifadə olunur.

## DESKTOP faylında nə var?

.desktop faylı xüsusi formata uyğundur və bir neçə əsas sahəni ehtiva edir:

- **[Desktop Entry]:** Bu, .desktop faylı üçün əsas bölmə başlığıdır.
- **Ad:** Tətbiqin adını müəyyən edir.
- **Comment:** Provides brief description or comment about application.
- **Exec:** Proqramı işə salarkən yerinə yetiriləcək əmri müəyyənləşdirir.
- **İkon:** Tətbiqlə əlaqəli ikon faylına gedən yolu müəyyən edir.
- **Terminal:** Proqramın terminal pəncərəsində işə salınıb-çalışdırılmamasını müəyyən edir.
- **Növ:** Tətbiq və ya Link kimi giriş növünü müəyyən edir.
- **Categories:** Specifies categories or groups under which the application should be displayed in the menu.
- **StartupNotify:** İş masası mühitinin tətbiq üçün başlanğıc bildirişinin göstərilib-göstərilmədiyini müəyyən edir.
- **NoDisplay:** Specifies whether application should be hidden from menus.
- ** Fəaliyyətlər:** Müəyyən bir faylın açılması kimi tətbiqdə yerinə yetirilə bilən əlavə hərəkətləri müəyyənləşdirir.

## Nümunə DESKTOP faylı

Burada MyTextEditor adlı uydurma mətn redaktoru üçün .desktop faylının nümunəsi verilmişdir:

```
[Desktop Entry]
Name=MyTextEditor
Comment=A simple text editor
Exec=mytexteditor %F
Icon=/path/to/icon.png
Terminal=false
Type=Application
Categories=TextEditor;Utility;
StartupNotify=true
NoDisplay=false
Actions=OpenNewWindow;OpenExistingFile;

[Desktop Action OpenNewWindow]
Name=Open New Window
Exec=mytexteditor

[Desktop Action OpenExistingFile]
Name=Open Existing File
Exec=mytexteditor %U
```

Bu nümunədə, .desktop faylı əlaqəli xüsusiyyətləri ilə MyTextEditor proqramını müəyyən edir. O, həmçinin proqram başlatma qurğusunun kontekst menyusundan daxil olmaq mümkün olan Yeni Pəncərəni Aç və Mövcud Faylı Aç adlı iki əlavə hərəkəti ehtiva edir.

.desktop faylını `/usr/share/applications` və ya `~/.local/share/applications` kimi xüsusi qovluqlara yerləşdirməklə, iş masası mühiti onu tanıyacaq və müvafiq olaraq menyularda proqramı göstərəcək və ya onun işə salınmasına icazə verəcək. iş masası.

## DESKTOP faylını necə açmaq olar?

Bir neçə proqram proqramı .desktop fayllarını aça və idarə edə bilər. Bu proqramlar adətən fayl menecerləri və ya Linux əsaslı sistemlərdə iş masası mühitləridir. Budur bəzi nümunələr:

- **Nautilus (Fayllar):** GNOME iş masası mühiti üçün standart fayl meneceri.
- **Nemo:** Cinnamon iş masası mühiti üçün fayl meneceri.
- **Dolfin:** KDE Plazma iş masası mühiti üçün standart fayl meneceri.
- **Thunar:** Xfce iş masası mühiti üçün standart fayl meneceri.
- **KDE Menyu Redaktoru:** .desktop fayllarına baxmaq və redaktə etməyə imkan verən KDE Plazma iş masası mühitinə xas alət.

Bu fayl menecerləri və iş masası mühitləri .desktop fayllarını idarə etmək üçün qrafik interfeys təmin edir. Onlar sizə .desktop fayllarının xassələrinə baxmaq və redaktə etmək, proqram işə salmaq və proqram menyularında və ya iş masasında qısa yolları təşkil etmək imkanı verir.

.desktop faylları düz mətn fayllarıdır, ona görə də siz onları seçdiyiniz mətn redaktoru ilə aça və redaktə edə bilərsiniz. Quraşdırılmış proqramlar siyahısından mətn redaktorunu seçmək üçün sadəcə olaraq .desktop faylına sağ klikləyin və Birlikdə aç və ya Başqa proqramla aç seçin.

## DESKTOP faylının formatı nədir?

.desktop fayl formatı xüsusi struktur və formata uyğundur. Bu, bölmələrə təşkil edilmiş açar-dəyər cütləri dəsti olan düz mətn faylıdır. Budur formata ümumi baxış:

- **Bölmə Başlıqları:** Hər bölmə kvadrat mötərizədə ([]) alınmış başlıq ilə başlayır. Əsas bölmə adətən proqram və ya başlatma üçün əsas metadatadan ibarət olan [Masaüstü Girişi] adlanır.
- **Açar-dəyər cütləri:** Hər bölmədə siz açar-dəyər cütlərindən istifadə edərək xassələri müəyyənləşdirirsiniz. Format Açar = Dəyərdir. Açar əmlakı müəyyənləşdirir və dəyər müvafiq məlumatları təqdim edir.
- **Əmlak Sintaksisi:** Əmlak dəyərləri sətirlər, boolean dəyərlər, fayl yolları və ya siyahılar daxil olmaqla müxtəlif növ ola bilər. Hər bir əmlak dəyərinin formatı onun növündən asılıdır.
- **Şərhlər:** Siz '#' simvolundan istifadə edərək şərhləri .desktop faylına daxil edə bilərsiniz. Xəttdə '#' işarəsindən sonra gələn hər şey şərh hesab olunur və nəzərə alınmır.

## İstinadlar
* [Masaüstü Giriş Faylları](https://www.baeldung.com/linux/desktop-entry-files)


