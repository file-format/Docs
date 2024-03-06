{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MSG — Microsoft Outlook e-pasta formāts",
  "description": "Uzziniet par MSG failu formātu un API, kas var izveidot un atvērt MSG failus.",
  "linktitle": "MSG",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-ms-lvg"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir MSG fails?

MSG is a file format used by [Microsoft Outlook](https://products.office.com/en-us/outlook/email-and-calendar-software-microsoft-outlook?rtc#1) and Exchange to store email messages, contact, appointment, or other tasks. Such messages may contain one or more email fields, with the sender, recipient, subject, date, and message body, or contact information, appointment particulars, and one or more task specifications. The properties that constitute the Message object, including are also a part of the MSG file.  MSG file has headers, main message body, and hyperlinks as plain ASCII text. MSG files are also suitable with the programs that need Microsoft's Messaging Applications Programming Interface (MAPI).

## MSG faila struktūra

CFB_3 formāts ir MSG faila pamats. Paradigma ir balstīta uz krātuvju un straumju koncepcijām, kas ir diezgan tuvu direktorijiem un failiem. Tāpēc galvenā atšķirība pirmajā ir visa hierarhija, kas ir iepakota atsevišķā failā, ko sauc par salikto failu. Objekti veido ziņojumu failus un sastāv no viena īpašuma vai tā kolekcijām. Šī iespēja atvieglo lietojumprogrammām sarežģītu, strukturētu datu glabāšanu vienā failā. Šis formāts norāda arī vairākas krātuves, katra krātuve ir ziņojuma objekts kā galvenā sastāvdaļa. Šajās krātuvēs ir vairākas straumes, kas atspoguļo šī komponenta īpašību. Iespējama arī noliktavas ligzdošana.

## Mapi rekvizīti

.msg faila augšējā līmenī krātuvēs ir straumes, kurās tiek glabāti rekvizīti. Īpašumus var iedalīt šādās kategorijās:

* Fiksēta garuma īpašības

* Mainīga garuma īpašības

* Vairāku vērtību īpašības


Neatkarīgi no kategorijas īpašums ir atzīmēts vai nosaukts. Tomēr nosauktajiem rekvizītiem ir nepieciešama piemērota kartēšanas informācija, kā norādīts to kartēšanas krātuvē.

## Krātuves

Krātuves ir ziņojuma objekta galvenās sastāvdaļas. MSG faila formātā ir norādītas šādas krātuves:

## Augstākā līmeņa struktūra

Ziņojuma objekts apzīmē visu MSG faila formāta augšējo līmeni. Atkarībā no veida, īpašībām, adresātu un pielikuma objektu skaita, ziņojuma objektam var būt dažādas straumes krātuves atbilstošajā .MSG failā.

### Attiecības ar citām struktūrām

Msg faila formātam ir šādas attiecības ar citām struktūrām:

* Faila .msg pamatā ir saliktā faila binārais faila formāts.

* Šis formāts izmanto rekvizītus, ko izmanto ziņojumu un pielikumu objektu protokols.


## Scenāriji, lai izvairītos no MSG formātiem

Ziņojuma objektu var koplietot starp klientiem vai ziņojumu veikaliem, kas izmanto .msg failu sistēmu. Ir daži apstākļi, kuros ziņojuma objekta glabāšana .msg faila formātā nebūtu piemērota. Piemēram:

* Ja tiek uzturēts liels savrups arhīvs, labāk ir izmantot pilnvērtīgu formātu, kurā skatus var renderēt precīzāk.

* Ja uztvērējs nav zināms, iespējams, uztvērējs neatbalsta formātu un var tikt piegādāts privāts vai neatbilstošs.


## MSG faila piemērs

To get an idea of how a MSG file looks like, you can download a [sample MSG file](https://products.conholdate.app/viewer/view/mL7cmq6qYbcNG329P/sample-msg-file.msg) and open on your computer to view its contents.

## Atsauces

* [[MS-OXMSG]: Outlook MSG faila formāts](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)


