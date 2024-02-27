{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MSG - Microsoft Outlook e-mail-format",
  "description": "Lær om MSG filformat og API'er, der kan oprette og åbne MSG filer.",
  "linktitle": "MSG",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-ms-dag"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en MSG fil?

MSG is a file format used by [Microsoft Outlook](https://products.office.com/en-us/outlook/email-and-calendar-software-microsoft-outlook?rtc#1) and Exchange to store email messages, contact, appointment, or other tasks. Such messages may contain one or more email fields, with the sender, recipient, subject, date, and message body, or contact information, appointment particulars, and one or more task specifications. The properties that constitute the Message object, including are also a part of the MSG file.  MSG file has headers, main message body, and hyperlinks as plain ASCII text. MSG files are also suitable with the programs that need Microsoft's Messaging Applications Programming Interface (MAPI).

## MSG filstruktur

CFB_3-formatet er bunden af MSG-filen. Paradigmet er baseret på storage- og streams-koncepterne, ret tæt på mapper og filer. Derfor er en stor forskel i førstnævnte hele hierarkiet, pakket ind i en særskilt fil, kaldet en sammensat fil. Objekter udgør meddelelsesfilerne og består af en enkelt egenskab eller dens samlinger. Denne evne gør det lettere for applikationer at gemme indviklede, strukturerede data i en enkelt fil. Dette format specificerer også flere lager, hver lager repræsenterer meddelelsesobjektet som en hovedkomponent. Disse lagre indeholder et antal strømme, der repræsenterer en egenskab for den pågældende komponent. Indlejring af opbevaring er også muligt.

## Mapi Egenskaber

På det øverste niveau af .msg-filen indeholder storages streams, der gemmer egenskaber i dem. Egenskaber kan kategoriseres som følger:

* Egenskaber med fast længde

* Egenskaber med variabel længde

* Ejendomme med flere værdier


Uanset kategorien er en ejendom enten tagget eller navngivet. Der kræves dog passende kortlægningsoplysninger for navngivne egenskaber som specificeret af deres kortlægningslager.

## Opbevaring

Lagringer udgør nøglekomponenterne i meddelelsesobjektet. MSG-filformat angiver følgende lagerpladser:

## Struktur på øverste niveau

Meddelelsesobjekt repræsenterer hele det øverste niveau af MSG-filformatet. Afhængigt af typen, egenskaberne, antallet af modtager- og vedhæftede objekter, kan et meddelelsesobjekt have forskellige strømlager i dets tilsvarende .MSG-fil.

### Forholdet til andre strukturer

Msg-filformatet har følgende relationer til andre strukturer:

* Basen af .msg er sammensat fil binært filformat.

* De egenskaber, der bruges af Message and Attachment Object Protocol, bruges af dette format.


## Scenarier for at undgå MSG-formater

Meddelelsesobjekt kan deles mellem klienter eller meddelelseslagre, der bruger .msg-filsystemet. Der er få omstændigheder, hvor det ikke ville være passende at gemme et meddelelsesobjekt i .msg-filformatet. For eksempel:

* I tilfælde af at opretholde et stort selvstændigt arkiv, er det bedre at bruge et fuldt udstyret format, hvor visninger kan gengives mere præcist.

* Hvis modtageren er ukendt, er det muligt, at formatet ikke understøttes af modtagerens ende, og privat eller irrelevant kan blive leveret.


## Eksempel på MSG-fil

To get an idea of how a MSG file looks like, you can download a [sample MSG file](https://products.conholdate.app/viewer/view/mL7cmq6qYbcNG329P/sample-msg-file.msg) and open on your computer to view its contents.

## Referencer

* [[MS-OXMSG]: Outlook MSG-filformat](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)


