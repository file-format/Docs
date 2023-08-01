{
  "date" : "2020-11-11",
  "keywords" :[ "DTSX", "extensie", "fișier", "format fișier", "Tip fișier bază de date", "Format fișier bază de date", "Fișiere bază de date"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier DTSX și despre API-urile care pot crea și deschide fișiere DTSX.",
  "title" :"Format de fișier DTSX - Fișier de setări DTS SQL Server",
  "linktitle" : "DTSX",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Ce este un fișier DTSX?

Un fișier cu extensia .dtsx (Data Transformation Services Package XML) este un fișier Data Transformation Services (DTS) care este utilizat de Microsoft SQL pentru a se referi la pașii/regulile de migrare a datelor pentru transferul de date dintr-o bază de date în alta. Aceasta include transformările și orice pași opționali de procesare care pot fi necesari în timpul transferului de date între punctele de origine și cele de destinație. SQL Server Integration Services (SSIS), o componentă a Microsoft SQL Server, utilizează fișierele DTSX pentru a identifica pașii de procesare a datelor între serverele de baze de date. Fișierele DTSX pot fi deschise cu Microsoft SQL Server 2019.

## Format de fișier DTSX

Mișcarea datelor între serverele de baze de date necesită reguli și pași de procesare pentru a asigura integritatea datelor în timpul acestei operațiuni. SSIS asigură că toate aceste activități, de mutare și conformare a datelor din diferite surse dintr-o întreprindere, au loc în mod convenabil. Aici vine DTSX care definește structurile care urmează să fie utilizate de SSIS pentru a stabili pașii în care datele pot fi procesate după cum urmează acești pași.

Fluxul de date descris de DTSX este așa cum se arată în imaginea următoare.

{{< figure src="../DataFlowDTSX.png" alt="Flux de date DTSX" >}}

DTSX este bazat pe [XML](/ro/web/xml/) și este documentat în [MS-DTSX](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd). Refactorizarea îmbunătățită a DTSX XML este DTSX 2.0 care include noi atribute pentru structuri, înlocuirea proprietăților numite ca atribute XML părinte, specifică valorile implicite pentru majoritatea valorilor atributelor și plasarea elementelor repetate în interiorul unui element părinte. Structurile DTSX sunt descrise folosind aceste [Scheme XML](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/e5095968-26ea-4824-a717-153ccee642dc#Appendix_A_1) și formatul structural este XML-text celar.

## Referințe

* [Format DTSX - Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)
* [Format DTSX 2 - De la Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx2/fb216aa4-62ab-41c8-a6d5-5b1002739d21)

