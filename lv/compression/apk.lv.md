{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "APK — kas ir APK fails?",
  "description": "Uzziniet, kas ir APK fails un API, kas var izveidot un atvērt APK failus.",
  "linktitle": "APK",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-ap-lvk"
}
},
  "lastmod": "2021-04-27"
}

## Kas ir APK fails?

Fails ar paplašinājumu .apk ir Google Android lietotnes fails, ko izmanto, lai instalētu lietotnes (lietojumprogrammas) Android ierīcēs. Tas tiek izveidots kā izpildāms fails, izmantojot oficiālo IDE Google Android Studio, un tiek augšupielādēts Google Play veikalā, lai galalietotāji to lejupielādētu un instalētu. APK failus var ģenerēt un padarīt pieejamus manuālai instalēšanai, kā arī pirms publicēšanas Google Play veikalā. Tas palīdz pārbaudīt ģenerētā APK pakotnes faila funkcionalitāti un darbību. Tāpēc ir jāpārliecinās, ka APK fails ir no uzticama avota un nesatur ļaunprātīgu programmatūru.

## APK faila formāts

APK faili ir saspiesti [ZIP](/compression/zip/) faila formātā, ko var atvērt ar jebkuru ZIP failu atvēršanas programmatūru. Šāda faila .apk paplašinājumu var pārdēvēt par .zip un atvērt failu jebkurā ZIP lietojumprogrammā vai izvilkt tā saturu.

## APK pakotnes saturs

Vienā APK failā ir visi nepieciešamie faili, kas nepieciešami tā instalēšanai un izpildei. APK failā, kas iegūts ar ZIP lietojumprogrammu, ir šādi faili un mapes.

 * META-INF/: direktorijs, kurā ir manifesta fails, paraksts un arhīva resursu saraksts.
 * lib/: direktorijs, kurā ir apkopots kods, kas saistīts ar noteiktām platformām, piemēram, armeabi-v7a, x86, arm64-v8a utt.
 * `res/`: direktorijs, kas satur neapkopotus resursus, piemēram, attēlus
 * Assets/: direktorijs, kurā ir lietojumprogrammu līdzekļi, kurus var izgūt AssetManager.
 * `androidManifest.xml`: satur APK faila nosaukumu, versiju informāciju un saturu.
 * `classes.dex`: šīs ir apkopotas Java klases, kuras var palaist Dalvik virtuālajā mašīnā un Android Runtime.
 * resources.arsc: apkopots resursu fails, piemēram, virknes

## Kā atvērt APK failus

APK faili ir paredzēti instalēšanai Android ierīcēs. Turklāt Windows 11 ir pirmā Windows versija, kas oficiāli atbalsta APK failu instalēšanas funkciju.

### Kā instalēt APK failu Android ierīcē

Lai Android ierīcēs instalētu APK failu, var veikt šādas darbības.

 1. Lejupielādējiet APK, izmantojot tīmekļa pārlūkprogrammu
 2. Pieskarieties tam — pēc tam ierīces augšējā joslā vajadzētu redzēt, kā tas tiek lejupielādēts
 3. Kad tas ir lejupielādēts, atveriet Lejupielādes, pieskarieties APK failam un pieskarieties Jā, kad tas tiek prasīts.

Veicot šīs darbības, tiks sākta lietotnes instalēšana jūsu ierīcē.

### Kā atvērt APK failu sistēmā Windows

Lai atvērtu/piekļūtu APK failam, operētājsistēmā Windows PC varat izmantot Android emulatoru. BlueStacks ir viens no šādiem Android emulatoriem, ko var izmantot, lai atvērtu Android emulatoru operētājsistēmā Windows. Ja izmantojat operētājsistēmu Windows 11, jums ir paveicies, jo sistēma Windows 11 oficiāli atbalsta iespēju instalēt APK failus.

### Kā atvērt APK failu operētājsistēmā Mac

