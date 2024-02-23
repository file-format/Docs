{
  "date" : "2023-01-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Lär dig om Age of Empires 2 Expansion Replay MGX-filformat och API:er som kan skapa och öppna MGX-filer.",
  "title" : "MII-fil - Wii Virtual Avatar-filformat",
  "linktitle" : "MII",
  "menu" : {
    "docs" : {
      "identifier":"game-mii-sv",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-15"
}

## Vad är MII fil?

En MII-fil är ett virtuellt avatar-filformat som används för att lagra virtuella avatarer på Nintendo Wii-spelkonsolen. Dessa filer innehåller information som avatarens utseende, rörelser och animationer. De kan användas i spel, sociala nätverksapplikationer och annan programvara på Wii. En MII-fil innehåller även andra funktioner om avataren som kön, hårfärg, hudfärg, ansiktsdrag och ögontyp.

Du kan öppna en MII-fil med [My Avatar Editor](https://rc24.xyz/goodies/mii/).

## MII filformat

MII-filformatet definieras i detalj på [Wii Brew](https://wiibrew.org/wiki/Mii_data). Strängar i en MII-fil lagras i Unicode-format (UTF-16), big-endian.

### MI-block

MII-fildata lagras på Wiimote i två block. Varje block är 750 byte långt, med 2 byte CRC, vilket gör det totalt 752 byte. Varje block börjar med ett 4-byte-värde ('RNCD') som verkar vara det magiska numret för MII-filformatet.

## Hur skapar man MII-filer?

Det finns några olika sätt att skapa avatarer för Nintendo Wii:

1. Använda den inbyggda Mii-kanalen på Wii: Denna kanal låter dig skapa anpassade avatarer med hjälp av en mängd olika verktyg, inklusive ansiktsdrag, kroppsform och kläder. När du har skapat din avatar kan du spara den som en Mii-fil och använda den i spel och annan programvara på Wii.

1. `Använda Mii Maker-appen på Nintendo 3DS:` Mii Maker-appen låter dig skapa anpassade avatarer med hjälp av pekskärmen och kameran på din Nintendo 3DS. När du har skapat din avatar kan du spara den som en Mii-fil och överföra den till din Wii via en trådlös anslutning.

1. `Använda programvara från tredje part:` Vissa utvecklare har skapat programvara som låter dig skapa anpassade avatarer för Wii. Denna programvara är vanligtvis utformad för användning på en dator och kan kräva ytterligare steg för att överföra avataren till din Wii.

1. `Använda förgjorda avatarer:` Vissa spel och annan programvara på Wii kan komma med färdiga avatarer som du kan använda.

I alla fall måste du ha ett Nintendo-konto för att skapa och spara din avatar på Wii.

## Referenser

* [My Avatar Editor](https://rc24.xyz/goodies/mii/)

* [Wii Brew](https://wiibrew.org/wiki/Mii_data)


