{
  "date": "2021-06-21",
  "keywords": [
"UDL",
"pagarinājumu",
"udl failu",
"udl faila formātā",
"Datu bāzes faila tips",
"Datu bāzes faila formāts",
"kas ir udl fails"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par UDL faila formātu un API, kas var izveidot un atvērt UDL failus.",
  "title": "UDL — Microsoft universālās datu saites fails",
  "linktitle": "UDL",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-ud-lvl"
}
},
  "lastmod": "2021-06-21"
}

## Kas ir UDL fails?
Failu ar paplašinājumu .udl sauc par Microsoft Universal Data Link failu; savienojuma atribūtu norādīšana; izmanto Windows lietojumprogrammas, lai izveidotu savienojumu ar datu bāzi. UDL failā ir OLE DB datu avota savienojuma virkne; ar lietotājvārdu un paroli un būtiskām savienojuma virknes īpašībām. Lai izvairītos no tiešas rekvizītu norādīšanas ar roku savienojuma virknē, kā alternatīvu var izmantot dialoglodziņu Data Link Properties, lai saglabātu savienojuma informāciju .udl failā.

## UDL faila formāts
Būtībā UDL (Universal Data Link) fails ir vienkāršs teksta fails, kas sastāv no datu bāzes savienojuma virknes ar noteiktiem atribūtiem vai rekvizītiem. Kad UDL fails ir izveidots, to var pārbaudīt, izmantojot SQL Server Management Studio, lai pārbaudītu savienojamību.

### Savienojuma virknes rekvizīti
Lai nodrošinātu pareizu savienojamību, UDL var iestatīt šādus rekvizītus:

- **Servera nosaukums**: tā servera atrašanās vieta, kurā atrodas datu bāze, kurai vēlaties piekļūt.
- **Autentifikācijas opcijas**
- **Windows autentifikācija**: autentifikācija SQL Server, izmantojot pašlaik pieteikušās lietotāja Windows konta akreditācijas datus.
- **SQL servera autentifikācija**: autentifikācija, izmantojot pieteikšanās ID un paroli.
- **Active Directory — Integrated**: integrēta autentifikācija ar Azure Active Directory identitāti; var izmantot arī Windows autentifikācijai SQL Server.
- **Active Directory — Parole**: lietotāja ID un paroles autentifikācija ar Azure Active Directory identitāti.
- **Active Directory — universāls ar MFA atbalstu**: interaktīva autentifikācija ar Azure Active Directory identitāti.
- **Aktīvais direktorijs — pakalpojuma galvenais**: autentifikācija, izmantojot Azure Active Directory pakalpojuma galveno.
- **Servera SPN**: ja izmantojat uzticamu savienojumu, varat norādīt servera pakalpojuma galveno nosaukumu (SPN).
- **Lietotājvārds**: ierakstiet lietotāja ID, kas jāizmanto autentifikācijai, kad pierakstāties datu avotā.
- **Parole**: ierakstiet paroli, ko izmantot autentifikācijai, kad pierakstāties datu avotā.
- **Tukša parole**: ja šī opcija ir atzīmēta, norādītais pakalpojumu sniedzējs savienojuma virknē var izmantot tukšu paroli.
- **Atļaut saglabāt paroli**: ļauj saglabāt paroli kopā ar savienojuma virkni.
- **Izmantojiet spēcīgu datu šifrēšanu**: dati, kas tiek nodoti caur savienojumu, tiks šifrēti.
- **Trust server certificate**: The server's certificate will be validated.
- **Datu bāze**: datu bāzes nosaukums, kurai vēlaties piekļūt.
- **Pievienot datu bāzes failu kā datu bāzes nosaukumu**: norāda pievienojamās datu bāzes primārā faila nosaukumu.

## Atsauces Nr.

* [Microsoft Data Access Components](https://en.wikipedia.org/wiki/Microsoft_Data_Access_Components#Universal_data_link)

* [Universālās datu saites (UDL) konfigurācija](https://learn.microsoft.com/en-us/sql/connect/oledb/help-topics/data-link-pages?view=sql-server-ver15)


