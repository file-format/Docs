{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OFT - Microsoft Outlook e-mail-skabelonfil",
  "description": "Lær om OFT-filformat og API'er, der kan oprette og åbne OFT-filer.",
  "linktitle": "OFT",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-of-dat"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en OFT fil?

Filer med filtypenavnet .oft er skabelonfiler, der er oprettet ved hjælp af Microsoft Outlook. Det forudformaterede layoutsæt til beskedskabeloner bruges derefter til at udsende e-mails med almindelige oplysninger for at spare tid. Sådanne filer kan genereres ved at oprette en ny e-mail, tilføje nødvendige oplysninger og derefter bruge rullemenuen Gem som Office-skabelon (.oft) fra Microsoft Outlook. Brugere kan åbne OFT-filerne ved at dobbeltklikke på dem, og de åbnes i tilhørende applikation på det pågældende system.

## OFT filstruktur ##

.OFT-filformatet bruger filformatet [MSG](/email/msg/) som udgangspunkt. Den eneste forskel er, at OFT-filer har CLSID_TEMPLATEMessage ({0006F046-0000-0000-C000-0000000046}) som lagerklasse (WriteClassStg), mens MSG-filer bruger CLSID_MASMESSAGE ({00020D0B-0000-000000-00000000000046}).

CFB_3-formatet er bunden af MSG-filen. Paradigmet er baseret på storage- og streams-koncepterne, ret tæt på mapper og filer. Derfor er en stor forskel i førstnævnte hele hierarkiet, pakket ind i en særskilt fil, kaldet en sammensat fil. Objekter udgør meddelelsesfilerne og består af en enkelt egenskab eller dens samlinger. Denne evne gør det lettere for applikationer at gemme indviklede, strukturerede data i en enkelt fil. Dette format specificerer også flere lager, hver lager repræsenterer meddelelsesobjektet som en hovedkomponent. Disse lagre indeholder et antal strømme, der repræsenterer en egenskab for den pågældende komponent. Indlejring af opbevaring er også muligt.

### OFT egenskaber

På det øverste niveau af .msg-filen indeholder storages streams, der gemmer egenskaber i dem. Egenskaber kan kategoriseres som følger:

* Egenskaber med fast længde

* Egenskaber med variabel længde

* Ejendomme med flere værdier


Uanset kategorien er en ejendom enten tagget eller navngivet. Der kræves dog passende kortlægningsoplysninger for navngivne egenskaber som specificeret af deres kortlægningslager.

### OFT Lager

Lagringer udgør nøglekomponenterne i meddelelsesobjektet. MSG-filformat angiver følgende lagerpladser:

### Struktur på øverste niveau

Meddelelsesobjekt repræsenterer hele det øverste niveau af Msg-filformatet. Afhængigt af typen, egenskaberne, antallet af modtager- og vedhæftede objekter, kan et meddelelsesobjekt have forskellige strømlager i dets tilsvarende .MSG-fil.

#### Forholdet til andre strukturer

MSG/OFT-filformatet har følgende relationer til andre strukturer:

* Basen af .msg er sammensat fil binært filformat.

* De egenskaber, der bruges af Message and Attachment Object Protocol, bruges af dette format.


## Referencer

* [[MS-OXMSG]: Outlook MSG-filformat](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)


