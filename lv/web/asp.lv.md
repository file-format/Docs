{
  "date": "2019-10-11",
  "keywords": [
"asp",
"asp failu",
"asp faila formātā",
"asp faila tips",
"failu",
"veids",
"kas ir asp fails"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASP — aktīvā servera lapu faila formāts",
  "description": "Uzziniet, kas ir ASP fails un API, kas var tos izveidot un atvērt.",
  "linktitle": "ASP",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-as-lvp"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir ASP fails?

ASP apzīmē Active Server Pages, kas ir izstrādes ietvars tīmekļa lapu izveidei. Tas ļauj iekšējam serverim izpildīt datora kodu, lai apkalpotu tīmekļa pieprasījumus. Kad tīmekļa pārlūkprogramma ģenerē ASP faila pieprasījumu, serveris nolasa failu un izpilda tajā esošo kodu/skriptu, lai ģenerētu rezultātu **[HTML](/web/html/)**, kas tiek atgriezts pārlūkprogrammā parādīšanai.

Atšķirībā no HTML lapām, kas ir statiskas lapas, ko apkalpo serveris, ASP faili izpildes laikā ģenerē dinamisku saturu, kas var ietvert datu pieprasījumus no datu bāzes. ASP lapās parasti tiek izmantots paplašinājums .asp, nevis .html. Tā kā kods/skripts ASP failā tiek izpildīts servera pusē, pieprasītāja pārlūkprogramma nevar redzēt kodu, kas izmantots apkalpotās lapas izveidei. Visas mūsdienu pārlūkprogrammas spēj attēlot rezultātā ģenerētās lapas. Izmantojot Microsoft tehnoloģiju, lapas, kas izveidotas ar ASP, tiek mitinātas Microsoft interneta informācijas pakalpojumu (IIS) serveros.

## Īsa ASP faila formāta vēsture
ASP ir veiktas tikai dažas pārskatīšanas, līdz to aizstāja ASP.NET, kas ir modernāks un efektīvāks servera sānu lapu izstrādes un pārvaldības veids. ASP atbalsts ir iekļauts pēc noklusējuma kopā ar interneta informācijas pakalpojumiem (IIS). ASP tika publicēts trīs dažādās versijās ar uzlabojumiem katrā.

* ASP 1.0 tika izlaists 1996. gada decembrī kā daļa no IIS 3.0

* ASP 2.0 tika izlaists 1997. gada septembrī kā daļa no IIS 4.0

* ASP 3.0 tika izlaists 2000. gada novembrī kā daļa no IIS 5.0


## ASP funkcionālie objekti

ASP faili izmanto servera puses objektus, lai apstrādātu lietotāju pieprasījumus un ģenerētu izvades lapas, kas tiks pasniegtas lietotājiem. Katram objektam ir kolekciju, rekvizītu un metožu kopa pieprasījumu un atbilžu apstrādei. Šie objekti ietver:

### Pieprasīt objektu

Kad pārlūkprogramma pieprasa servera lapu, to sauc par pieprasījumu. Pieprasījuma objekts tiek izmantots, lai iegūtu informāciju no apmeklētāja.

### Atbildes objekts

ASP atbildes objekts tiek izmantots, lai nosūtītu izvadi lietotājam no servera.

### Servera objekts

ASP servera objekts tiek izmantots, lai piekļūtu servera rekvizītiem un metodēm. Tas ļauj izveidot savienojumus ar datu bāzēm (ADO), failu sistēmu un izmantot serverī instalētos komponentus.

### Sesijas objekts

Sesijas objekts ir kā saite starp lietotāja pārlūkprogrammu, kas pieprasa lapu no servera, un pašu serveri. Tas tiek panākts ar sīkfailu, ko izveido ASP un nosūta uz lietotāja datoru. Sesijas objekts saglabā informāciju par lietotāja sesiju vai maina tās iestatījumus. Informācija, kas tiek glabāta sesijas objektā, tiek koplietota visās lietojumprogrammas lapās. Kopējā informācija, kas tiek glabāta sesijas mainīgajos, ir nosaukums, ID un preferences. Serveris katram jaunam lietotājam izveido jaunu sesijas objektu un iznīcina sesijas objektu, kad sesija beidzas.

### Lietojumprogrammas objekts

Lietojumprogrammas objektā ir informācija, kas tiks izmantota daudzās lietojumprogrammas lapās (piemēram, datu bāzes savienojuma informācija). Informācijai var piekļūt no jebkuras lapas. Informāciju var arī mainīt vienuviet, un izmaiņas automātiski tiks atspoguļotas visās lapās. Lietojumprogrammas objekts tiek izmantots, lai saglabātu un piekļūtu mainīgajiem no jebkuras lapas, tāpat kā sesijas objektu.

### ASPERror objekts

Objekts ASPERror tika ieviests ASP 3.0 un ir pieejams IIS5 un jaunākās versijās. ASPERror objekts tiek izmantots, lai parādītu detalizētu informāciju par jebkuru kļūdu, kas rodas skriptos ASP lapā.

**Piezīme.** Objekts ASPERror tiek izveidots, kad tiek izsaukts Server.GetLastError, tāpēc informācijai par kļūdu var piekļūt, tikai izmantojot metodi Server.GetLastError.

## Atsauces

* [ASP — W3C](https://www.w3schools.com/asp/default.asp)

* [Vienkāršu ASP lapu izveide](https://learn.microsoft.com/en-us/previous-versions/iis/6.0-sdk/ms524741(v=vs.90))


