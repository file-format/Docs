{
  "date" : "2022-02-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om CSD Steam Game Data Backup-filformat och API:er.",
  "title" :"CSD File Format - Steam Game Data Backup File",
  "linktitle" : "CSD",
  "menu" : {
    "docs" : {
      "identifier": "game-csd",
      "parent" : "game"
}
},
  "lastmod" : "2022-02-08"
}

## Vad är en CSD-fil?

En CSD-fil är en säkerhetskopieringsfil som genereras av speltjänsten **Steam** som låter användare ladda ner och hantera **Valve**-spel. Den innehåller säkerhetskopieringsdata relaterade till spel som kan användas för att återställa ett borttaget spel. Steam kan bara återställa spel från en CSD-fil om spelet har laddats ner, installerats och korrigerats genom Steam. För att återställa spelet från CSD-fil, använd alternativet Steam → Säkerhetskopiera och återställ Gamesteam och välj filen.

## CSD-filformat - Mer information

Den interna strukturen för CSD-filformatet är inte tillgänglig offentligt och dess filformatspecifikationer är inte tillgängliga för utvecklarens referens. CSD-filer åtföljs av CSM- och ISS-filer som också är Steam-spelfilformat.

### Var hittar jag Steam-säkerhetskopieringsfiler?

Hela Steam-backupfilerna finns på följande platser:

* C:\Program Files (x86)\Steam\steamapps\common\<game name> \ :
* \cfg\ - Anpassade konfigurationer och konfigurationsskript
* \downloads\ - Anpassat innehåll för spel med flera spelare
* \maps\ - Anpassade kartor som har installerats eller laddats ner under multiplayer-spel
* \materials\ - Anpassade texturer och skal
* \SAVE\ - Sparade spel för en spelare

Platsen för spel som skapats av tredje part kan dock vara annorlunda och bestäms av spelets utvecklare.

### Återställer från CSD Backup File

Installera Steam och logga in på rätt Steam-konto (se Installera Steam för ytterligare instruktioner)
* Starta Steam
* Klicka på "Steam" i det övre vänstra hörnet av Steam-applikationen
* Välj "Säkerhetskopiera och återställa spel..."
* Välj "Återställ en tidigare säkerhetskopia"
* Bläddra till platsen för spelets säkerhetskopior
* Fortsätt genom Steam-fönstren för att installera de nödvändiga spelen.

## Referenser

* [Använda Steam Backup-funktionen](https://help.steampowered.com/en/faqs/view/4593-5CB7-DC3C-64F0)

