{
  "date": "2019-10-11",
  "keywords": [
"M4V",
"comhad",
"síneadh",
"formáid",
"MPEG-4",
"Bainistíocht Cearta Digiteacha",
"DRM",
"Úll",
"físeán"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "M4V",
  "description": "Foghlaim faoi fhormáid comhaid M4V agus APIs ar féidir leo comhaid M4V a chruthú agus a oscailt.",
  "linktitle": "M4V",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-m4-gav"
}
},
  "lastmod": "2019-09-14"
}

## Cad is comhad M4V ann?

**M4V** file format, developed by Apple, is a video container optionally protected with Digital Rights Management (DRM) copy protection to protect privacy or copy. Videos and audio tracks are wrapped around by container files to indexing and organizing playback streams. In addition, containers also provide the feature of chapters similar to those on DVDs. Apple uses M4V to encode videos in its iTunes Store. It protects unauthorized reproduction through Apple’s FairPlay copy protection by allowing M4V files to be played on only authorized computers having the accounts used to purchase the video. However, if DRM-protection is removed from M4V files, these files can be played in other video players by changing the extension from .m4v to .mp4, which is why M4V files are associated with MPEG-4. Úsáideann M4V H.264 le haghaidh físeáin agus **[AAC](/audio/aac/)** agus Dolby Digital le haghaidh ionchódú agus díchódú fuaime.

## Struchtúr Comhad M4V ##

M4V files have continuous chunks with 8 byte header, 4 byte chunk size and 4 byte chunk type in each chunk. First chunk is “ftype” and has a sub-type at offset 8. M4V sainmhínithe ag fo-chineál a chaithfidh a bheith M4V_. Is sínithe réamhshainithe iad cineálacha smután eile: ftyp, mdat, moov, pnot, udta, uuid, moof, free, skip, jP2, wide , luchtú, ctab, imap, neamhlonrach, kmat, gearrthóg, crgn, sioncronú, chap, tmcd, scpt, ssrc,  PICT. Sumpaí atriallta, go dtí go n-aimsítear cineál anaithnid, déanaimid comhad M4V a chumadh.

Here is an examination of a sample: A sample m4v file’s binary data is inspected through Hex Viewer and it can be observed that it starts with a signature **ftyp** (hex: 66 74 79 70) at offset 4, which defines QuickTime Container File Type. File sub-type is **M4V_** (hex: 4D 34 56 20) which points to M4V (MPEG-4) file type. First block size is 32 (hex: 00 00 00 20, big-endian, high byte first), size located at offset 0. Ag fritháireamh 32 (heics: 20) tá an dara smután, a bhfuil méid 30,322 aige (hex: 00 00 76 72, mór-endian, beart níos ísle ar dtús) agus cineál **moov** (hex: 6D 6F 6F 76). Tá an chéad smután eile suite ar fhritháireamh 32+30,322#30,354 (heicsidheachúlach: 00 00 76 92) agus tá méid 8 aige (heicse: 00 00 00 08) agus clóscríobh **saor in aisce** (hex: 66 72 65 65).
### Codecs Úsáidte i M4V ###

#### Codec Físe H.264 ####

Is caighdeán comhbhrú físe é H.264 a thiontaíonn físeán digiteach go formáid a éilíonn níos lú spáis nuair is gá é a tharchur nó a stóráil. Úsáideann M4V H.264 le haghaidh comhbhrú físeáin. Cuimsíonn a fheidhmchlár ó DVD, teilifís, físchomhdháil, agus sruthú físeáin ar an idirlíon. Tá dhá phríomhchuid i H.264: Ionchódóir – A chomhbhrúigh an físeán, Díchódóir – A dhí-chomhbhrúigh an físeán comhbhrúite ar ais. Sa fhigiúr thíos, leagtar béim ar phróisis ionchódaithe agus díchódaithe, agus clúdaítear próisis eile sa chaighdeán H.264.

##### Próiseas um Chódú agus Díchódú Físeáin in H.264 #####

Maidir leis an sruth giotán comhbhrúite H.264, seolann an t-ionchódóir físeáin an próiseas réamh-mheasta, claochlaithe agus ionchódaithe. Ag an am céanna, déanann an díchódóir an próiseas inbhéartach díchódaithe, claochlú inbhéartach agus atógáil chun an comhad físe a thabhairt ar ais. Glacann H.264 leath mhéid an MPEG.

#### Codec Fuaime ####

Is codec fuaime é Ardchódú Fuaime (AAC) le haghaidh comhbhrú fuaime digiteach caillte agus úsáidtear é i gcoimeádán M4V. Tagann AAC i gcomharbacht ar fhormáid [MP3](/audio/mp3/) agus baineann sé cáilíocht níos fearr amach ná MP3 leis an ráta giotán céanna. Caitheann formáid AAC roinnt faisnéise le linn an phróisis chomhbhrúite, rud nach bhfuil chomh tábhachtach céanna. Is CODEC bloc-bhunaithe ráta inathraithe (VBR) é AAC ina ndíchódaíonn gach bloc go 1024 sampla fearainn ama.

### Tagairtí ###

* [Wikipedia - M4V](https://en.wikipedia.org/wiki/M4V)

* [Vicipéid - MPEG-4_AVC](https://en.wikipedia.org/wiki/H.264/MPEG-4_AVC)


