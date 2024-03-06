{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OFT — Microsoft Outlook e-pasta veidnes fails",
  "description": "Uzziniet par OFT failu formātu un API, kas var izveidot un atvērt OFT failus.",
  "linktitle": "OFT",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-of-lvt"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir OFT fails?

Faili ar paplašinājumu .oft ir veidņu faili, kas izveidoti, izmantojot Microsoft Outlook. Iepriekš formatētais ziņojumu veidņu izkārtojums pēc tam tiek izmantots e-pasta ziņojumu izsūtīšanai ar vispārēju informāciju, lai ietaupītu laiku. Šādus failus var ģenerēt, izveidojot jaunu e-pastu, pievienojot nepieciešamo informāciju un pēc tam izmantojot Microsoft Outlook nolaižamo izvēlni Saglabāt kā Office veidni (.oft). Lietotāji var atvērt OFT failus, veicot dubultklikšķi uz tā, un tas tiks atvērts saistītajā lietojumprogrammā konkrētajā sistēmā.

## OFT faila struktūra ##

.OFT faila formātā pamatā tiek izmantots faila formāts [MSG](/email/msg/). Vienīgā atšķirība ir tā, ka bieži failiem ir CLSID_TEMPLATEMESSAGE ({0006F046-0000-0000-C000-0000000046}) kā krātuves klasi (WriteCLassStg), savukārt MSG faili izmanto CLSID_MailMessage (00020D0B-00000000-000000000046}).

CFB_3 formāts ir MSG faila pamats. Paradigma ir balstīta uz krātuvju un straumju koncepcijām, kas ir diezgan tuvu direktorijiem un failiem. Tāpēc galvenā atšķirība pirmajā ir visa hierarhija, kas ir iepakota atsevišķā failā, ko sauc par salikto failu. Objekti veido ziņojumu failus un sastāv no viena īpašuma vai tā kolekcijām. Šī iespēja atvieglo lietojumprogrammām sarežģītu, strukturētu datu glabāšanu vienā failā. Šis formāts norāda arī vairākas krātuves, katra krātuve ir ziņojuma objekts kā galvenā sastāvdaļa. Šajās krātuvēs ir vairākas straumes, kas atspoguļo šī komponenta īpašību. Iespējama arī noliktavas ligzdošana.

### OFT rekvizīti

Msg faila augšējā līmenī krātuvēs ir straumes, kurās tiek glabāti rekvizīti. Īpašumus var iedalīt šādās kategorijās:

* Fiksēta garuma īpašības

* Mainīga garuma īpašības

* Vairāku vērtību īpašības


Neatkarīgi no kategorijas īpašums ir atzīmēts vai nosaukts. Tomēr nosauktajiem rekvizītiem ir nepieciešama piemērota kartēšanas informācija, kā norādīts to kartēšanas krātuvē.

### OFT krātuves

Krātuves ir ziņojuma objekta galvenās sastāvdaļas. MSG faila formātā ir norādītas šādas krātuves:

### Augstākā līmeņa struktūra

Ziņojuma objekts attēlo visu Msg faila formāta augšējo līmeni. Atkarībā no veida, īpašībām, adresātu un pielikuma objektu skaita, ziņojuma objektam var būt dažādas straumes krātuves atbilstošajā .MSG failā.

#### Attiecības ar citām struktūrām

MSG/OFT faila formātam ir šādas attiecības ar citām struktūrām:

* .msg bāze ir saliktā faila binārais faila formāts.

* Šis formāts izmanto rekvizītus, ko izmanto ziņojumu un pielikumu objektu protokols.


## Atsauces

* [[MS-OXMSG]: Outlook MSG faila formāts](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)


