{
  "date": "2021-08-31",
  "keywords": [
"xbe fails",
"xbe faila formātā",
"kas ir xbe fails",
"failu",
"xbe piemērs",
"xbe faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par XBE failu formātu un API, kas var izveidot un atvērt XBE failus.",
  "title": "XBE — iOS lietojumprogrammu pakotnes fails",
  "linktitle": "XBE",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-xb-lve"
}
},
  "lastmod": "2021-08-31"
}

## Kas ir XBE fails?
Fails ar paplašinājumu .xbe ir izpildāma lietojumprogramma no Xbox videospēļu diska. XBE faili ir galvenie faili, kas tiek izpildīti Xbox sistēmā, un parasti tie nav jāatver datorā, taču tos var atvērt datorā, izmantojot Xbox emulācijas programmu. Šos failus parasti izveido spēļu izstrādātāji, un pēc tam tos paraksta Microsoft. Faila struktūra ir līdzīga Windows PE failiem, taču tiek piemērotas dažas svarīgas izmaiņas saskaņā ar XBox iestatījumiem, lai padarītu to darbināmu XBox.

## XBE faila formāts
XBE fails sastāv no attēla galvenes, sadaļu galveņu kolekcijas, sertifikāta, pavedienu lokālās krātuves datiem, bibliotēkas versiju kolekcijas, Microsoft bitkartes un sadaļām, kurās ir kods un resursi.

### Attēla galvene
Attēla galvenē ir ietverta informācija, kas izskaidro, kur failā atrodas citi izpildāmā faila komponenti un kā ir jāapstrādā un jāielādē palaišanas fails.

### TLS tabula
TLS tabula sastāv no visas informācijas, kas nepieciešama XBE, lai pareizi iestatītu pavedienu lokālo krātuvi. Tas būtībā ir unikāls TLS direktorijam, kas atrodams PE32 failos, un to var tieši kopēt no turienes. Šo tabulu var izlaist, ja XBE failā netiek izmantota lokālā pavedienu krātuve un attēla galvenē attiecīgais lauks ir iestatīts uz nulli.

| Ofseta | Izmērs | Vārds | Apraksts |
--------|--------|--------|------------|
| 0x0000 | 0x0004 | Neapstrādāti dati Sākt | Programmas attēla TLS mainīgā datu sākuma absolūtā (ti, nevis RVA) adrese. |
| 0x0004 | 0x0004 | Neapstrādāti dati Beigas | TLS mainīgā datu beigu adrese programmas attēlā (ti, nevis RVA). |
| 0x0008 | 0x0004 | Indeksa adrese | TLS indeksa mainīgā absolūtā (ti, nevis RVA) adrese. |
| 0x000C | 0x0004 | Atzvanīšanas adrese | TLS atzvanīšanas funkciju tabulas absolūtā (ti, nevis RVA) adrese. |
| 0x0010 | 0x0004 | Nulles aizpildījuma izmērs | Baitu skaits pēc neapstrādātajiem datiem, kas atmiņā jāiestata uz nulli. |
| 0x0014 | 0x0004 | Raksturlielumi | Apraksta izlīdzināšanu. |

### Sertifikāts

 A a certificate is mandatory for each Xbox executable that contains information about the titles:
 
- Laiks un datums, kad sertifikāts tika izveidots
- Virsraksta ID
- Titula nosaukums
- Alternatīvi nosaukumu ID
- Atļautie datu nesēju veidi, no kuriem var palaist izpildāmo failu (HD, DVD, CD utt.)
- Spēļu reģions
- Spēļu vērtējumi
- Diska numurs
- Versija
- LAN atslēgas neapstrādātie dati, kas izmantoti sistēmas saitei
- Paraksta atslēgas neapstrādātie dati (izmanto, lai parakstītu saglabāšanas spēles)
- Alternatīvās paraksta atslēgas
- Sertifikāta oriģinālais izmērs
- Tiešsaistes pakalpojuma nosaukums (nav agrīnā izpildāmā failā)
- izpildlaika drošības karodziņi (nav agrīnā izpildāmā failā)
 
### Atļautie multivides veidi
Multivides veidi, no kuriem izpildāmais fails atļauj palaist. Ir zināmas šādas vērtības:
| Multivides veids | Vērtība |
---------------------|------------|
| HARD_DISK | 0x00000001 |
| DVD_X2 | 0x00000002 |
| DVD_CD | 0x00000004 |
| CD | 0x00000008 |
| DVD_5_RO | 0x00000010 |
| DVD_9_RO | 0x00000020 |
| DVD_5_RW | 0x00000040 |
| DVD_9_RW | 0x00000080 |
| DONGLE | 0x00000100 |
| MEDIA_BOARD | 0x00000200 |
| NONSECURE_HARD_DISK | 0x40000000 |
| NONSECURE_MODE | 0x80000000 |
| MEDIA_MASK | 0x00FFFFFF |

### Sadaļas
Sadaļas tiek izteiktas ar sadaļu virsrakstiem. Sadaļu galvenes sākas uzreiz aiz sertifikāta un satur informāciju, kur failā atrodas faktiskās sadaļas. Xbox izpildāmajā failā vienmēr ir vismaz divas sadaļas:
- .teksts
- .rdata


## Atsauces 

* [Xbe — XBox Executable](https://xboxdevwiki.net/Xbe)



