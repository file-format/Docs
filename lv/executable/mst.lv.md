{
  "date": "2021-06-30",
  "keywords": [
"mst failu",
"mst faila formātā",
"kas ir mst fails",
"failu",
"mst piemērs",
"mst faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par MST faila formātu un API, kas var izveidot un atvērt MST failus.",
  "title": "MST — Windows Installer pakotnes fails",
  "linktitle": "MST",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ms-lvt"
}
},
  "lastmod": "2021-06-30"
}

## Kas ir MST fails?
Faili ar paplašinājumu .mst tiek izmantoti, lai pārveidotu MSI pakotnes saturu. Sistēmas administratori tos parasti izmanto, lai esošam MSI failam lietotu pielāgotos iestatījumus. MST faili tiek izmantoti kopā ar sākotnējo MSI pakotni to programmatūras izplatīšanas sistēmās, piemēram, grupu politikās. MST faili parasti tiek izmantoti programmatūras izstrādē un testēšanā, lai konfigurētu to izstrādes stadijā esošās programmatūras versijas.

## MST faila formāts
MST vai Transform fails tiek izmantots, lai apkopotu instalēšanas opcijas programmām, kuras failā izmanto Microsoft Windows Installer. Šie faili parasti tiek izmantoti Installer (MSIEXEC.EXE) komandrindā vai tiek izmantoti programmatūras instalēšanas grupas politikā; Microsoft Active Directory domēnā. MST failus var izmantot arī ar iesaiņotiem izpildāmajiem instalētājiem. Vispārīgs gadījums ir tāds, ka kāds vēlas nosūtīt komandrindas parametrus iesaiņotajam instalētājam. Lai to izdarītu, ir nepieciešams MST fails, kas rekvizītu tabulai pievieno rekvizītu WRAPPED_ARGUMENTS. Šos failus nevar izveidot vai rediģēt, izmantojot vispārīgos redaktorus. Šim nolūkam ir pieejami īpaši rīki.

### Kā lietot MST failus?
MST failus var ģenerēt, izmantojot dažādus rīkus, un Ocra parasti izmanto MST failu ģenerēšanai. Pēc tam iestatījumus var pielāgot atbilstoši vajadzībām un saglabāt tos noteiktā vietā. Pēc tam MST failus var izmantot kopā ar MSI failiem. Ja vēlaties pārbaudīt šos failus; komandrindā izmantojiet šādu sintaksi

```
msiexec /i setup_1.0.msi TRANSFORMS=mylog.mst
```
### TRANSFORMĒ īpašumu

Varat arī izmantot Windows instalēšanas programmas rekvizītu **TRANSFORMS**, kas faktiski ir to pārveidojumu saraksts, ko instalētājs izmanto, instalējot pakotni. Instalētājs izpilda transformācijas tādā pašā secībā, kādā tās ir norādītas rekvizītā TRANSFORM. Transformācijas var norādīt pēc faila nosaukuma ar .mst paplašinājumu vai pilnu ceļu. Lai norādītu vairāk nekā vienu transformāciju, atdaliet katra faila nosaukumu vai semikolu, kā parādīts šajā piemērā.

```
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
```

## Atsauces 

* [MST transformācijas faili](https://www.exemsi.com/documentation/mst-transformation-files/)

* [Īpašums TRANSFORMS](https://learn.microsoft.com/en-us/windows/win32/msi/transforms)



