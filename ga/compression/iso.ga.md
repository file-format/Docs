{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ISO - Formáid Comhaid Íomhá Diosca",
  "description":"Cad is comhad ISO agus APIs ann ar féidir comhaid ISO a chruthú agus a oscailt.",
  "linktitle" : "ISO",
  "menu" : {
    "docs" : {
     "identifier": "compression-iso-ga",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Cad is comhad ISO ann?

Comhad íomhá diosca cartlainne neamh-chomhbhrúite is ea comhad le síneadh .iso a léiríonn inneachar na sonraí iomlána ar dhiosca optúil ar nós CD nó DVD. Bunaithe ar an gcaighdeán [ISO-9660](https://www.iso.org/standard/17505.html), tá na sonraí diosca mar aon leis an bhfaisnéis maidir leis an gcóras comhad atá stóráilte ann i bhformáid íomhá ISO. Toisc gur féidir le comhaid ISO macasamhail beacht den ábhar a chuimsiú, is é an cineál comhaid foirfe é chun cóipeanna de dhlúthdhioscaí/DVDanna a chruthú agus úsáidtear iad go príomha chun sonraí bootable a stóráil lena suiteáil. An chuid is mó de na huaire, dóitear comhaid ISO chuig USB/CD/DVD mar ábhar bootable chun an meaisín a thosú lena shuiteáil. Tá feidhmchlár cineál MIME/x-iso9660-image ag comhaid ISO.

## Formáid Comhaid ISO

Níl formáid comhaid ISO cosúil le formáidí comhaid coimeádáin eile cé go cartlannaíonn sé inneachar sonraithe na sonraí. Cruthaítear an chartlann mar chomhad dénártha le struchtúr cruinn an ábhair agus faisnéis an chórais comhad. Déanann [ISO-9660](https://en.wikipedia.org/wiki/ISO_9660) cur síos ar fhormáid an chomhaid ISO mar seo a leanas.

### Struchtúr Barrleibhéil an Chomhaid ISO

Is éard atá i struchtúr foriomlán an chomhaid:

 * `Achar an Chórais' - 32,768 beart agus níl sé in úsáid ag ISO_9660
 * `Ceantar Sonraí` - comhdhéanta de thacar tuairisceoir toirte agus táblaí Conair, eolairí agus comhaid

### Socraigh Tuairisceoir Imleabhar

Tosaíonn an t-achar sonraí leis an tacar tuairisceoirí toirte, sraith de thuairisceoirí toirte amháin nó níos mó a chríochnaíonn le críochnóir tacair tuairisceora toirte. Feidhmíonn siad seo le chéile mar cheanntásc don limistéar sonraí, ag cur síos ar a ábhar (cosúil leis an mbloc paraiméadar BIOS a úsáideann dioscaí formáidithe FAT, HPFS agus NTFS).

Tá tacar tuairisceoirí toirte mar a thaispeántar thíos.

|Tacar Tuairisceoir Imleabhar |
---|
|Tuairisceoir imleabhar #1|
|...|
|Tuairisceoir imleabhar #N|
|Tuairisceoir toirte socraithe Críochnaitheoir|

#### Tuairisceoir Imleabhar

Is ionann méid gach tuairisceora toirte agus 2048 beart agus tá an struchtúr seo a leanas aige:

|Cuid |Cineál |Aitheantóir |Leagan |Sonraí|
---|---|---|---|---|
|Méid |1 bheart |5 bhearta ('CD001' i gcónaí) |1 bheart (0x01 i gcónaí) |2,041 beart |

## Tagairtí

* [Íomhá Diosca Optúil - Vicipéid](https://en.wikipedia.org/wiki/Optical_disc_image)

* [Sínithe Comhad](https://www.garykessler.net/library/file_sigs.html)

* [ISO 9660 - Vicipéid](https://ga.wikipedia.org/wiki/ISO_9660)


