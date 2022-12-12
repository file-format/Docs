{
  "date" : "2021-03-08",
  "keywords" :[ "RB", "zařízení eBook Rocket společnosti Nuvo Media", "soubor", "rozšíření", "formát", "elektronická kniha" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souboru RB pro zařízení Nuvo Media Rocket eBook a rozhraní API, která mohou vytvářet a otevírat soubory RB.",
  "title" :"RB - Rocket eBook File",
  "linktitle" : "RB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-08"
}

## Co je soubor RB?

Soubor s příponou .rb obsahuje obsah eKnihy Rocket. Rocket eBook je ve skutečnosti zařízení vyrobené společností Nuvo Media; vydali toto zařízení v roce 1998. Rocket eBook je sice schopen zobrazovat obrázky, ale pouze v černobílém zobrazení. Má obrazovku s rozlišením 106 dpi nebo 480 x 320 pixelů na 4,5 x 3palcové dotykové obrazovce. Elektronická kniha Rocket se připojuje k počítači prostřednictvím připojení sériového portu pro stahování elektronických knih ve formátu RB. Soubory RB jsou schopny používat DRM, ale tato technologie se v moderních elektronických knihách nepoužívá. Soubor RB obvykle obsahuje soubor HTML s obrázky a soubor pseudo-OPF se všemi metadaty (.info).

## Technická specifikace formátu souboru RB ##

V prvních 4 bajtech souboru se objeví magické číslo (v hexanech): B0 0C B0 0C.

Zdá se, že další dva bajty jsou číslo verze, například „02 00“, což znamená hlavní verzi 2 a vedlejší verzi 0.

Další čtyři bajty obsahují text „NUVO“, po kterém následují 4 bajty 00h.

Další 4 bajty je datum, kdy byla kniha vytvořena, zakódováno jako int16. Tím se dostáváme na offset 0Eh. Stará verze ORocketLibrary zakódovala plnou hodnotu roku (tj. 1999 byl „CF 07“, 2000 byl „D0 07“). V nejnovější verzi je tm_year uložen doslovně, tj. 100 pro rok 2000 ("64 00"). Po roce následuje int8 představující 1 relativní číslo měsíce a int8 představující den v měsíci.

Dalších 6 bajtů je 00h. Pro nastavení času mohou být vyhrazeny.

Absolutní offset "Table of Contents" je obsažen v int32 na offsetu 18h.

Poté následuje int32 obsahující délku souboru .rb. To se používá k určení, zda jsou soubory úplné nebo ne.

Zdá se, že celý tento kus bajtů (20 h až 128 h) potřebuje pouze titul, který je zašifrován. V nešifrovaných titulech jsou vždy nulové.

Ve většině případů následuje obsah (odsazení 128). Začíná int32 počtem položek „stránek“ (sekce souboru .rb) v ToC. Každá položka se skládá z názvu (vyplněno nulami na 32 bajtů), za kterým následují 3 int32: délka datového segmentu, pozice v souboru .rb a příznak pro tuto položku. K dnešnímu dni jsou známé hodnoty: 1 (zašifrováno), 2 (informační stránka) a 8 (vypuštěno). Jména jsou všechna přizpůsobena podle potřeby, aby bylo zajištěno, že jsou jedinečná.

## Reference

* [E-Reader – By MobileRead](https://en.wikipedia.org/wiki/E-reader)

