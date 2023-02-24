{
  "date" : "2021-02-01",
  "keywords" :[ "usdz", "usdz-fil", "usdz-filformat", "filformat", "3d","usdz-filnedladdning"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USDZ - Universal Scene Description ZIP Format",
  "description":"Läs mer om USDZ-filformat och API:er som kan öppna och skapa USDZ-filer.",
  "linktitle" : "USDZ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## Vad är en USDZ fil?

En fil med .usdz är ett okomprimerat och okrypterat ZIP-arkiv för filformatet [USD](/sv/3d/usd/) (Universal Scene Description) som innehåller och proxyservrar för filer av andra format (som texturer och animationer) inbäddade i arkivet och kör dem direkt med USD-körtiden utan att behöva packa upp. USDZ-filer är paket vars design är baserad på den nya abstraktionen på Ar-nivå av ett paket. Usdz registrerades hos IANA och har medietypnamnet på modellen och undertypsnamnet vnd.usd+zip och dess detaljer finns som på [IANA-registreringssidan](https://www.iana.org/assignments/media-types/model/vnd.usdz+zip).

## USDZ filformat

USDZ-filer är baserade på ZIP-filformatet som arkiverar enskilda filer i sin behållare. Detta gör det möjligt för mottagaren att bara packa upp innehållet och använda de vanliga USD-scenbeskrivningsfilerna för att arbeta med och inspektera. Nästan alla operativsystem tillhandahåller inbyggt stöd för ZIP-filformat och att välja detta arkiveringsformat framför alla anpassade metoder gör det enkelt för USDZ-filer att vara användbara som ett enkelt transportprotokoll.

### ZIP-begränsningar

Filformatet USDZ använder ZIP-filformatet utan någon "komprimering" och "kryptering". Detta var designat för att uppfylla två krav:

* För ett paket som redan laddats in i minnet eller som en enda fil på disken, är API:erna tillgängliga i USD för åtkomst till data som finns i bilden
* Det borde inte finnas något behov av att extrahera filer till skiva eller tilldela mer höglagring

Med USDZ uppfylls båda dessa krav eftersom de flesta bildformaten i sig tillåter interna komprimeringsscheman, vilket resulterar i kompakt filstorlek.

### Layoutkrav

USDZ-paket kräver layouten av filer i paketet är att data för varje fil ska börja med en multipel av 64 byte från början av paketet. Paketet bör dock börja med en inbyggd [USD](/sv/3d/usd/)-fil i händelse av att paketet riktas med en enkel referens. I ett sådant fall kallas denna första USD-fil som standardskiktet. Kunder som vill leverera "streambart innehåll" kanske också vill överväga andra layoutbegränsningar.

## Ladda ner USDZ-fil
Eftersom usdz-filerna är packade med andra högkvalitativa bilder och usd-filer kan de uppta större disklagring. Här kan du hitta en enkel och mindre USDZ-exempelfil för nedladdning:

- [Sample.usdz](../sample.usdz)

## Referenser

* [USDZ filformatspecifikationer](https://graphics.pixar.com/usd/docs/Usdz-File-Format-Specification.html)
