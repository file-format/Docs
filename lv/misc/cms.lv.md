{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "CMS faila formāts — savienojumu pārvaldnieka pakalpojuma profila fails",
  "description":"Uzziniet par CMS failiem un API, kas var izveidot un atvērt CMS failus.",
  "linktitle" : "CMS",
  "menu" : {
    "docs" : {
      "identifier": "misc-cms-lv",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Kas ir CMS fails?

CMS fails ir datu fails, kas satur Microsoft Windows savienojumu pārvaldnieka izmantoto profila informāciju. Tas ļauj attāliem lietotājiem izveidot savienojumu ar tīklu, izmantojot šo profila informāciju. CMS failā saglabātā informācija ietver datus par lietotāja operētājsistēmu un atļaujām, kas tiek izmantotas, lai izveidotu savienojumu starp attālo lietotāju un tīklu. SPS administratori izmanto savienojumu pārvaldnieka administratora komplektu (CMAK), lai ģenerētu CMS failus.

## CMS faila formāts — vairāk informācijas

CMS faili nav parasti atrodami lietotāju iekārtās. Tā kā tie tiek īpaši izmantoti, lai ļautu attāliem lietotājiem piekļūt tīklam, jūs tos atradīsit datoros, kas tiek izmantoti, lai izveidotu savienojumu ar uzņēmuma tīklu vai kādu konkrētu biroju. Vairumā gadījumu to izmanto, lai izveidotu savienojumu ar organizācijas tīklu, piemēram, virtuālo privāto tīklu (VPN), kas ir paredzēts tikai uzņēmumam. Tā kā jūs esat tīkla administrators, jūs iestatīsit piekļuvi šādam tīklam, izmantojot savienojumu pārvaldnieku, lai ļautu viņam piekļūt uzņēmuma tīklam no attālas atrašanās vietas.

### Kas ir iekšējā CMS?

CMS profila fails tiek izveidots, izmantojot savienojumu pārvaldnieku, un tiek iesaiņots kopā ar citiem konfigurācijas failiem, pirms tiek nodrošināts attālajam lietotājam. Šajos papildu failos var būt ietverts CMP un un INF fails, kas ir iesaiņoti kopā ar [EXE](/executable/exe/) failu. Šī pilnā pakotne tiek nodrošināta attālajam lietotājam, lai izveidotu savienojumu ar tīklu.

## Atsauces

* [Izpratne par Windows savienojumu pārvaldnieku un tās konfigurēšanu](https://learn.microsoft.com/en-us/windows-hardware/drivers/mobilebroadband/understanding-and-configuring-windows-connection-manager)


