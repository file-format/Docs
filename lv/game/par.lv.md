{
   "date":"2023-07-18",
   "keywords":[
"PAR",
"PAR fails",
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
   "title":"PAR faila formāts — FMS lidmašīnas parametru fails",
   "description":"Uzziniet par PAR formātu un API, kas var izveidot un atvērt PAR failus.",
   "linktitle":"PAR",
   "menu":{
      "docs":{
         "identifier":"game-par-lv",
         "parent":"game"
}
},
   "lastmod":"2023-07-18"
}

## Kas ir PAR fails?

PAR failu, ko parasti sauc par gaisa kuģa parametru failu, īpaši izmanto FMS (Flying-Model-Simulator), lidojuma simulācijas spēle, kas paredzēta Windows operētājsistēmām. Tās mērķis ir saglabāt svarīgus datus par lidmašīnas ģeometriju un fiziskajām īpašībām, tostarp tādām īpašībām kā masa, smaguma centrs un inerces momenti. Šie PAR faili ir noderīgi pielāgotu lidmašīnu izveidē spēlē, ļaujot spēlētājiem simulēt un lidot ar savu unikālo virtuālo lidmašīnu ar precīzu un reālistisku fiziku.

## PAR faila formāts — vairāk informācijas

FMS ir programmatūras sistēma, ko izmanto lidmašīnās, lai palīdzētu veikt navigāciju, lidojuma plānošanu un autopilota funkcijas. FMS gaisa kuģa parametru fails, kas bieži tiek saīsināts kā PAR fails, satur konkrētus datus, kas saistīti ar gaisa kuģa veiktspējas īpašībām un lidojuma pārvaldību.

Šis PAR faila formāts ir raksturīgs lidojuma simulācijas programmatūrai, piemēram, tai, ko izmanto populārās lidojumu simulatora programmās, piemēram, Microsoft Flight Simulator vai X-Plane. Failā ir dažādi parametri un dati, kas nosaka simulatora virtuālā gaisa kuģa uzvedību, veiktspēju un sistēmas.

FMS gaisa kuģa parametru fails parasti ietver šādu informāciju:

- **Lidakuģa specifikācijas:** ietver informāciju par gaisa kuģa fiziskajām īpašībām, piemēram, svaru, izmēriem, degvielas ietilpību un dzinēja specifikācijām.

- **Lidojuma veiktspējas dati:** tajā ir ietverti dati, kas saistīti ar gaisa kuģa veiktspēju dažādās lidojuma fāzēs, tostarp kāpšanas, kruīza, nolaišanās un nosēšanās laikā. Tas var ietvert kāpuma ātrumu, degvielas patēriņa rādītājus, ātruma ierobežojumus un citus ar veiktspēju saistītus parametrus.

- **Autopilota iestatījumi:** failā var norādīt gaisa kuģa autopilota darbību un ierobežojumus, tostarp autopilota režīmus, augstuma un virziena ierobežojumus un vadības jutīgumu.

- ** Navigācijas dati:** var ietvert ar navigāciju saistītus parametrus, piemēram, gaisa kuģa navigācijas datu bāzi, tostarp maršruta punktus, gaisa ceļus un lidostu datus.

Šos PAR failus parasti izveido un uztur gaisa kuģu izstrādātāji vai trešo pušu entuziasti, kuru mērķis ir nodrošināt reālistisku un precīzu simulācijas pieredzi lidojuma simulatora programmatūrā. Pēc tam faili tiek ielādēti simulatorā, lai noteiktu simulētā gaisa kuģa uzvedību un veiktspējas raksturlielumus.

## PAR failu, 3D modeļu, faktūru un skaņu loma lidojuma simulācijas spēlēs

PAR faili ir tikai viena daļa no kopējās gaisa kuģa datu paketes. Papildus PAR failiem ir vairāki citi faili, kas kopā veicina pilnīgu lidmašīnas attēlojumu spēlē. Šie papildu faili parasti ietver 3D modeļu failus, tekstūras bitkartes un skaņas.

- **3D modeļu faili:**

Lidojumu simulācijas spēlēm ir nepieciešami detalizēti 3D modeļi, lai vizuāli attēlotu lidmašīnu virtuālajā vidē. Šie 3D modeļi sastāv no dažādām sastāvdaļām, piemēram, fizelāžas, spārniem, šasijas un citām sarežģītām lidmašīnas daļām. 3D modeļu faili nodrošina vizuālo struktūru un ģeometriju, kas nepieciešama, lai precīzi attēlotu lidmašīnas izskatu un formu spēlē.

- **Tektūras bitkartes:**

Tekstūru bitkartes, kas pazīstamas arī kā tekstūras vai attēlu kartes, tiek izmantotas, lai 3D modeļiem pievienotu krāsas, virsmas detaļas un vizuālo reālismu. Šajos tekstūras failos ir ietverta informācija, piemēram, krāsu shēmas, uzlīmes, logotipi un virsmas faktūras, piemēram, metāls, plastmasa vai audums. Lietojot tekstūras bitkartes 3D modeļiem, spēles lidaparātu var vizuāli uzlabot, tādējādi radot iespaidīgāku un vizuāli pievilcīgāku pieredzi.

- **Skaņas:**

Skaņas faili ir būtisks lidojuma simulācijas spēļu elements, jo tie nodrošina dzirdes atgriezenisko saiti un reālismu. Šajos failos parasti ir iekļautas dzinēja skaņas, kabīnes skaņas, vides efekti, piemēram, vējš vai lietus, un citi gaisa kuģim raksturīgi audio signāli. Iekļaujot atbilstošus skaņas failus, spēle var precīzi atjaunot audio vidi, kas saistīta ar simulēto lidmašīnu, vēl vairāk uzlabojot vispārējo iegremdēšanu.

Lai gan PAR fails satur konkrētus datus, kas saistīti ar gaisa kuģa veiktspēju un lidojuma pārvaldību, tā ir PAR failu, 3D modeļu failu, faktūras bitkartes un skaņas failu kombinācija, kas kopā atdzīvina virtuālo lidaparātu lidojuma simulācijas spēlē. Katrs fails kalpo unikālam mērķim, veidojot visaptverošu un reālistisku lidmašīnas attēlojumu, nodrošinot spēlētājiem aizraujošu pieredzi.

## Kā atvērt PAR failu?

Programmas, kas atver PAR failus, ietver

- Lidojošs modelis-simulators (FMS)
- Microsoft lidojuma simulators
- X-Plane

## Atsauces
* [Flying-Model-Simulator (FMS)](https://modelsimulator.com/)

* [Microsoft Flight Simulator](https://en.wikipedia.org/wiki/Microsoft_Flight_Simulator)



