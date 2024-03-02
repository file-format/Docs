{
  "date" : "2022-12-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Comhad ZST - Formáid Chomhaid Chomhbhrúite Zstandard",
  "description":"Foghlaim faoi fhormáid comhaid ZST agus APIs ar féidir leo comhaid ZST a chruthú agus a oscailt.",
  "linktitle" : "ZST",
  "menu" : {
    "docs" : {
      "identifier":"compression-zst-ga",
      "parent" : "compression"
}
},
  "lastmod" : "2022-12-26"
}

## Cad is comhad ZST ann?

Is comhad comhbhrúite é comhad ZST a ghintear leis an algartam comhbhrú Zstandard (zstd). Is comhad comhbhrúite é a chruthaítear le comhbhrú gan chailliúint ag an algartam. Is féidir comhaid ZST a úsáid chun cineálacha éagsúla comhaid a chomhbhrú amhail bunachair shonraí, córais comhad, líonraí agus cluichí. Tá an Zstandard á rialú ag [RFC 8878](https://www.rfc-editor.org/rfc/rfc8878) a chuireann síos ar mheicníocht iomlán comhbhrú, cineál meán, agus ionchódú ábhair.

## Formáid Comhaid ZST

Stóráiltear comhaid ZST i bhformáid chomhaid chomhbhrúite chuig diosca. Tá an mheicníocht comhbhrúite mar a thuairiscítear ag RFC 8878 a théann i léig RFC 8478.

## Frámaí ZST

Tá comhad ZST comhdhéanta de fhráma amháin nó níos mó. Is féidir le gach fráma a bheith ina fhráma Zstandard nó ina fhráma inscipeála. Tá sonraí comhbhrúite i bhfráma Zstandard, ach tá meiteashonraí saincheaptha úsáideora i bhfráma inscipeála.

### Fráma Zstandard

Tá an struchtúr seo a leanas ag fráma Zstandard.

|Réimse|Méid i mBeart|
---|---|
|Draíocht_Uimhir |4 beart|
|Fráma_Ceanntásc |2-14 beart|
|Sonraí_Bloc |n beart|
|[Tuilleadh Sonraí_Bloic] ||
|[Ábhar_Seiceáil] |4 beart|

### Fráma Scipeála

Ligeann fráma inspioráideach meiteashonraí atá sainithe ag an úsáideoir a chur isteach i sreabhadh frámaí comhghafa. Seo a leanas struchtúr fráma inscipeála.

|Draíocht_Uimhir|Fráma_Méid|Sonraí_Úsáideora|
---|---|---|
|4 beart |4 beart |n beart|

## Tagairtí ##

* [Comhbhrú RFC 8878 Zstandard]( https://www.rfc-editor.org/rfc/rfc8878)


