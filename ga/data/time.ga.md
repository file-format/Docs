{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Comhad AMA - Cad é comhad .time? An t-am nuair a cruthaíodh Comhad i Linux",
  "description" : "Foghlaim faoi chomhad TIME agus faigh amach Am nuair a cruthaíodh an comhad i Linux",
  "linktitle" : "TIME",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-time-ga",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Cad is comhad TIME?

Baineadh úsáid as formáid comhaid TIME ag córas gréasáin ar a dtugtar SOLAS, a chabhraigh le húsáideoirí a saol a thaifeadadh, a eagrú agus a roinnt. Go bunúsach, stóráil sé bailiúchán post agus léirigh sé fillteán ar leathanach saol an úsáideora laistigh den chóras.

## Conas Faigh Amach Nuair a Cruthaíodh Comhad i Linux

I Linux, is féidir leat an t-ordú `stat` a úsáid chun a fháil amach cathain a cruthaíodh comhad. Seo mar is féidir leat é a dhéanamh:

Oscail teirminéal agus clóscríobh an t-ordú seo a leanas:

```
stat <file_path>
```

Ionadaigh `<file_path> ` leis an cosán go dtí an comhad a bhfuil suim agat ann. Mar shampla:

```
stat /path/to/your/file.txt
```

Taispeánfaidh an t-ordú seo faisnéis éagsúla faoin gcomhad, lena n-áirítear a am cruthaithe. Cuardaigh an líne a thosaíonn le Breith nó Comhad:. Léiríonn an t-am Breithe nuair a cruthaíodh an comhad ar an gcóras comhaid.

Seo sampla den chuma a bheadh ar an aschur:

```
  File: /path/to/your/file.txt
  Size: 1024       	Blocks: 8          IO Block: 4096   regular file
Device: 801h/2049d	Inode: 1643318     Links: 1
Access: (0644/-rw-r--r--)  Uid: ( 1000/   user)   Gid: ( 1000/   user)
Access: 2024-01-31 12:34:56.789012345 +0000
Modify: 2024-01-31 12:34:56.789012345 +0000
Change: 2024-01-31 12:34:56.789012345 +0000
 Birth: 2024-01-31 12:34:56.789012345 +0000
```

Sa sampla seo, léiríonn an t-am Breith nuair a cruthaíodh an comhad.

