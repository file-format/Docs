{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ONETOC2 - Formáid Chomhaid Microsoft OneNote",
  "description": "Foghlaim faoi fhormáid comhaid ONETOC2 agus APIanna ar féidir comhaid ONETOC2 a chruthú agus a oscailt.",
  "linktitle": "ONETOC2",
  "menu": {
    "docs": {
      "parent": "note-taking",
      "identifier": "note-taking-onetoc-ga2"
}
},
  "lastmod": "2019-09-10"
}

## Cad é ONETOC2? ##

Those who have worked with [Microsoft OneNote](https://products.office.com/en-us/onenote/digital-note-taking-app) application may have noticed the presence of .onetoc2 files in the notebook folder. Microsoft OneNote creates binary .onetoc2 file as Table of Contents for keeping an index about the ordering of different note-taking sections in a notebook. A notebook is a collection of section files that are stored in the same directory. The .onetoc2 file uses a collection of properties to specify settings such as order of sections within the notebook and the color of the notebook.

Nuair a chruthaíonn tú leabhar nótaí in OneNote 2016, déantar é a shábháil go huathoibríoch san fhormáid comhaid nua 2010-2016. Beidh an fhormáid seo uait más mian leat go n-oibreoidh na gnéithe go léir in OneNote 2016, amhail cothromóidí matamaitice agus nótaí nasctha, i gceart.

## Formáid Chomhaid ONETOC2 ##

The .onetoc2 file format is represented as OneNote Revision Store File Format and is a collection of of structures that specify a revision store organized into cross-referenced object spaces, containing objects with property sets, and containing a transaction log to ensure file integrity across asynchronous writes. Complete specifications for the .onetoc2 file format are available [online](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx) and can be referred to for development of applications.

### Struchtúr Comhad ###

NÍ MÓR do stór comhad athbhreithnithe tosú le struchtúr **Ceanntásc. Roinntear an chuid eile den chomhad i mbloic beart, áit a bhfuil méid agus struchtúr gach bloc sonraithe ag an réimse a thagraíonn dó. Is féidir teacht ar bhloc má tá tagairt dó sa struchtúr **Header**, nó má tá tagairt dó ag réimse i mbloc eile is féidir a rochtain. NÍ MÓR neamhaird a dhéanamh ar shonraí lasmuigh den struchtúr **Headder** agus ar aon bhloc insroichte.

Tá gach struchtúr ailínithe ar theorainneacha 1 beart. Sínítear gach slánuimhir mura sonraítear a mhalairt. Tá na réimsí go léir [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7) mura sonraítear a mhalairt.

#### Ceanntásc ####

Cuimsíonn Ceanntásc comhad .ONE smután ina bhfuil aitheantais uathúla éagsúla agus réimsí chun faisnéis comhaid a léiriú mar seo a leanas:

`guidFileType (16 bytes):` GUID a shonraíonn cineál an chomhaid stórais athbhreithnithe. NÍ MÓR a bheith ar cheann de na luachanna ón tábla seo a leanas.

|Formáid Chomhaid|Luach
--- | --- |
|.amháin|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`GuidFile (16 bytes):` GUID a shonraíonn céannacht an chomhaid stórais athbhreithnithe seo. BA CHÓIR a bheith uathúil ar fud an domhain.

`guidLegacyFileVersion (16 beart):` NÍ MÓR a bheith {00000000-0000-0000-0000-00000000000} agus NÍ MÓR neamhaird a dhéanamh air.

`guidFileFormat (16 bytes):` GUID a shonraíonn gur comhad stórais athbhreithnithe é an comhad. NÍ MÓR é a bheith {109ADD3F-911B-49F5-A5D0-1791EDC8AED8}.

`ffvLastCodeThatWroteToThisFile (4 bytes):` Slánuimhir gan síniú. NÍ MÓR a bheith ar cheann de na luachanna sa tábla seo a leanas, ag brath ar an gcineál comhaid.

|Formáid Chomhaid|Luach
--- | --- |
|.aon|0x0000002A
|.onetoc2|0x0000001B

`ffvCodeOldestThatHesWrittenToThisFile (4 bytes):` Slánuimhir gan síniú. NÍ MÓR a bheith ar cheann de na luachanna sa tábla seo a leanas, ag brath ar fhormáid comhaid an chomhaid seo.


|Formáid Chomhaid|Luach
--- | --- |
|.aon|0x0000002A
|.onetoc2|0x0000001B

`ffvCodeIs déanaíAtá ScríobhadhChunAnFile Seo (4 beart):` Slánuimhir gan síniú. NÍ MÓR a bheith ar cheann de na luachanna sa tábla seo a leanas, ag brath ar fhormáid comhaid an chomhaid seo.
:


|Formáid Chomhaid|Luach
--- | --- |
|.aon|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 bytes):` Slánuimhir gan síniú. NÍ MÓR a bheith ar cheann de na luachanna sa tábla seo a leanas, ag brath ar fhormáid comhaid an chomhaid seo.


|Formáid Chomhaid|Luach
--- | --- |
|.aon|0x0000002A
|.onetoc2|0x0000001B

## Tagairtí ##

* [[MS-ONESTORE] - Formáid Chomhaid OneNote](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)

* [Microsoft OneNote - Vicipéid](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)


