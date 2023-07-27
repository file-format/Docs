{
  "date" : "2019-10-11",
  "keywords" :[ "u3d fil", "u3d filformat", "vad är en u3d fil", "fil", "u3d exempel", "u3d filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"U3D - Universal 3D File Format",
  "description":"Läs mer om U3D-filformat och API:er som kan öppna och skapa U3D-filer.",
  "linktitle" : "U3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en U3D fil?

**U3D** (Universal 3D) är ett komprimerat filformat och datastruktur för 3D-datorgrafik. Den innehåller 3D-modellinformation som triangelnät, belysning, skuggning, rörelsedata, linjer och punkter med färg och struktur. Formatet accepterades som[ ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) standard i augusti 2005. 3D [PDF](/sv/pdf/) dokument stöder U3D objekt som bäddas in och kan visas i Adobe Reader (version 7 och senare).

U3D-formatet utvecklades med syftet att etablera en universell standard för tredimensionell datalagring och utbyte. Formatet finner dock sin huvudsakliga användning i kodning för 3D PDF snarare än att användas som ett utbytesformat. Acrobat 3D konverterar en 3D-filtyp som stöds till antingen U3D eller PRC vid konvertering till PDF.

## U3D filformat

U3D-filer är i binärt filformat som genomgick fyra utgåvor enligt beskrivningen av referensdokumentet [ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/), vilket resulterade i uppdatering av specifikationerna med varje upplaga. PDF-filstandarden ISO-32000 accepterar U3D som tillåten anteckning och multimediatyp.

Den första utgåvan av U3D var fokuserad på nyckelrepresentationerna av 3D-grafikegenskaper som geometri, färg, texturer, belysning, ben och transformationsbaserad animation. Den andra och tredje utgåvan korrigerade vissa fel i den första utgåvan, där tredje versionen var den vanligaste typen i industriprogramvara. Den fjärde upplagan ger definitioner för primitiver av högre ordning (krökta ytor). [U3D-specifikationer](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) finns tillgängliga online för användarreferens på ECMA:s webbplats.

### Datatyper i U3D-filer

Den binära filen kommer att innehålla följande typer: U8, U16, U32, U64, I16, I32, F32, F64 och String.

* U8 : Ett 8-bitars heltal utan tecken
* U16 : Ett 16 bitars heltal utan tecken
* U32 : Ett 32-bitars heltal utan tecken
* U64 : Ett 64-bitars heltal utan tecken
* I16 : Ett 16-bitars heltal med tecken
* F32: En IEEE enkel precisionsflottör.
* F64: En IEEE dubbel precisionsflytare.
* Sträng: Strängar i en U3D-fil börjar med ett osignerat 16-bitars heltal som definierar den totala längden på tecknen i strängen. Strängar behandlas alltid som skiftlägeskänsliga.

## U3D-filstruktur

En U3D-fil innehåller en sekvens av block. Det finns 3 olika typer av ett block i varje U3D-fil.

* Filhuvudblock
* Deklarationsblock
* Fortsättningsblock

Laddaren bestämmer slutet på ett block om data i det blocket inte krävs eller om en avkodare för den blocktypen inte är tillgänglig.

{{< figure src="../u3d.png" alt="U3D filformat" >}}

### Filhuvudblock
Ett filhuvudblock innehåller filinformation som används av den laddade för att bestämma hur filen ska läsas.

### Deklarationsblock

Deklarationsblocken innehåller information om objekten i filen. Objekten i ett deklarationsblock måste definieras.

### Fortsättningsblock

Ytterligare information för objekt som deklareras i ett deklarationsblock finns i fortsättningsblocket. Varje fortsättningsblock måste vara associerat med ett deklarationsblock.


## Referenser ##

* [U3D-filformat - Wikipedia](https://en.wikipedia.org/wiki/Universal_3D)
* [ECMA U3D filformatspecifikationer](https://www.ecma-international.org/publications/standards/Ecma-363.htm)

