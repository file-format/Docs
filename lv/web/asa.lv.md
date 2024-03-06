{
  "date": "2021-12-09",
  "keywords": [
"kā",
".kā",
"faila formātā",
"faila tips",
"kas ir .asa fails"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASA — ASP konfigurācijas fails",
  "description": "Uzziniet, kas ir ASA fails un API, kas var izveidot un atvērt ASA failus.",
  "linktitle": "ASA",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-as-lva"
}
},
  "lastmod": "2021-12-09"
}

## Kas ir ASA fails?

ASA fails ir konfigurācijas fails, kas izveidots [ASP](/web/asp/)/ASP.NET projektiem. Tas satur mainīgo lielumu deklarācijas, satur un funkcijas, kas ir paredzētas, lai lietojumprogrammā būtu pieejamas globālā līmenī. Visām projekta lapām var piekļūt šiem mainīgajiem lielumiem un funkcijām, tādējādi izvairoties no nepieciešamības tos pārrakstīt. Viens no šādiem piemēriem ir lapa Global.asa, kas tiek saglabāta saknes direktorijā, lai tai varētu piekļūt citām ASP vietņu lapām. Global.asa faili nav obligāti, taču, ja tie tiek izmantoti, katrai lietojumprogrammai var būt tikai viens Global.asa fails.

## ASA faila formāts — vairāk informācijas

ASA faili ir vienkārša teksta faili ar šādu informāciju.

 * Pieteikšanās pasākumi
 * Sesijas pasākumi
 * \<object> deklarācijas
 * TipsBibliotēkas deklarācijas
 * #include direktīva

## ASA faila piemērs

Global.asa fails varētu izskatīties apmēram šādi.

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

## Atsauces

* [ASP Global.asa fails — w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)


