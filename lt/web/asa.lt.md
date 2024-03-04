{
  "date": "2021-12-09",
  "keywords": [
"kaip",
".kaip",
"Dokumento formatas",
"Failo tipas",
"kas yra .asa failas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASA – ASP konfigūracijos failas",
  "description": "Sužinokite, kas yra ASA failas ir API, kurios gali kurti ir atidaryti ASA failus.",
  "linktitle": "ASA",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-as-lta"
}
},
  "lastmod": "2021-12-09"
}

## Kas yra ASA failas?

ASA failas yra konfigūracijos failas, sukurtas [ASP](/web/asp/)/ASP.NET projektams. Jame yra kintamųjų deklaracijos, yra ir funkcijos, kurios turi būti pasiekiamos visuotiniu programos lygiu. Visi projekto puslapiai gali pasiekti šiuos kintamuosius ir funkcijas, taip išvengiant reikalavimo juos perrašyti. Vienas iš tokių pavyzdžių yra Global.asa puslapis, kuris saugomas šakniniame kataloge, kad būtų pasiekiamas kitiems ASP svetainės puslapiams. Global.asa failai yra neprivalomi, bet jei naudojami, kiekviena programa gali turėti tik vieną Global.asa failą.

## ASA failo formatas – daugiau informacijos

ASA failai yra paprasto teksto failai su tokia informacija.

 * Paraiškos renginiai
 * Sesijos renginiai
 * \<object> deklaracijas
 * TypeLibrary deklaracijos
 * #include direktyva

## ASA failo pavyzdys

Global.asa failas gali atrodyti maždaug taip.

```
<script language="vbscript" runat="server">

sub Application_OnStart
'some code
end sub

sub Application_OnEnd
'some code
end sub

sub Session_OnStart
'some code
end sub

sub Session_OnEnd
'some code
end sub

</script>
```

## Nuorodos

* [ASP Global.asa failas – w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)


