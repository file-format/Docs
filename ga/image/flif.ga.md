---
date: 2020-08-12
keywords: flif, .flif, flif file format, how to open flif files, .flif extension, flif extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: FFoirm Comhaid LIFat
linktitle: FLIF
description: Lthuilleamh faoi fhormáid comhaid FLIF agus APIs ar féidir leo comhad FLIF a chruthú agus a oscailts.
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Cad is comhad FLIF ann? ##

Is formáid íomhá gan chailliúint é FLIF (Formáid Íomhá Saor in Aisce) a úsáideann an síneadh .flif dá chomhaid. Maíonn FLIF go sáraíonn sé [PNG](/image/png/), gan chailliúint [WebP](/image/webp/), BPG gan chailliúint, agus JPEG 2000 gan chailliúint i dtéarmaí cóimheas comhbhrú. Úsáideann FLIF interlacing forásach, mar gheall ar a bhféadfar aon íoslódáil páirteach den íomhá a úsáid mar ionchódú caillteanas don íomhá iomlán.

## Stair Ghearr ##

FLIF was announced in September 2015, and the alpha version was released in October 2015. I mí Mheán Fómhair 2016, scaoileadh an chéad leagan cobhsaí de FLIF.

## Dearadh FLIF ##

Úsáideann FLIF malairt de CABAC (códú dénártha comhthéacs-oiriúnaitheach), MANIAC (Códú Uimhríochtúil Slánuimhir Meta-Oiriúnaithe Near-nialais) le haghaidh comhbhrú. Is algartam códaithe eantrópachta é MANIAC arna fhorbairt ag Jon Sneyers agus Pieter Wuille. I MANIAC, is iad na comhthéacsanna ná nóid de chrainn chinnidh a fhoghlaimítear ag am ionchódaithe go dinimiciúil. Déanann sé seo an múnla comhthéacs níos sainiúla don íomhá agus cruthaíonn sé comhbhrú níos fearr. Tá na gnéithe seo a leanas ag FLIF:

- Tacaíonn comhbhrú lossless
- Tacaíonn comhbhrú lossy le réamhphróiseáil ionchódóra
- Tacaíonn Greyscale, RGB agus RGBA
- Tacaíonn doimhneacht dath 1 go 16 giotán in aghaidh an chainéil
- Tacaíonn comhaid interlaced agus neamh-interlaced
- Tacaíonn sé le díchódú forásach ar chomhaid a íoslódáltar go páirteach
- Tacaíonn beochan
- Tacaíonn sé le próifílí datha ICC leabaithe, meiteashonraí Exif agus XMP
- Tá tacaíocht teoranta aige chun comhaid amh ceamara a chomhbhrú (RGGB)

## Formáid Chomhaid FLIF ##

Tá na ceithre chuid seo a leanas i gcomhad FLIF:

## Príomhcheannfhocal ##

Tá na príomh-mheiteashonraí sa phríomhcheann, lena n-áirítear an leithead, airde, doimhneacht datha, líon na bhfrámaí.

|Cineál|Luach|Cur Síos|
|---|---|---|
|4 beart|FLIF|Draíocht|
|4 ghiotán|3 = ni fós; 4 = mé fós; 5 = ni anam; 6 = i beochan|Idirléite, beochan|
|4 ghiotán|1 = Liathscála; 3 = RGB; 4 = RGBA|Líon na gcainéal (nb_chainéil)|
|1 beart|'0','1','2' ('0'=saincheaptha)|Beirt in aghaidh an chainéil (Bpc)|
|varint|leithead-1|leithead|
|varint|airde-1|Airde|
|varint|nb_frames-2 (más beochan amháin)|Líon na bhfrámaí (nb_frames)|

## Sliotán meiteashonraí ##

Tá neamh-phicteilín sa chuid seo cosúil le meiteashonraí Exif/XMP, próifíl datha ICC, srl. atá ionchódaithe le comhbhrú DEFLATE. Sainmhínítear na smután seo mar an gcéanna le smután PNG agus is é an difríocht ná go bhfuil an méid chuck ionchódaithe le líon athraitheach beart. Is féidir le hainmneacha smután a bheith ina 4 litir (4 beart) nó luach faoi bhun 32 ag léiriú smután neamhroghnach.

Seo a leanas sampla de chucks roghnacha:

