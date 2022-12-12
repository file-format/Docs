{
  "date" : "2019-10-11",
  "keywords" :[ "M4V", "soubor", "rozšíření", "formát", "MPEG-4", "Správa digitálních práv", "DRM", "Apple", "video"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M4V",
  "description":"Další informace o formátu souboru M4V a rozhraních API, která mohou vytvářet a otevírat soubory M4V.",
  "linktitle" : "M4V",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-14"
}

## Co je soubor M4V?

Formát souboru **M4V**, vyvinutý společností Apple, je kontejner videa volitelně chráněný ochranou proti kopírování Digital Rights Management (DRM), která chrání soukromí nebo kopírování. Videa a zvukové stopy jsou obaleny kontejnerovými soubory pro indexování a organizování přehrávaných streamů. Kromě toho kontejnery také poskytují funkci kapitol podobných těm na DVD. Apple používá M4V ke kódování videí ve svém iTunes Store. Chrání neoprávněnou reprodukci prostřednictvím ochrany proti kopírování FairPlay společnosti Apple tím, že umožňuje přehrávat soubory M4V pouze na autorizovaných počítačích, které mají účty použité k nákupu videa. Pokud je však ze souborů M4V odstraněna ochrana DRM, lze tyto soubory přehrávat v jiných přehrávačích videa změnou přípony z .m4v na .mp4, což je důvod, proč jsou soubory M4V spojeny s MPEG-4. M4V používá H.264 pro video a **[AAC](/cs/audio/aac/)** a Dolby Digital pro kódování a dekódování zvuku.

## Struktura souboru M4V ##

Soubory M4V mají souvislé bloky s 8bajtovým záhlavím, 4bajtovou velikostí bloku a 4bajtovým typem bloku v každém bloku. První blok je „ftype“ a má podtyp na offsetu 8. M4V definovaný podtypem, který musí být „M4V_“. Další typy chunků jsou předdefinované signatury: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2", "wide" , "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", " OBRÁZEK". Opakujeme bloky, dokud není detekován neznámý typ, skládáme soubor M4V.

Zde je zkoumání vzorku: Binární data ukázkového souboru m4v jsou kontrolována pomocí Hex Viewer a lze pozorovat, že začíná podpisem **ftyp** (hex: 66 74 79 70) na offsetu 4, který definuje QuickTime Typ souboru kontejneru. Podtyp souboru je **M4V_** (hex: 4D 34 56 20), což ukazuje na typ souboru M4V (MPEG-4). Velikost prvního bloku je 32 (hex: 00 00 00 20, big-endian, první vysoký bajt), velikost umístěná na offsetu 0. Na offsetu 32 (hex: 20) je umístěn druhý blok, který má velikost 30 322 (hex : 00 00 76 72, big-endian, nejprve nižší bajt) a zadejte **moov** (hex: 6D 6F 6F 76). Další blok se nachází na offsetu 32+30,322#30,354 (hex: 00 00 76 92) a má velikost 8 (hex: 00 00 00 08) a typ **free** (hex: 66 72 65 65).
### Kodeky používané v M4V ###

#### Video kodek H.264 ####

H.264 je standard pro kompresi videa, který převádí digitální video do formátu, který vyžaduje méně místa při přenosu nebo ukládání. M4V používá pro kompresi videa H.264. Jeho aplikace sahá od DVD, TV, videokonferencí a streamování videa přes internet. H.264 se skládá ze dvou hlavních částí: Encoder – který komprimuje video, Decoder – který dekomprimuje komprimované video zpět. Na obrázku níže jsou zvýrazněny procesy kódování a dekódování a další procesy jsou pokryty standardem H.264.

##### Proces kódování a dekódování videa v H.264 #####

U komprimovaného bitového toku H.264 provádí kodér videa proces predikce, transformace a kódování. Současně dekodér provádí inverzní proces dekódování, inverzní transformace a rekonstrukce, aby vytvořil zpět video soubor. H.264 má poloviční velikost než MPEG.

#### Audio kodek ####

Advanced Audio Coding (AAC) je zvukový kodek pro ztrátovou digitální kompresi zvuku a používá se v kontejneru M4V. AAC je nástupcem formátu [MP3](/cs/audio/mp3/) a dosahuje lepší kvality než MP3 se stejným datovým tokem. Formát AAC zahazuje některé informace během procesu komprese, což je méně důležité. AAC je blokově založený kodek s proměnným bitrate (VBR), kde každý blok dekóduje na 1024 vzorků v časové doméně.

### Reference ###

* [Wikipedie – M4V](https://en.wikipedia.org/wiki/M4V)
* [Wikipedie – MPEG-4_AVC](https://en.wikipedia.org/wiki/H.264/MPEG-4_AVC)

