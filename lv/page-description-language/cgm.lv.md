{
  "date": "2019-10-11",
  "keywords": [
"CGM",
"Datorgrafikas metafails",
"Fails",
"Pagarinājums",
"Faila formāts",
"Vektorgrafika",
"Metafaila deskriptors"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CGM faila formāts",
  "description": "Uzziniet par CGM failu formātu un API, kas var izveidot un atvērt CGM failus.",
  "linktitle": "CGM",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-cg-lvm"
}
},
  "lastmod": "2021-04-23"
}

## Kas ir CGM fails? ##

Computer Graphics Metafile (CGM) ir bezmaksas, no platformas neatkarīgs, starptautiska standarta metafaila formāts vektorgrafikas (2D), rastra grafikas un teksta glabāšanai un apmaiņai. CGM izmanto uz objektu orientētu pieeju un daudzus funkciju nosacījumus attēlu veidošanai. CGM izmanto šos objektorientētos raksturlielumus grafisko elementu pārveidošanai attēla renderēšanai. Metafails satur nepieciešamo informāciju, kas nosaka citus failus. CGM teksta avota failā ir visi grafiskie elementi, kurus vēlāk var apkopot binārā failā. Būtībā CGM ir veids, kā atvieglot 2D grafisko datu apmaiņu neatkarīgi no konkrētas platformas vai ierīces.

CGM formāts nodrošina dažādus elementus funkciju veikšanai un objektu apzīmēšanai, lai pielāgotu ģeometriskos primitīvus un grafisko informāciju. Lai gan CGM ir aizstāts ar citiem formātiem, lai tīmekļa lapās attēlotu grafisko mākslu, jo tas nav labi atbalstīts tīmekļa lapās, joprojām ir ļoti populārs industriālo, aeronavigācijas un citu tehnisko lietojumu vidū. Lai gan World Wide Web Consortium ir izstrādājis WebCGM, alternatīvu pieeju CGM lietošanai tīmeklī. Primārā CGM ieviešana bija grafiskās kodola sistēmas (GKS) pamatoperāciju secības ilustrācija. Profesionālajos dizainos tas nav tik daudz izmantots, taču to lielā mērā ir aizstājuši citi formāti, piemēram, DXF un SVG.

## Vēsture ##

1987. gadā CGM izrādījās starptautisks standarts (ISO 8632-1987), un to kā nacionālo standartu pieņēma arī Apvienotajā Karalistē BSI un ASV — ANSI. Pēc vairākiem grozījumiem 1991. gadā pārskatītais CGM standarts tika izlaists 1992. gadā (ISO 8632:1992). 2001. gadā World Wide Web Consortium izstrādāja WebCGM ar uzlabotām iespējām, ko izmantot ar tīmekļa lapām. 2007. gadā tika izlaista otrā WebCGM versija, bet 2010. gadā tika izlaista trešā versija ar uzlabotām iespējām.

## CGM faila formāts ##

Datorgrafikas metafaili pamatā ir grafiskās informācijas datubāze un nodrošina grafisko datu uztveršanas, uzglabāšanas un pārsūtīšanas līdzekļus. Līdz ar to ir jābūt grafiskai sistēmas komponentei datu bāzes izveidei vienlaikus ar lietojumprogrammas izpildi metafaila formātā. Vairumā gadījumu šis komponents ir Metafile ģenerators. Līdztekus ir nepieciešams vēl viens komponents, kas var ienest, interpretēt un renderēt grafiskos datus metafailā. Šo vajadzību apmierina metafailu tulka klātbūtne. Nākamajā attēlā ir attēlota grafiskā metafaila darba vide.

CGM saistība ar citiem tipiskas grafikas sistēmas komponentiem ir parādīta augstāk esošajā attēlā. No attēla arī redzams, ka metafaila funkcionalitāte nav atkarīga no galīgās ierīces izvades.

Generally, there are two categories of metafile: **section capture** and **picture capture**. The primary functionality of picture capture metafile is the capturing of device-independent, multiple picture definitions. While session capture metafiles use the system interface to capture the output dialogue in a graphical system. CGM belongs to the category of static picture capture metafiles. CGM provides a well-organized arrangement of components with a two-level structure.

1. Metafaila deskriptors
1. Loģiski neatkarīgu attēlu kopums

Katrs attēls ir attēlu deskriptoru kolekcija un attēla pamatteksts, tostarp attēla definīcija. metafaila deskriptors definē aprakstošu informāciju, kas vienlīdz attiecas uz visiem šī metafaila attēliem. Šī informācija palīdz tulkam pareizi parsēt metafailu un atpazīt resursus, kas nepieciešami pareizai attēla renderēšanai. Lai gan attēla deskriptoram ir pievienota arī aprakstošā informācija, tas var atpazīt tikai attēlu, kurā atrodas deskriptors. Šajā faila formātā katra attēla definīcija ir autonoma un loģiski suverēna. Tie ir neatkarīgi no visām pārējām attēla definīcijām failā. Tūlīt pēc metadeskriptora interpretācijas attēliem var piekļūt un tos interpretēt nejauši. Iepriekšējo attēlu stāvokļa maiņa neietekmē to pēctečus. Šī attēla neatkarība ir vēl viena ievērojama CGM iezīme. CGM sastāv no koordinātu telpas, kas ir 2D Dekarta koordinātas, ko sauc par virtuālās ierīces koordinātām un kuras var attēlot ar skaitļiem vai precizitāti, kas atspoguļo diapazonu un granularitāti. CGM norāda gan tiešu krāsu izvēli, gan uz indeksu balstītu atlasi. Pirmajā gadījumā krāsu norādītājs sastāv no RGB trīskārša, savukārt vēlāk krāsu norādītājs norāda krāsu tabulas indeksu.

CGM matches the needs of both communication-dependent as well as performance-dependent applications. Centralized and distributed graphics systems can use CGM in an unlimited number of ways.  It can be tailored to access graphics devices using a spooling system.
