{
  "date" : "2023-01-31",
  "keywords" : ["run file", "what is a run file", "file", "how to open run file", "run file extension","extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Uzziniet par RUN faila formātu un API, kas var izveidot un atvērt RUN failus.",
  "title" : "RUN faila formāts — Linux izpildāmais fails",
  "linktitle" : "RUN",
  "menu" : {
    "docs" : {
      "identifier":"executable-run-lv",
      "parent" : "executable"
}
},
  "lastmod" : "2023-01-31"
}

## Kas ir RUN fails?

Faila formāts .run parasti tiek izmantots programmatūras vai lietojumprogrammu instalētāju izplatīšanai Linux vidē. Lai instalētu programmatūru, jums būs jāpadara fails izpildāms, ko var izdarīt, izmantojot šādu komandu:

```bash
chmod +x file_name.run 
```

Pēc tam failu var palaist, izmantojot šādu komandu:

```bash
./file_name.run 
```

Instalēšanas process var atšķirties atkarībā no konkrētā faila un programmas, kuru mēģināt instalēt.

Faila formāts .run ir čaulas skripta veids, ko izmanto programmatūras vai lietojumprogrammu instalētāju izplatīšanai Linux vidē. Tā ir autonoma pakotne, kas ietver visu, kas nepieciešams programmatūras instalēšanai, tostarp bināros failus, bibliotēkas un konfigurācijas failus.

Ir svarīgi ņemt vērā, ka .run failos var būt arī ļaunprātīgs kods, tāpēc pirms faila palaišanas vienmēr ir ieteicams pārbaudīt faila avotu un pārbaudīt, vai tajā nav vīrusu.

Turklāt, lai palaistu un instalētu dažus .run failus, var būt nepieciešamas root tiesības, tāpēc, iespējams, būs jāizmanto komanda sudo, lai palaistu failu ar paaugstinātām atļaujām:

```bash
sudo ./filename.run
```

## Kā atvērt RUN failu?

Lai atvērtu .run failu, tas ir jāpadara izpildāms, ko var izdarīt ar komandu chmod:

```bash
chmod +x filename.run 
```

Kad fails ir padarīts izpildāms, varat to palaist, ierakstot:

```bash
./filename.run
```

.run faila palaišana nav tas pats, kas tā atvēršana teksta redaktorā. Palaižot .run failu, tiks izpildīti tā norādījumi, kas var būt jebkas, sākot no programmas instalēšanas līdz skripta palaišanai. Lai skatītu .run faila saturu, tas ir jāatver teksta redaktorā, piemēram, nano vai vim:

```
nano filename.run
```
vai
```
vim filename.run
```

## Atsauces
* [Kā izpildīt .bin un .run failus Ubuntu](https://vitux.com/how-to-execute-bin-and-run-files-in-ubuntu/)



