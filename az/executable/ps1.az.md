{
  "date" : "2024-03-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "PS1 Faylı - Windows PowerShell Cmdlet Faylı - .ps1 faylı nədir və onu necə açmaq olar?",
  "description" : "PS1 Windows PowerShell Cmdlet Faylı və onun necə açılacağını öyrənin.",
  "linktitle" : "PS1",
  "menu" : {
    "docs" : {
      "identifier" : "executable-ps1-az",
      "parent" : "executable"
}
},
  "lastmod" : "2024-03-08"
}

## PS1 faylı nədir?

PS1 faylında PowerShell skript kodu var. PowerShell, Microsoft-un əmr satırı qabığından və əlaqəli skript dilindən ibarət tapşırıqların avtomatlaşdırılması və konfiqurasiya idarəetmə çərçivəsidir.

PowerShell skriptinin .ps1 faylında necə görünə biləcəyinə dair sadə bir nümunə:

```
# This is a comment
Write-Host "Hello, World!"
```

Bu skript Salam, Dünya! icra edildikdə. PowerShell skriptlərində tapşırıqları avtomatlaşdırmaq, sistem konfiqurasiyalarını idarə etmək, sistem komponentləri ilə qarşılıqlı əlaqə yaratmaq və s. üçün müxtəlif əmrlər və məntiqlər ola bilər.

## PS1 Fayl Format - Ətraflı Məlumat

PS1 faylları .BAT və .CMD fayllarına bənzəyir, çünki onlar tapşırıqları avtomatlaşdırmaq və əmrləri yerinə yetirmək üçün istifadə olunur. Bununla belə, .BAT və .CMD faylları CMD.EXE və ya COMMAND.COM istifadə edərək Windows əmr sorğusunda icra edildiyi halda, PS1 faylları Microsoft tərəfindən hazırlanmış daha güclü və xüsusiyyətlərlə zəngin qabıq və skript dili olan Windows PowerShell-də icra olunur.

PowerShell ənənəvi əmr əmri ilə müqayisədə müxtəlif sistem komponentləri və xidmətləri ilə daha geniş imkanlar və inteqrasiya təklif edir. Bu, PS1 fayllarını Windows platformalarında daha təkmil skript, avtomatlaşdırma və sistem idarəetməsi tələb edən tapşırıqlar üçün xüsusilə faydalı edir.

## PS1 faylını necə açmaq olar?

**.ps1 faylını** (PowerShell skript faylı) açmaq və icra etmək üçün bu addımları yerinə yetirə bilərsiniz:

1. Fayl Explorer və ya hər hansı bir fayl menecerindən istifadə edərək kompüterinizdə PS1 faylını tapın.
1. Başlat menyusunda onu axtararaq və ya `Win + X` qısa yolundan istifadə edərək və Windows PowerShell seçərək PowerShell-i açın.
1. PS1 faylı defolt PowerShell qovluğunda deyilsə, faylın yerləşdiyi qovluğa getmək üçün `cd` əmrindən istifadə edin.
1. Sisteminizin icra siyasəti skriptlərin işləməsinə icazə vermirsə, `Set-ExecutionPolicy` əmrindən istifadə edərək onu dəyişdirin.
1. PowerShell pəncərəsində `.\filename.ps1` yazın (fayl adını PS1 faylınızın faktiki adı ilə əvəz edin) və skripti icra etmək üçün Enter düyməsini basın.

Siz həmçinin .ps1 faylının məzmununa baxmaq üçün Notepad, Notepad++, Visual Studio Code kimi mətn redaktorundan və ya seçdiyiniz hər hansı digər mətn redaktorundan istifadə edə bilərsiniz. Sadəcə olaraq faylın üzərinə sağ klikləyin, Birlikdə aç seçin və istədiyiniz mətn redaktorunu seçin.

## İstinadlar
* [PowerShell](https://en.wikipedia.org/wiki/PowerShell)


