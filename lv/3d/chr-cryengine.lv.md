{
   "date":"2023-10-11",
   "keywords":[
"chr",
"chr fails",
"chr cryengine rakstzīmju fails",
"kā atvērt chr failu",
"failu",
"chr faila paplašinājums",
"pagarinājumu",
"failu"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"CHR faila formāts — CryENGINE rakstzīmju fails",
   "description":"Uzziniet par CHR CryENGINE rakstzīmju faila formātu un API, kas var izveidot un atvērt CHR failus.",
   "linktitle":"CHR CryENGINE",
   "menu":{
      "docs":{
         "identifier":"3d-chr-cryengine-lv",
         "parent":"3d"
}
},
   "lastmod":"2023-10-11"
}

## Kas ir CHR fails?

CHR fails CryENGINE kontekstā attiecas uz **CryENGINE rakstzīmju failu**. CryENGINE ir Crytek izstrādāts spēļu dzinējs, un šie faili tiek izmantoti rakstzīmju modeļu un saistīto datu glabāšanai, lai tos izmantotu videospēlēs un citās reāllaika lietojumprogrammās.

## CryENGINE rakstzīmju fails

CryENGINE rakstzīmju failā parasti ir šādi komponenti:

1.  **Rakstzīmju modelis**: šis ir tēla 3D modelis, tostarp tā ģeometrija, faktūras un animācijas. Šie modeļi bieži tiek izveidoti, izmantojot programmatūru, piemēram, Autodesk Maya vai Blender, un pēc tam importēti programmā CryENGINE.
    
2.  **Animācijas dati**: CryENGINE atbalsta sarežģītas varoņu animācijas, tāpēc .chr failā var būt ietvertas dažādas animācijas, piemēram, staigāšana, skriešana, lēkšana un citas. Šīs animācijas parasti tiek saglabātas kā atslēgas kadra dati.
    
3.  **Informācija par takelāžu**: takelāža attiecas uz rakstzīmju modeļa skeleta struktūras izveides procesu, kas ļauj modelim izmantot animācijas. Failā .chr” var būt ietverta informācija par kaulu hierarhiju un to, kā rakstzīmes siets ir savienots ar šo skeletu.
    
4.  **Materiāla un faktūras dati**: informācija par materiāliem, kas izmantoti rakstzīmju modelī un saistītajās tekstūras kartēs, var tikt iekļauta failā .chr. CryENGINE atbalsta fiziski balstītu renderēšanu, tāpēc šie materiāli var būt diezgan detalizēti.
    
5.  **Fizikas dati**: ja varonis ir paredzēts mijiedarbībai ar spēļu pasauli, failā .chr var būt ietverti fizikas dati, piemēram, sadursmes formas vai lupatu lelles fizikas ierobežojumi.
    
6.  **Konfigurācijas iestatījumi**: .chr failā var būt arī dažādi konfigurācijas iestatījumi, kas saistīti ar varoņa uzvedību spēļu pasaulē, piemēram, AI uzvedība vai skriptēti notikumi.

## CryENGINE

CryENGINE ir jaudīgs spēļu dzinējs, ko izstrādājis vācu videospēļu uzņēmums Crytek. Tas ir pazīstams ar savām visprogresīvākajām grafikas iespējām un ir izmantots, lai izveidotu dažas vizuāli satriecošas un tehnoloģiski progresīvas videospēles. Šeit ir dažas galvenās funkcijas un informācija par CryENGINE:

1.  **Grafika un renderēšana**: CryENGINE ir slavens ar savām uzlabotajām grafikas iespējām. Tā atbalsta tādas funkcijas kā reāllaika globālais apgaismojums, augstas kvalitātes dinamiskais apgaismojums un ēnas, fiziski balstīta renderēšana (PBR) un augstas izšķirtspējas faktūras. Šīs funkcijas palīdz radīt vizuāli satriecošas un reālistiskas spēļu pasaules.
    
2.  **Physics Engine**: CryENGINE ietver iebūvētu fizikas dzinēju, kas nodrošina reālistisku mijiedarbību starp objektiem spēļu pasaulē. Tā atbalsta tādas funkcijas kā stingrā ķermeņa fizika, mīkstā ķermeņa fizika un lupatu lelles fizika, padarot to piemērotu dinamiskas un ieskaujošas vides radīšanai.
    
3.  **Apvidus un veģetācija**: CryENGINE nodrošina rīkus plašas un detalizētas āra vides izveidei. Tā atbalsta reljefa rediģēšanu, veģetācijas izvietojumu un dinamiskas laikapstākļu sistēmas, ļaujot izstrādātājiem izveidot plašus un reālistiskus āra iestatījumus.
    
4.  **Rakstzīmju animācija**: CryENGINE ietver spēcīgus varoņu animācijas rīkus. Tā atbalsta sarežģītas rakstzīmju iekārtas, sejas animāciju un sajaukšanas koku sistēmu, kas ļauj izstrādātājiem izveidot reālistiskas varoņu kustības un animācijas.
    
5.  **AI sistēma**: dzinējam ir AI sistēma, kas ļauj izveidot viedus NPC (ne-spēlētājus) un ienaidnieka AI. Izstrādātāji var skriptēt AI uzvedību un mijiedarbību, lai radītu izaicinošu un aizraujošu spēles pieredzi.
       
6.  **Skriptēšana**: CryENGINE izmanto skriptu valodu ar nosaukumu Schematyc, kas ļauj izstrādātājiem izveidot spēles loģiku un mijiedarbības. Turklāt tas atbalsta C++ progresīvākām programmēšanas vajadzībām.

## CryENGINE izmantotie failu formāti

Šeit ir daži izplatītākie failu veidi, kas saistīti ar CryENGINE:

1.  **cryproj**: CryENGINE projekta faili. Šajos failos tiek glabāti projekta iestatījumi un konfigurācijas konkrētam spēles projektam.
    
2.  **.level**: līmeņa faili satur 3D spēļu pasaules datus, tostarp reljefu, objektus, apgaismojumu un citus līmenim raksturīgus iestatījumus. Līmeņi ir būtiska spēles dizaina sastāvdaļa programmā CryENGINE.
    
3.  **.cgf**: rakstzīmju ģeometrijas formāts. Šajos failos ir ietverti 3D modeļa dati par rakstzīmēm, objektiem un citiem spēles līdzekļiem. CGF faili var ietvert ģeometriju, faktūras un animācijas datus.
    
4.  **.chrparams**: rakstzīmju parametru faili. Šajos failos tiek saglabāti rakstzīmju modeļu un to animāciju iestatījumi un konfigurācijas.
    
5.  **.dds**: DirectX tekstūras formāts. CryENGINE parasti izmanto DDS failus, lai saglabātu tekstūras, tostarp difūzās kartes, parastās kartes un citus tekstūru veidus.
    
6.  **.cryshader**: CryENGINE Shader faili. Šie faili nosaka, kā materiāli un objekti tiek atveidoti spēļu pasaulē, norādot ēnotājus, materiāla īpašības un daudz ko citu.
    
7.  **.crytif**: tekstūras informācijas fails. Šajos failos tiek glabāta papildu informācija par tekstūrām, piemēram, saspiešanas iestatījumi, mipmaps un cita ar tekstūru saistīta informācija.
    
8.  **.cdf**: rakstzīmju definīcijas fails. CDF faili tiek izmantoti, lai definētu rakstzīmju līdzekļus un to rekvizītus, tostarp pielikumus, animācijas stāvokļus un ar rakstzīmēm saistītus iestatījumus.
    
9.  **.dds**: CryENGINE izmanto arī DDS (DirectDraw Surface) failus dažādām tekstūras kartēm, piemēram, parastajām kartēm, spoguļkartēm un difūzajām kartēm.
    
10.  **.anim**: animācijas faili. Šajos failos tiek glabāti varoņu un objektu animācijas dati, tostarp atslēgas kadri, kaulu pozīcijas un animācijas secības.
    
11.  **.xml**: XML failus var izmantot dažādām konfigurācijām un datu definīcijām programmā CryENGINE, piemēram, spēļu loģikai, AI uzvedībai un citiem.
    
12.  **.pak**: [PAK files](/game/pak/) ir arhīva faili, ko izmanto spēļu līdzekļu un resursu iepakošanai, padarot to efektīvāku spēļu izplatīšanai un ielādei.

## Kā atvērt CHR failu?

Programmas, kas atver CHR failus, ietver

- **Crytek CryENGINE SDK** (bezmaksas izmēģinājuma versija) operētājsistēmai Windows

## Citi CHR faili

Tālāk ir norādīti citi failu tipi, kuros tiek izmantots faila paplašinājums **.chr**.

**3D**
- [CHR - CryENGINE Character File](/3d/chr-cryengine/)
- [CHR - 3ds Max Characters File](/3d/chr-3ds/)

**Fonts un spēle**
- [CHR - Borland Character Set](/font/chr/)
- [CHR - Doki Doki Literature Club! Character File](/game/chr-doki/)

## Atsauces
- [CryEngine](https://en.wikipedia.org/wiki/CryEngine)

