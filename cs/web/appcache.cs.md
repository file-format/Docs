{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Soubor APPCACHE – formát souboru manifestu mezipaměti HTML5",
  "description" :"Zjistěte, co je soubor APPCACHE a rozhraní API, která mohou vytvářet a otevírat soubory APPCACHE.",
  "linktitle" : "APPCACHE",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## Co je soubor APPCACHE?

Soubor APPCACHE je textový soubor, který obsahuje seznam zdrojů, které mají prohlížeče uložit do mezipaměti pro offline přístup k webovým aplikacím. To je užitečné, když není k dispozici připojení k internetu. V takové situaci používá prohlížeč prostředky offline mezipaměti k poskytování přístupu k webovému obsahu. Soubor APPCACHE obsahuje webové zdroje, jako jsou obrázky (například **[PNG](/cs/image/png/)**, **[WEBP](/cs/image/webp/)** atd.), šablony stylů **([ CSS])(/cs/web/css/)** a soubory skriptů (jako jsou soubory Javascript **[JS](/cs/web/js/)**).

Mezi aplikace, které mohou **otevřít soubory APPCACHE**, patří webové prohlížeče, jako je Google Chrome, Safari a Firefox.

## Formát souboru APPCACHE – Další informace

Soubory APPCACHE jsou jednoduché textové soubory, které poskytují offline přístup k webovým stránkám pro spuštění bez připojení k internetu. Přítomnost APPCACHE označuje stránku jako dostupnou offline.

### Jak odkazovat na soubor APPCACHE?

Na vaší HTML stránce je soubor APPCACHE odkazován následovně.

```
<html manifest="example.appcache">
  ...
</html>
```

## Struktura souboru manifestu APPCACHE

Jednoduchý soubor manifestu APPCACHE vypadá následovně.

```
CACHE MANIFEST
index.html
stylesheet.css
images/logo.png
scripts/main.js
http://cdn.example.com/scripts/main.js
```

Toto je nejjednodušší příklad a mohou existovat i složitější struktury.

## Výhody APPCACHE Manifest

Použití mezipaměti poskytuje webovým aplikacím následující výhody.

1. Procházení offline – Rozhraní mezipaměti umožňuje koncovým uživatelům procházet celý váš web, když jsou offline
1. Rychlost - cache umožňuje vysokorychlostní přístup k offline obsahu přímo z disku
1. Přístupnost po celou dobu – V případě, že vaše stránky přestanou fungovat, budou mít uživatelé stále přístup k webovému obsahu a budou moci využívat offline prostředí

## Reference

* [Příručka pro začátečníky k manifestu AppCache](https://web.dev/appcache-beginner/)

