{
   "date":"2023-07-18",
   "keywords":[
"PAR",
"PAR fails",
"kā atvērt par failu",
"failu",
"PAR faila paplašinājums",
"pagarinājumu",
"failu"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"PAR faila formāts — parhīva indeksa fails",
   "description":"Uzziniet par PAR formātu un API, kas var izveidot un atvērt PAR failus.",
   "linktitle":"PAR",
   "menu":{
      "docs":{
         "identifier":"compression-par-lv",
         "parent":"compression"
}
},
   "lastmod":"2023-07-18"
}

## Kas ir PAR fails?

Parhīva (PAR) arhīvos .par fails attiecas uz indeksa failu, kas satur paritātes sējumu vai paritātes bloku grupu. Šis indeksa fails tiek izmantots kļūdu noteikšanas un atkopšanas nolūkos, ja viens vai vairāki arhīva faili tiek pazaudēti vai bojāti.

Parhīva arhīvs parasti sastāv gan no sākotnējiem datu failiem, gan no atbilstošajiem paritātes sējumiem. Paritātes apjomi tiek izveidoti, izmantojot Rīda-Zālamana kļūdu labošanas algoritmus. Šajos paritātes sējumos ir lieka informācija, ko var izmantot sākotnējo datu failu atkopšanai.

.par fails, kas pazīstams arī kā paritātes sējumu kopa, satur informāciju par paritātes sējumu struktūru un atrašanās vietu arhīvā. Tas kalpo kā indekss vai karte atkopšanas procesam. Izmantojot .par failu, specializētā PAR programmatūra var noteikt, kuri paritātes sējumi ir nepieciešami un kā tie jāizmanto, lai rekonstruētu trūkstošos vai bojātos failus.

Ja viens vai vairāki faili parhīva arhīvā kļūst nepieejami vai bojāti, .par failu var izmantot kopā ar pieejamajiem paritātes sējumiem, lai atgūtu zaudētos datus. PAR programmatūra nolasa .par failu, identificē trūkstošos vai bojātos failus un izmanto paritātes sējumus, lai tos rekonstruētu.

## Kā atvērt PAR failu?

Lai atvērtu un izmantotu .par failus, jums būs nepieciešama specializēta PAR programmatūra. Tālāk ir norādītas dažas populāras programmatūras opcijas, kas var apstrādāt .par failus:

- **QuickPar:** QuickPar ir plaši izmantota PAR programmatūra operētājsistēmai Windows. Tas ļauj jums izveidot, pārbaudīt un labot PAR failus. Varat atvērt .par failu programmā QuickPar, lai pārbaudītu tā integritāti, vai izmantot to bojātu vai trūkstošu failu labošanai parhīva arhīvā.

- **MultiPar:** MultiPar ir vēl viena populāra PAR programmatūra, kas pieejama operētājsistēmai Windows. Tā atbalsta gan PAR, gan PAR2 failu formātus un nodrošina uzlabotas funkcijas arhīvu izveidei, pārbaudei un labošanai. MultiPar var atvērt .par failus un veikt kļūdu noteikšanas un atkopšanas darbības, pamatojoties uz nodrošinātajiem paritātes apjomiem.

- **MacPAR deLuxe:** MacPAR deLuxe ir PAR programmatūra, kas īpaši izstrādāta operētājsistēmai MacOS. Tā atbalsta PAR un PAR2 failu formātus un nodrošina līdzīgu funkcionalitāti kā QuickPar un MultiPar. MacPAR deLuxe var atvērt .par failus un palīdzēt pārbaudīt arhīvus un atgūt bojātus vai trūkstošus failus.

## PAR faila formāts — vairāk informācijas

PAR faila formāts, ko parasti dēvē par parhīvu, ir īpašs faila formāts, ko izmanto, lai izveidotu paritātes datus un veiktu kļūdu noteikšanu un atkopšanu failu arhīvos. PAR faila formāts parasti sastāv no trīs veidiem: PAR, PAR2 un PAR3.

- **PAR:** Oriģinālo PAR faila formātu, kas pazīstams arī kā PAR1, izstrādāja projekts Parchive. Tas ietver paritātes datus, kas ģenerēti no sākotnējiem datu failiem. PAR faili nodrošina kļūdu noteikšanas un atkopšanas pamatlīmeni, taču tiem ir ierobežojumi kļūdu labošanas iespēju ziņā.

- **PAR2:** PAR2 ir uzlabota PAR faila formāta versija. Tā piedāvā uzlabotas kļūdu labošanas iespējas un uzlabotas atkopšanas funkcijas. PAR2 faili parasti tiek izmantoti, lai izveidotu paritātes datus, kas var atgūt zaudētos vai bojātos failus arhīvā. PAR2 faili nodrošina labāku aizsardzību pret datu korupciju un tiek plaši izmantoti failu arhivēšanai.

- **PAR3:** PAR3 is the latest version of the PAR file format and provides further improvements in error correction and recovery. It offers even higher levels of redundancy and error correction capabilities compared to PAR2. PAR3 faili ir izstrādāti, lai nodrošinātu stingrāku aizsardzību un atkopšanas iespējas arhīvos glabātajiem datiem.

Gan PAR2, gan PAR3 failu formātus plaši atbalsta PAR programmatūra, un tie piedāvā iespēju pārbaudīt arhīvā esošo failu integritāti un atgūt zaudētos vai bojātos datus. PAR un PAR2 faili joprojām tiek plaši izmantoti, savukārt PAR3 faili pakāpeniski tiek pieņemti, pateicoties to uzlabotajām kļūdu labošanas iespējām.

## Atsauces
* [Parchive](https://en.wikipedia.org/wiki/Parchive)


