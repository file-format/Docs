---
date: 2019-10-11
keywords: MP4, file, extension, format, video format, MPEG-4
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Lthuilleamh faoi formáid comhaid MP4 agus APIs is féidir a chruthú agus a oscailt comhad MP4s.
title: MFoirm Chomhaid P4at
linktitle: MP4
menu:
  docs:
    parent: "video"
lastmod: 2021-07-26
---

## Cad is comhad MP4 ann? ##

MP4(short for MPEG-4 Part 14) is a file format based on ISO/IEC 14496-12:2004 that is based on QuickTime File Format but formally specifies support for Initial Object Descriptors (IOD) and other MPEG features. It is mostly used to store video and audio but can also be used to store subtitles and still images. MP4 files are stored with the .mp4 extension. MP4 is an international audio-visual coding standard. Similar to most modern container formats, MP4 supports streaming over the internet. Due to the high compression used in MP4, the resultant files are smaller in size with almost all the original quality retained.

## Stair Ghearr ##

MP4 specification was developed by Moving Picture Experts Group (MPEG) and was based on the QuickTime format [MOV](/video/mov/) that was published in 2001. Ba athbhreithniú é an chéad leagan (ISO/IEC 14496-1:2001) de MP4 ar shonraíocht an chórais MPEG-4 Cuid 1: a foilsíodh i 1999. Rinneadh formáid comhaid MP4 a ghinearálú go Formáid Chomhaid Meán-Bhun ISO ISO/IEC 14496-12 :2004 a shainigh an struchtúr ginearálta do chomhaid meán bunaithe ar am. Mar thoradh air sin, úsáidtear é mar bhunús le formáidí comhaid eile.

## Struchtúr Chomhaid MP4 ##

Is comhad coimeádán sínte é MP4, rud a chiallaíonn nach sainmhíníonn sé struchtúr docht agus go gceadaíonn sé struchtúr agus ordlathas saincheaptha do gach cineál meán. Tá na sonraí sa chomhad MP4 roinnte ina dhá chuid, an chéad cheann ina bhfuil na sonraí a bhaineann leis na meáin agus an dara ceann ina bhfuil meiteashonraí. Tá fuaime nó físe sna sonraí meán agus léiríonn meiteashonraí bratacha le haghaidh rochtana randamach, stampaí ama, etc.
De ghnáth tugtar adaimh nó boscaí ar na struchtúir i MP4. Is é 8 mbeart an t-íosmhéid adaimh (sonraíonn an chéad 4 beart an méid agus sonraíonn an chéad 4 beart an cineál). Seo liosta de na hadaimh bunleibhéil atá i gcomhaid MP:

- **ftyp**: Contains the file type, description, and the common data structures used.
- **pdin**: Tá faisnéis maidir le luchtú/íoslódáil físe forásach ann.
- **moov**: Coimeádán do na meiteashonraí scannáin ar fad.
- **moof**: Coimeádán le blúirí físeáin.
- **mfra**: An coimeádán a bhfuil rochtain randamach aige ar an blúire físeáin
- **mdat**: Coimeádán sonraí do na meáin.
- **sts**: tábla samplach go ham.
- **stsc**: tábla samplach-go-bunt.
- **stsz**: méideanna na samplaí (frámáil)
- **meta**: An coimeádán leis an bhfaisnéis meiteashonraí.

Seo liosta na n-adamh dara leibhéal a úsáidtear i MP4:

- **mvhd**: Tá an fhaisnéis ceanntásca físeáin mar aon le sonraí iomlána an fhíseáin.
- **trak**: Coimeádán leis an rian aonair.
- **udta**: An coimeádán leis an úsáideoir agus faisnéis rian.
- **iods**: tuairisceoir comhaid MP4

## Tagairtí ##

- [MP4 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

