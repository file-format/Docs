{
  "date" : "2021-08-11",
  "keywords" :[ "vox", "fil", "tillägg", "format", "ljud", "ADPCM", "Dialogic ADPCM", "Xentec VOX Studio","vox-tillägg", "vox-filer"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om VOX-filformat och API:er som kan skapa och öppna VOX-filer.",
  "title" :"VOX - Audio File Format",
  "linktitle" : "VOX",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-11"
}

## Vad är en VOX fil? ##

Vid en låg samplingshastighet specificeras VOX-filerna för att lagra digitaliserade röstdata. Dessa är ljudfiler som vanligtvis används i de applikationer som specificeras för telefonisk kommunikation. Denna typ av filformat använder en algoritm för förlustkomprimering som har en optimering för röst.

Vanligtvis används i talapplikationer VOX-filerna innehåller förinspelade röstuppmaningar. Denna typ av filformat konverteras också till andra mer populära format. Dessa kan användas i Windows operativsystem och macOS.

Det används mest för röstinspelningar och komprimering. I detta format kan polyfonisk data inte lagras eftersom den endast stöder homofoba data.



## Kortfattad bakgrund ##

VOX-filerna är associerade med Media Boards som kallas DMV och JCT of Dialogic. Dessa tillhör VoxWare och mycket annan programvara. Det brukade betraktas som ett föråldrat format.

Som ett föråldrat format användes det inte efter det. I likhet med andra ADPCM-format komprimerades den till 4 bitar. Funktionerna i dessa filer är tillräckligt nära [WAV](/sv/audio/wav/) filspecifikationer.


## Formatspecifikationer ##

Den här typen av filformat är kompatibelt med Windows OS-program som Xentec Vox Studio. Den har specifika egenskaper som används för att stimulera människors tal. Arkadspel använder oftast detta format. VOX-filtillägget har en 32-byte header tillsammans med 10-byte index och ramar. Den faktiska röstdatan sparas i ramar i form av segment i en enda fil. Det finns en annan form av flera byte i varje ram baserat på typen av kodning.

Klargörandet av rösten hålls vid en låg samplingshastighet, vilket är sällsynt i de flesta ljudformat. Algoritmen som användes i dessa var matematisk.

Denna fil är kodad med hjälp av ADPCM. Den kortsluter 16-bitars ljuddata och 4-bitars komprimering. Så det finns en fördel med att spara större ljudinformation i en kompakt form med hjälp av VOX-filer.


## Referenser ##

* [VOX - av Wikipedia](https://en.wikipedia.org/wiki/Dialogic_ADPCM)

