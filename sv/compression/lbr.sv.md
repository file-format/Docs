{
  "date" : "2021-04-08",
  "keywords" :[ "mst-fil", "mst-filformat", "vad är en mst-fil", "fil", "mst-exempel", "mst-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
	

},
  "draft" : "false",
  "toc" : true,
  "title" :"LBR - LU Library Archive File Format",
  "description":"Läs mer om LBR-filformat och API:er som kan skapa och öppna LBR-filer.",
  "linktitle" : "LBR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Vad är LBR fil?

En fil med tillägget .lbr är en arkivfil skapad med LU-programmet och användes på CP/M- och DOS-operativsystem under 1980-talet. Den används inte längre och har ersatts av moderna arkiveringsfilformat. Formatet komprimerar inte medlemsfilerna och fungerar som containerarkiv för dessa. Arkiveringsfunktionen användes mest för överföring av arkiverade filer över internet. Eftersom LBR inte erbjöd komprimering, användes andra verktyg som SQ eller CRUNCH för att komprimera medlemsfilerna före arkivering eller den resulterande arkivfilen efter arkivering för att minska dess storlek.

## LBR filformat

LBR-filformatet har designats av Gary P. Novosielski och har inga tekniska detaljer tillgängliga för allmänheten. LBR-filer börjar med en 0x00 byte, följt av 11 mellanslag (0x20), sedan två 0x00 byte, sedan två byte som inte båda är 0x00. Eftersom det är containerfilformat kan det extraheras med hjälp av LU.COM och NULU.COM.

## Referenser

* [LBR - Wikipedia](https://en.wikipedia.org/wiki/LBR_(file_format))

