{
  "date": "2021-03-02",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "RDLC — ziņojuma definīcijas valoda klienta pusē",
  "keywords": [
"rdlc",
"ziņojuma definīcijas valoda",
"mkv formātā",
"XSD",
"atskaites definīcijas valoda klienta pusē"
],
  "description": "Uzziniet par RDLC faila formātu, kas ir SQL Server Reporting Services pārskata definīcijas XML attēlojums.",
  "linktitle": "RDLC",
  "menu": {
    "docs": {
      "parent": "reporting",
      "identifier": "reporting-rdl-lvc"
}
},
  "lastmod": "2021-03-02"
}

## Kas ir RDLC fails? ##

RDLC apzīmē ziņojuma definīcijas valodas klienta pusi. Faktiski tas ir atskaites faila paplašinājums, kas izveidots, izmantojot Microsoft atskaišu tehnoloģiju. Lai izveidotu šos failus, tiek izmantota Report Designer SQL Server 2005 versija. **ReportViewer** vadīkla klienta pusē var tieši izpildīt RDLC pārskatus.

## RDL VS RDLC faili
|.rdl faili |.rdlc faili|
---|---|
|RDL failus izveido Report Designer SQL Server 2005 versija|RDLC failus izveido Report Designer Visual Studio 2005 versija|
|Tas tiek izmantots SQL Server Reporting Services|Tas tiek izmantots Visual Studio|
|Tas ir attālināts ziņojums|Tas ir vietējais ziņojums|
|Lai to palaistu, nepieciešama Reporting Services instance|Nav nepieciešama Reporting Services instance|

## Klienta atskaites definīcijas (.rdlc) failu izveide
ReportViewer vadīkla tiek izmantota, lai palaistu klienta atskaites definīcijas (.rdlc) failus, izmantojot vadīklā iebūvētās apstrādes iespējas. Lietojumprogrammas projektā var viegli izveidot klienta pārskatus, kurus darbināt vietējā apstrādes režīmā. Tālāk ir norādītas pārskata izveides metodes.

- Izmantojiet **Pārskatu vedni**, lai izveidotu jaunu klienta pārskata definīciju (.rdlc).

- Izveidojiet jaunu klienta atskaites definīcijas (.rdlc) failu, izmantojot Visual Studio.

- Programmatiski ģenerējiet pārskata definīciju.


Pārskatu var priekšskatīt, tikai palaižot to **ReportViewer** vadīklā. Lūdzu, ņemiet vērā, ka jebkurā laikā varat atvērt un rediģēt pārskata definīciju un pēc tam izveidot vai izvietot lietojumprogrammu, lai pārbaudītu rezultātus.

## Atsauces Nr.

- [Creating Client Report Definition (.rdlc) Files](https://learn.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/ms252067(v=vs.100))

