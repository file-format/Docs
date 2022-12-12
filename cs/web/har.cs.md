{
  "date" : "2021-07-08",
  "keywords" :["HAR", "Soubor", "Přípona", "Formát souboru", "Přípona souboru", "JSON", "Archivní soubor"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HAR - HTTP Archive File Format",
  "description" :"Váš průvodce formátem souboru, kde se dozvíte, co je soubor HAR a rozhraní API, která mohou vytvořit a otevřít soubor HAR.",
  "linktitle" : "HAR",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-08"
}

## Co je soubor HAR?

Soubor se souborem .har ([HTTP](/cs/web/http/) Archive) je archivní soubor HTTP, který ukládá data relací přenášených přes mnoho prohlížečů (jako je Chrome, Safari, IE, Firefox atd.) v [JSON] (/cs/web/json/) formát souboru. Data přenášená přes internet mezi serverem a klientem (v tomto případě prohlížečem uživatele) obsahují hlavičky HTTP požadavku a odpovědi, které jsou uloženy v souboru HAR. Dále obsahuje podrobné informace o údajích o výkonu webových stránek načtených v prohlížeči. Soubory HAR lze otevřít v libovolném textovém editoru, jako je Poznámkový blok na OS Microsoft Windows a TextEdit na Apple MacOS.

## Formát souboru HAR – Další informace

Soubory HAR ukládají informace o relaci v prostém textovém souboru pomocí oblíbeného formátu JSON. Specifikace pro formát souboru HAR byly vytvořeny skupinou Web Performance Group při World Web Consortium (W3C), ale nemohly být zveřejněny. Úspěšně však definoval archivní formát pro transakce HTTP.

Kromě sledování přenosu informací o požadavcích a odpovědích vývojáři používají soubory HAR k protokolování výkonu webového prohlížeče, pokud jde o rychlost načítání stránky, dobu načítání obsahu, načtený obsah, prováděné dotazy k získání odpovědi z prohlížeče a mnoho dalších .

## Proč používat soubory HAR?

Soubory HAR mohou být užitečné při zlepšování výkonu webu tím, že vyhodnocují dlouhé doby načítání, doby vykreslování stránky a doby odezvy. Soubory HAR lze analyzovat za účelem nalezení takových problémů a vyřešení jakýchkoli problémů s webem pro zlepšení výkonu.

## Jak vygenerovat soubor HAR?

Jak tedy vygenerovat soubor HAR? To záleží na tom, jaký typ prohlížeče používáte ke generování souboru HAR. V této příručce uvádíme postup pro prohlížeč Google Chrome. Metody pro generování souborů HAR pomocí Safari, Firefox atd. lze snadno vyhledat na internetu a následovat.

### Kroky ke generování souboru HAR pomocí Google Chrome

Následující kroky lze provést na webové stránce, kde se potýkají s problémy.

1. Otevřete webovou stránku v prohlížeči Google Chrome, na které k problému došlo.
1. Otevřete vývojářský nástroj (kontrola prvku).
1. Přejděte do levé části panelu a začněte nahrávat soubor. V této části je malé kulaté červené tlačítko.
1. Kliknutím na ikonu „Vymazat“ odstraníte všechny záznamy protokolu uložené v prohlížeči.
1. Chcete-li uložit požadovaný obsah, jak je uvedeno výše, klikněte pravým tlačítkem a klikněte na „Uložit jako soubor HAR“

## Reference

* [Formát souboru HAR – Wikipedie](https://en.wikipedia.org/wiki/HAR_(formát_souboru))

