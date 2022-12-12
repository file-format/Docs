{
  "date" : "2019-10-11",
  "keywords" :[ "M4V", "fișier", "extensie", "format", "MPEG-4", "Gestionarea drepturilor digitale", "DRM", "Apple", "video"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M4V",
  "description":"Aflați despre formatul de fișier M4V și despre API-urile care pot crea și deschide fișiere M4V.",
  "linktitle" : "M4V",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-14"
}

## Ce este un fișier M4V?

Formatul de fișier **M4V**, dezvoltat de Apple, este un container video protejat opțional cu protecție la copiere Digital Rights Management (DRM) pentru a proteja confidențialitatea sau copierea. Videoclipurile și melodiile audio sunt împachetate în fișiere container pentru a indexa și organiza fluxurile de redare. În plus, containerele oferă și caracteristica capitolelor similare cu cele de pe DVD-uri. Apple folosește M4V pentru a codifica videoclipuri în iTunes Store. Protejează reproducerea neautorizată prin protecția de copiere FairPlay de la Apple, permițând ca fișierele M4V să fie redate numai pe computere autorizate care au conturile utilizate pentru achiziționarea videoclipului. Cu toate acestea, dacă protecția DRM este eliminată din fișierele M4V, aceste fișiere pot fi redate în alte playere video prin schimbarea extensiei de la .m4v la .mp4, motiv pentru care fișierele M4V sunt asociate cu MPEG-4. M4V folosește H.264 pentru video și **[AAC](/ro/audio/aac/)** și Dolby Digital pentru codificare și decodare audio.

## Structura fișierului M4V ##

Fișierele M4V au bucăți continue cu antet de 8 octeți, dimensiunea fragmentului de 4 octeți și tip de fragment de 4 octeți în fiecare fragment. Prima bucată este „ftype” și are un subtip la offset 8. M4V definit de subtip care trebuie să fie „M4V_”. Alte tipuri de bucăți sunt semnături predefinite: „ftyp”, „mdat”, „moov”, „pnot”, „udta”, „uuid”, „moof”, „free”, „skip”, „jP2”, „wide” , „încărcare”, „ctab”, „imap”, „mat”, „kmat”, „clip”, „crgn”, „sync”, „chap”, „tmcd”, „scpt”, „ssrc”, „ PICT”. Iterând bucăți, până când este detectat tipul necunoscut, compunem fișierul M4V.

Iată o examinare a unui eșantion: Datele binare ale unui fișier m4v eșantion sunt inspectate prin Hex Viewer și se poate observa că începe cu o semnătură **ftyp** (hex: 66 74 79 70) la offset 4, care definește QuickTime Tip de fișier container. Subtipul de fișier este **M4V_** (hex: 4D 34 56 20) care indică tipul de fișier M4V (MPEG-4). Dimensiunea primului bloc este 32 (hex: 00 00 00 20, big-endian, high byte primul), dimensiunea situată la offset 0. La offset 32 (hex: 20) se află a doua bucată, care are o dimensiune de 30.322 (hex). : 00 00 76 72, big-endian, primul octet inferior) și tastați **moov** (hex: 6D 6F 6F 76). Următoarea bucată este situată la offset 32+30,322#30,354 (hex: 00 00 76 92) și are dimensiunea 8 (hex: 00 00 00 08) și tip **free** (hex: 66 72 65 65).
### Codecuri utilizate în M4V ###

#### Codec video H.264 ####

H.264 este un standard de compresie video care convertește videoclipurile digitale într-un format care necesită mai puțin spațiu atunci când este necesar transmisia sau stocarea. M4V utilizează H.264 pentru compresia video. Aplicația sa variază de la DVD, TV, videoconferințe și streaming video pe internet. H.264 constă din două părți principale: Encoder – care comprimă videoclipul, Decoder – care decomprimă înapoi videoclipul comprimat. În figura de mai jos, procesele de codificare și decodare sunt evidențiate, iar alte procese sunt acoperite în standardul H.264.

##### Proces de codificare și decodare video în H.264 #####

Pentru fluxul de biți H.264 comprimat, codificatorul video conduce procesul de predicție, transformare și codificare. În același timp, decodorul efectuează procesul invers de decodare, transformare inversă și reconstrucție pentru a produce înapoi fișierul video. H.264 are jumătate din dimensiunea MPEG.

#### Codec audio ####

Advanced Audio Coding (AAC) este un codec audio pentru compresia audio digitală cu pierderi și este utilizat într-un container M4V. AAC este succesorul formatului [MP3](/ro/audio/mp3/) și atinge o calitate mai bună decât MP3 cu același bitrate. Formatul AAC aruncă unele informații în timpul procesului de comprimare, care este de mai puțină importanță. AAC este un codec bazat pe blocuri cu rata de biți variabilă (VBR) în care fiecare bloc decodifică la 1024 de mostre din domeniul timpului.

### Referințe ###

* [Wikipedia - M4V](https://en.wikipedia.org/wiki/M4V)
* [Wikipedia - MPEG-4_AVC](https://en.wikipedia.org/wiki/H.264/MPEG-4_AVC)

