{
  "date" : "2021-06-16",
  "keywords" :[ "LZH", "Komprimovaný", "Soubor", "Rozšíření", "Formát souboru", "Lempel-Ziv", "Haruyasu", "LHA" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru LZH",
  "description":"Další informace o formátu souborů LZH a rozhraních API, která mohou vytvářet a otevírat soubory LZH.",
  "linktitle" : "LZH",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## Co je soubor LZH? ##

Soubor s příponou .lzh a .lha se obvykle týká formátu souboru komprimovaného archivu. Tento formát souboru je stejný jako u jiných formátů komprese souborů, jako je [ZIP](/cs/compression/zip/), [RAR](/cs/compression/rar/) atd. Hlavním účelem těchto formátů souborů je zmenšit velikost formát pro snadné odesílání a také pro jejich uchování v komprimované podobě. V porovnání s jinými západními společnostmi jsou soubory LZH velmi populární v Japonsku a obvykle se používají pro kompresi dat videoher. Doplněk LZH pro Windows 7 je zabudován do japonské verze Windows 7. Společnost Microsoft poprvé vydala doplněk Microsoft Compressed (LZH) Folder Add-on pro japonskou verzi systému Windows XP. Tento formát souboru je implementován s kompresními ustanoveními a funkcemi používanými algoritmem Lempel-Ziv a Haruyasu

## Specifikace LZH ##

Metoda komprese archivu LZH je zobrazena jako pětibajtový textový řetězec, například -lz1-. Jedná se o třetí až sedmý bajt v komprimovaném souboru.

|Specifikace|Popis|
---|---|
|Prodloužení | .lzh, .lha|
|Typ média| application/x-lzh-compressed|
|Kód typu| "LHA_" (LHA-PROSTOR)|
|UTI| veřejný.archiv.lha|
|Vyvinul| Haruyasu Yoshizaki (Yoshi)|
|Typ| Komprese|
|Rozšířeno z| LArc|

## Problémy s otevřením souboru LZH ##

Následuje několik problémů, které mohou způsobit špatné fungování formátu souboru LZH:
  

* Soubor může být poškozen. Chcete-li tento problém vyřešit, stáhněte soubor znovu nebo požádejte odesílatele o opětovné zaslání souboru
* Druhým důvodem je infikovaný soubor v tomto případě soubor řádně prohledejte
* Nesprávné odkazy na soubor LZH
* Odstranění popisu LZH
* Nedostatek hardwarových zdrojů
* Zastaralé ovladače zařízení

## Reference ##

* [LZH - By Wikipedia](https://en.wikipedia.org/wiki/LHA_(file_format))