Varat arī izmantot BlueStack operētājsistēmā MacOS un atvērt APK failus. Tas ir bezmaksas Android emulators un piedāvā iespēju to izmantot kā labāko veidu, kā piekļūt tikai Android lietotnēm.

## Kā izveidot APK failu

Lai izveidotu APK failu, ir jāizmanto specializēti rīki un izstrādes vide. Android izstrādātāji galvenokārt izmanto Android Studio, oficiālo integrēto izstrādes vidi (IDE) Android lietotņu izstrādei. Tālāk ir sniegts vispārīgs pārskats par darbībām, kas saistītas ar APK faila izveidi.

 1. **Iestatiet izstrādes vidi:** instalējiet un iestatiet Android Studio savā datorā. Android Studio nodrošina visaptverošu rīku komplektu Android lietotņu izstrādei, testēšanai un iesaiņošanai.
 1. **Izstrādājiet savu lietotni:** izmantojiet Java vai Kotlin programmēšanas valodas, lai rakstītu savas Android lietotnes kodu. Android Studio nodrošina bagātīgu funkciju un resursu kopumu, lai palīdzētu jums izveidot lietotni, tostarp koda redaktorus, emulatorus un atkļūdošanas rīkus.
 1. **Izveidojiet lietotni:** kad esat pabeidzis koda rakstīšanu un lietotāja interfeisa noformēšanu, izmantojiet Android Studio veidošanas rīkus, lai apkopotu un pakotētu savu lietotni. Šis process ģenerē APK failam nepieciešamos failus un resursus.
 1. **Parakstīt APK failu:** pirms lietotnes izplatīšanas ir obligāti jāparaksta APK fails. Lietotnes parakstīšana nodrošina lietotnes integritāti un autentiskumu. Android Studio ļauj ģenerēt parakstīšanas atslēgu un parakstīt APK failu, izmantojot šo atslēgu.
 1. **Izplatiet APK failu:** kad esat parakstījis APK failu, varat to izplatīt, izmantojot dažādus kanālus. Varat augšupielādēt to Google Play veikalā izplatīšanai plašai auditorijai vai kopīgot to tieši ar lietotājiem, izmantojot e-pastu, lejupielādes saites vai citas izplatīšanas platformas.

Ir vērts atzīmēt, ka no Android Studio ģenerētais APK fails parasti ir optimizēts ražošanas lietošanai. Izstrādes procesa laikā varat arī ģenerēt atkļūdošanas APK failus, kas ir noderīgi testēšanai un atkļūdošanai, bet nav paredzēti izplatīšanai.

## FAQ

 * **Vai APK faili var kaitēt manai ierīcei?** APK faili var apdraudēt ierīces. Tas ir saistīts ar iespējamu ļaunprātīgas programmatūras klātbūtni tajos. Tāpēc pirms instalēšanas APK failiem ieteicams veikt tiešsaistes vīrusu skenēšanu. Turklāt Android pretvīrusu lietotnes izmantošana ir apdomīgs pasākums. Lai samazinātu risku, ka ierīce var kļūt par maldinošas programmas upuri, vislabāk ir lejupielādēt no uzticamiem avotiem, kas jums pazīstami un kuriem uzticaties.

 * **Vai APK faili ir likumīgi?** APK failu lejupielāde un izmantošana lietotņu instalēšanai no avotiem, kas nav Google Play veikals, ir pilnībā atbilstošs tiesību aktiem. APK, kas līdzinās tādiem formātiem kā EXE vai ZIP, ir faila formāts. Lai gan Google bija šī formāta pionieris, ikviens var ģenerēt un izmantot APK failus.

 * **Kā atrast APK failus savā Android ierīcē?** APK faili paliek paslēpti no lietotājiem, jo Android pārvalda lietotņu instalēšanu fonā, izmantojot pakalpojumu Google Play vai citu lietojumprogrammu izplatīšanas platformu. Tomēr no citiem avotiem lejupielādētos APK failus var atrast, izmantojot Android failu pārvaldnieku.

## Atsauces

* [APK faila formāts](https://en.wikipedia.org/wiki/Android_application_package)


