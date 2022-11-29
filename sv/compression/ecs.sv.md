{
  "date" : "2022-06-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ECS File Format - Sony Ericsson Phone Backup File",
  "description":"Läs mer om ECS-filformat och API:er som kan skapa och öppna ECS-filer.",
  "linktitle" : "ECS",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-30"
}

## Vad är ECS fil?

En ECS-fil är en säkerhetskopieringsfil som skapats av Sony Ericssons mobiltelefoner. Den lagrar en kopia av användarens data som säkerhetskopia om återställning krävs för att återställa lagrad data. ECS-filer sparas som komprimerade [ZIP](/sv/compression/zip/)-arkiv för att minska skivutrymmesutnyttjandet. Detta gör det också enkelt att överföra data över låghastighetsinternetanslutningar.

## ECS-filformat - Mer information

ECS-filer sparas som komprimerade ZIP-arkiv. Den kan öppnas med vilket standardprogram som helst som WinZip och WinRAR. För detta, byt namn på filtillägget från .ecs till .zip och extrahera innehållet med WinZip.

## Referenser

* [Dzip](http://speeddemosarchive.com/dzip/)

