{
  "date" : "2021-08-04",
  "keywords" :[ "mod", "mp3", "fil", "tillägg", "format", "vad är mod filformat", "musik", "mod filformat", "mod vs MP3", "mod filformatspecifikation "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Lär dig om MOD-filformat och API:er som kan skapa, konvertera och öppna MOD-filer.",
  "title" :"MOD - Musikmodulfil",
  "linktitle" : "MOD",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-04"
}

## Vad är en MOD-fil?
En fil med filtillägget .mod är en musikmodulfil som skapats med hjälp av standardformatet för musikmodulen, som är baserat på **Amiga-modulformatet** utvecklat av Karsten Obarski och släppt med programvaran **Ultimate Soundtracker** för Commodore Amiga system. På samma sätt som en [MIDI](/sv/audio/mid/)-fil består den av notmönster och ljudsampel, som representerar olika instrument som spelas upp enligt noterna. MOD-filer används särskilt i videospel som bakgrundsmusik och i subkulturen **demoscene** datorkonst.

## MOD filformat

MOD är ett datorfilformat som används, dess grundläggande funktion är att representera musik, och det var det första modulfilformatet. MOD-filer använder filtillägget .mod, förutom på **Amiga** som läser en fils rubrik för att bestämma filtyp, så den är inte beroende av filnamnstillägg. En MOD-fil består av en uppsättning olika instrument i form av samples, ett antal mönster som anger hur och när samplen ska spelas samt en lista över vilka mönster som ska spelas i vilken ordning.

### MOD Filformatspecifikationer

Ett MOD-filmönster är faktiskt utformat i ett sequencer-användargränssnitt som en tabell med en kolumn per kanal, så denna tabell har fyra kolumner (en för varje Amiga-hårdvarukanal. Varje kolumn har 64 rader).

En cell i tabellen kan göra att en av följande åtgärder inträffar på dess kolumnkanal när tiden för dess rad har uppnåtts:

- Starta ett instrument som spelar en ny ton i den här kanalen vid en given volym, eventuellt med en speciell effekt på den
- Ändra volymen eller specialeffekten som tillämpas på den aktuella noten
- Ändra mönsterflöde; hoppa till en specifik låt eller mönsterposition eller loop inuti ett mönster
- Göra ingenting; alla befintliga noter som spelas i den här kanalen kommer att fortsätta att spelas

Ett instrument är ett enda prov tillsammans med en valfri specifikation av vilken del av provet som kan upprepas för att hålla en solid ton.

### Timing
Den minsta tidsramen var 0,02 sekunder i den ursprungliga MOD-filen, eller ett "vertical blanking" (VSync) intervall, eftersom den ursprungliga programvaran använde VSync-timingen för monitorn som körde på 50 Hz (för PAL) eller 60 Hz (för NTSC) för timing.

## Referenser

* [MOD (filformat) - av Wikipedia](https://en.wikipedia.org/wiki/MOD_(file_format))

