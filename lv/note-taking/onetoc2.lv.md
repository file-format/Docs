{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ONETOC2 — Microsoft OneNote faila formāts",
  "description": "Uzziniet par ONETOC2 faila formātu un API, kas var izveidot un atvērt ONETOC2 failus.",
  "linktitle": "ONETOC2",
  "menu": {
    "docs": {
      "parent": "note-taking",
      "identifier": "note-taking-onetoc-lv2"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir ONETOC2? ##

Those who have worked with [Microsoft OneNote](https://products.office.com/en-us/onenote/digital-note-taking-app) application may have noticed the presence of .onetoc2 files in the notebook folder. Microsoft OneNote creates binary .onetoc2 file as Table of Contents for keeping an index about the ordering of different note-taking sections in a notebook. A notebook is a collection of section files that are stored in the same directory. The .onetoc2 file uses a collection of properties to specify settings such as order of sections within the notebook and the color of the notebook.

Kad programmā OneNote 2016 izveidojat piezīmju grāmatiņu, tā tiek automātiski saglabāta jaunajā 2010.–2016. gada faila formātā. Šis formāts būs nepieciešams, ja vēlaties, lai visi OneNote 2016 līdzekļi, piemēram, matemātikas vienādojumi un saistītās piezīmes, darbotos pareizi.

## ONETOC2 faila formāts ##

The .onetoc2 file format is represented as OneNote Revision Store File Format and is a collection of of structures that specify a revision store organized into cross-referenced object spaces, containing objects with property sets, and containing a transaction log to ensure file integrity across asynchronous writes. Complete specifications for the .onetoc2 file format are available [online](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx) and can be referred to for development of applications.

### Faila struktūra ###

Versiju krātuves failam OBLIGĀTI jāsākas ar struktūru **Galvene**. Pārējā faila daļa ir sadalīta baitu blokos, kur katra bloka lielums un struktūra tiek norādīta laukā, kas uz to atsaucas. Bloks ir sasniedzams, ja uz to atsaucas struktūra **Header** vai ja uz to atsaucas lauks citā sasniedzamā blokā. Dati, kas atrodas ārpus **Galvenes** struktūras, un visi sasniedzamie bloki OBLIGĀTI ir jāignorē.

Visas struktūras ir izlīdzinātas uz 1 baita robežām. Visi veseli skaitļi ir parakstīti, ja vien nav norādīts citādi. Visi lauki ir [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7), ja vien nav norādīts citādi.

#### Virsraksts ####

ONE faila galvene sastāv no daļām, kurās ir dažādi unikāli ID un lauki faila informācijas attēlošanai, kā norādīts tālāk.

`guidFileType (16 baiti): GUID, kas norāda versiju krātuves faila veidu. OBLIGĀTI ir jābūt vienai no vērtībām no tālāk esošās tabulas.

|Faila formāts|Vērtība
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 baiti): GUID, kas norāda šī versiju krātuves faila identitāti. JĀBŪT globāli unikālam.

`guidLegacyFileVersion (16 baiti):` OBLIGĀTI ir {00000000-0000-0000-0000-000000000000} un OBLIGĀTI jāignorē.

`guidFileFormat (16 baiti): GUID, kas norāda, ka fails ir versiju krātuves fails. JĀBŪT {109ADD3F-911B-49F5-A5D0-1791EDC8AED8}”.

`ffvLastCodeThatWroteToThisFile (4 baiti): vesels skaitlis bez paraksta. Atkarībā no faila veida OBLIGĀTI ir jābūt vienai no vērtībām šajā tabulā.

|Faila formāts|Vērtība
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHasWrittenToThisFile (4 baiti): neparakstīts vesels skaitlis. OBLIGĀTI ir jābūt vienai no vērtībām šajā tabulā atkarībā no šī faila faila formāta.


|Faila formāts|Vērtība
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile (4 baiti): neparakstīts vesels skaitlis. OBLIGĀTI ir jābūt vienai no vērtībām šajā tabulā atkarībā no šī faila faila formāta.
:


|Faila formāts|Vērtība
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

ffvOldestCodeThatMayReadThisFile (4 baiti): Neparakstīts vesels skaitlis. OBLIGĀTI ir jābūt vienai no vērtībām šajā tabulā atkarībā no šī faila faila formāta.


|Faila formāts|Vērtība
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

## Atsauces Nr.

* [[MS-ONESTORE] — OneNote faila formāts](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)

* [Microsoft OneNote — Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)


