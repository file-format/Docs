{
  "date": "2019-10-11",
  "keywords": [
"Comhad rar",
"Formáid comhaid rar",
"Cad is comhad rar ann",
"comhad",
"sampla rar",
"Síneadh comhad rar saor in aisce,",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RAR",
  "description": "Cad é síneadh comhad RAR agus APIs is féidir comhaid RAR a chruthú agus a oscailt.",
  "linktitle": "RAR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-ra-gar"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad RAR ann?

Is comhaid cartlainne iad comhaid le síneadh .rar a chruthaítear chun faisnéis a stóráil i bhfoirm chomhbhrúite nó i ngnáthfhoirm. Is formáid comhaid dílseánaigh é RAR, a sheasann do fhormáid comhaid Roshal ARchive, a chruthaigh Eugene Roshal i 1995 a bhí ina innealtóir bogearraí Rúiseach. Úsáidtear an fhormáid chun comhaid a chartlannú le modhanna éagsúla lena n-áirítear teicnící comhbhrú éagsúla. Tá roinnt bogearraí feidhmchláir ar fáil do Windows, Linux agus MacOS chun comhaid RAR a bhaint astu. Is é bogearraí WinRAR, le RARLab, an áirgiúlacht cartlannaithe comhad shareware (saor in aisce ar feadh 40 lá) le haghaidh ardán Microsoft Windows; ba é an t-Údar céanna, Eugene Roshal, a rinne na bogearraí a aistriú chuig Linux (mar eastóscadh amháin).

## Stair na Leaganacha d'Fhormáid Chomhaid RAR

* v1.3 (bunaidh, níl síniú "Rar!")

* v1.5

* v2.0 - scaoileadh le WinRAR 2.0 agus Rar le haghaidh MS-DOS 2.0

* v2.9 - scaoileadh i WinRAR leagan 3.00

* v5.0 - le tacaíocht ó WinRAR 5.0 agus níos déanaí


## Príomhghnéithe d'Fhormáid RAR

Tá RAR sa réimse le fada an lá agus tá sé ar cheann de na formáidí cartlannaithe is fearr leat. Is iad seo a leanas na príomhghnéithe a bhaineann leis an bhformáid RAR:

**`Cóimheas comhbhrú ard:`** Níos fearr i gcomparáid le [ZIP](/compression/zip/), inchomparáide le formáid 7z agus zipx.

**`Criptiú comhad láidir de réir dearaidh:`** Braitheann cartlanna criptithe RAR4 ar chriptiú bunaithe ar AES-128 agus braitheann cartlanna criptithe RAR5 ar chriptiú AES-256 le sceidealú eochrach feabhsaithe

**`Ard-cheartú earráide agus cumais aisghabhála sonraí:`** Taifid aisghabhála roghnacha le linn cruthú cartlainne

**`Méid an Chomhaid:`** Íosmhéid 20 beart agus uasmhéid 2^63 beart (8 exabytes de mhéid iomlán na cartlainne)

**`Cartlanna RAR Il-imleabhar:`** Deis cartlanna móra a roinnt ina roinnt comhad níos lú chun aistriú thar an líonra a éascú. Sa chás sin, déantar na síntí comhaid a mhéadú faoi 1 chun méideanna scoilte a léiriú

## Formáid Comhaid RAR

Níl sonraíochtaí iomlána formáid RAR ar fáil go poiblí agus is é sin an fáth nach féidir sonraí faoin bhformáid a fhoirmiú go beacht.

### Leagan Amach Ginearálta na Cartlainne

Seo a leanas leagan amach ginearálta formáid comhaid RAR a tugadh isteach i leagan 5.0:

| Formáid Chomhaid
---|
| Modúl féin-eastósctha (roghnach)
|RAR 5.0 Síniú
| Ceanntásc Criptithe Cartlainne (roghnach)
|Príomhcheanntásc na Cartlainne
| Ceanntásc seirbhíse tuairimí cartlainne (roghnach)
Ceanntásc Comhad 1
| Ceanntásca Seirbhíse (NTFS ACL, sruthanna, etc.) don chomhad roimhe seo (roghnach)
|...
| Ceanntásc an Chomhaid N
| Ceanntásca Seirbhíse (NTFS ACL, sruthanna, etc.) don chomhad roimhe seo (roghnach)
|Taifead Aisghabhála (roghnach)
|Deireadh cheanntásc na cartlainne

Is féidir faisnéis faoi gach cuid de chomhad RAR a luaitear thuas a fháil sa doiciméad [RAR 5.0 File Format specifications](https://www.rarlab.com/technote.htm#arcstruct).

#### Cartlanna RAR á dtarraingt féin agat

Má tá an comhad RAR é féin asbhainte, tá an fhaisnéis féin-astarraingthe le fáil ag tús an chomhaid roimh shíniú na cartlainne. Ní shainítear a mhéid agus a bhfuil ann.

#### RAR 5.0 Síniú

Is ceanntásc 8 n-bheart é síniú RAR a chuimsíonn an uimhir draíochta seo a leanas:

0x 52 61 72 21 1A 07 00

cá

0x6152 - HEAD_CRC

0x72 - HEAD_TYPE

0x1A21 - HEAD_FLAGS

0x0007 - HEAD_SIZE

## Tagairtí

* [Formáid Cartlainne RAR 5.0]( https://www.rarlab.com/technote.htm)

* [RAR - Le Vicipéid]( https://en.wikipedia.org/wiki/RAR_(file_format))