|Ainm smeara|Cur Síos|Ábhar (tar éis dí-chomhbhrú deFLATE)|
|---|---|---|
|iCCP|próifíl datha ICC|sonraí amhphróifíl datha ICC|
|eXif|Meiteashonraí Exif| Ceanntásc Exif\0\0 agus ceanntásc TIFF ina dhiaidh agus sonraí EXIF |
|eXmp|Meiteashonraí XMP|XMP laistigh de xpaicéad inléite amháin gan stuáil|

### Coinbhinsiún Ainmnithe ###

- **An Chéad Litir**: Úsáidtear cás uachtair le haghaidh criticiúil agus úsáidtear cás íochtair le haghaidh smután neamhchriticiúil.
- **Dara Litir**: Baintear úsáid as an chás uachtair le haghaidh poiblí agus úsáidtear cás íochtair le haghaidh smutáin phríobháideacha
- **Tríú Litir**: Úsáidtear cás uachtair le haghaidh chucks a theastaíonn chun an íomhá a thaispeáint i gceart agus níl cás íochtair tábhachtach chun an íomhá a thaispeáint.
- **Ceathrú Litir**: Úsáidtear an cás uachtair le haghaidh chucks is féidir a chóipeáil go dall go sábháilte. Braitheann chucks cás íochtair ar shonraí na híomhá.

## Dara Ceanntásc ##

Tá an fhaisnéis ann maidir le fíor-ionchódú na bpicteilín.

|Cineál|Cur Síos|Coinníoll|Luach Réamhshocraithe|
|---|---|---|---|
|1 beart|beart NUL (0x00), ainm smuta srutha giotaí FLIF16 ||
|uni_int(1,16)|Giotán in aghaidh na picteilín de na cainéil|Bpc == '0': athrá(nb_chainéil)|8 má Bpc == '1', 16 má Bpc == '2'|
| uni_int(0,1)|Bratach: alfa_zero|nb_chainéil > 3|0|
|uni_int(0,100)|Líon lúb|nb_frámaí > 1||
| uni_int(0,60_000)|Moill fráma in ms| nb_frames > 1: athrá(nb_frames)|
| uni_int(0,1)|Bratach: has_custom_cutoff_and_alpha|||
| uni_int(1,128)|scoith|tá_custom_gearradh_agus_alfa|2|
| uni_int(2,128)|roinnteoir alfa|tá_custom_gearrtha_agus_alfa|19|
| uni_int(0,1)|Bratach: has_custom_bitchance|tá_custom_cutoff_and_alpha|0|
|?|Bitchance|tá_custom_bitchance||
|athróg|Claochluithe (féach thíos)||
|uni_int(1) = 0|Giotán táscairí: déanta le claochluithe ||
|uni_int(0,2)|Rangóir dofheicthe picteilín | alfa_nialas && idirfhite && folaíonn raon alfa nialas ||

**Cainéil**

|Uimhir chainéil|Cur síos|
|---|----|
|0|Dearg nó Liath|
|1|Glas|
|2|Gorm|
|3|Alfa|

**Claochluithe**

|Cineál|Cur Síos|
|---|---|
|uni_int(1) = 1|Giotán táscaire: gan déanamh fós|
|uni_int(0,13)|Aitheantóir claochlaithe |
|athróg|Sonraí claochlaithe (ag brath ar chlaochlú) |

Úsáidtear claochlú chun sonraí picteilín a mhodhnú le haghaidh comhbhrú níos fearr agus chun súil a choinneáil ar na luachanna picteilín atá ag tarlú i ndáiríre.

## Sonraí picteilíní ##

Tá na sonraí picteilín iarbhír ionchódaithe ag baint úsáide as códú eantrópachta MANIAC sa chuid seo. Is féidir na picteilíní a ionchódú trí úsáid a bhaint as ionchódú idirlactha nó neamh-idirfhriotaíoch.

### Modh idirléite ###

In this method, zoomlevels are defined. Zoomlevel 0 is used for the full image, zoomlevel 1 is used for all even-numbered rows, zoomlevel 2 is used for all even-numbered columns of zoomlevel 1. Is é sin le rá, is leagan íos-shampláilte den íomhá é gach leibhéal zúmála cothrom-uimhrithe 2k, ar scála 1:2 ^k. Tá Zoomlevels ionchódaithe ón gceann is airde go dtí an ceann is ísle.

### Modh neamhcheangailte ###

Ar an modh seo, tosaíonn ionchódú na gcrann MANIAC láithreach agus ansin ionchódú na bpicteilín.

## Tagairtí ##

- [FLIF - Wikipedia](https://en.wikipedia.org/wiki/Free_Lossless_Image_Format)
- [FLIF](http://flif.info/)

