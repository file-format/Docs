{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PDF/VT faila formāts",
  "description": "Uzziniet par PDF/VT failu formātu un API, kas var izveidot un atvērt PDF/VT failus.",
  "linktitle": "PDF/VT",
  "menu": {
    "docs": {
      "parent": "pdf",
      "identifier": "pdf-v-lvt"
}
},
  "lastmod": "2019-09-10"
}

# Kas ir PDF/VT? #

PDF/VT, kas 2010. gada augustā publicēts kā [ISO 16612-2](https://www.iso.org/standard/46428.html) kā standarts, ir izstrādāts, lai iespējotu mainīgo dokumentu drukāšanu (VDP) dažādās vidēs. Standarts nosaka mainīgās informācijas un transakciju drukāšanu par standarta pamatu. Mainīgo datu drukāšana tiek izmantota, ja daļa informācijas ir atšķirīga katram satura saņēmējam. Darījumu drukāšana ietver rēķinus, izrakstus un citus dokumentus, kas apvieno norēķinu informāciju ar mārketinga informāciju. Tā rezultātā tiek uzlabota attēlu, teksta un citu satura veidu apstrāde. PDF/VT nodrošina uzticamu un dinamisku lappušu pārvaldību liela apjoma transakciju izvades (HVTO) drukas datiem, izmantojot dokumenta daļas metadatu (DPM) koncepciju. PDF/VT failus var atvērt Adobe Acrobat skatītājā, nepievienojot citus komponentus.

## Dokumenta daļas hierarhija ##

Dokumenta daļas (DPart) hierarhija ir kā dokumenta daļas mezglu koka struktūra, kuras pamatā ir visas dokumenta lapas. Šī koka elementus sauc par DPart mezgliem. Katrs iekšējais mezgls satur citus DPart mezglus, un katrs lapas mezgls adresātam norāda vienu vai vairākas lapas. Būtībā DPart hierarhija nosaka PDF/VT failā esošo dokumentu vai dokumentu gabalu secību un attiecības. DPart mezglu koka struktūra viegli atspoguļo PDF/VT dokumenta iekšējo saturu, jo tā var saturēt apakšdokumentus daudziem adresātiem, un katra dokumenta daļa atbilst viena adresāta lapām. DPart hierarhija ir nepieciešama PDF/VT failos.

## Dokumenta daļas metadati (DPM) ##

Dokumenta daļas metadati (DPM) ir saistīti ar katru mezglu dokumenta daļas hierarhijā, un tos var izmantot, lai paziņotu informāciju par konkrēta adresāta apakšdokumentu un tā daļām. Jo īpaši DPM var saturēt informāciju par rekvizītiem vai informāciju par adresātiem kodētā veidā.

## Atbilstības līmeņi ##

PDF/VT tiek piešķirts šādiem trim atbilstības līmeņiem. Tie visi ir balstīti uz [PDF](/pdf/) 1.6.

* `PDF/VT-1` — tas ir balstīts uz PDF/X-4 un satur visus resursus, kas nepieciešami PDF dokumenta renderēšanai.

* `PDF/VT-2` — paredzēti vairāku failu apmaiņai, PDF/VT-2 dokumenti var atsaukties uz ārējiem izvades nolūkiem, ārēju saturu vai abiem. PDF/VT dokuments un visi tajā norādītie PDF faili un ārējās izvades nolūki tiek saukti par PDF/VT-2 failu kopu. Acrobat 9 un atbalsta šo funkciju.

* `PDF/VT-2s` — atbalsta PDF/VT-2 tiešraides straumēšanu. Tas ļauj apstrādāt segmentētas datu sadaļas.


## Atsauces Nr.

* [PDF/VT — Wikipedia](https://en.wikipedia.org/wiki/PDF/VT)

* [ISO 16612-2 grafiskā tehnoloģija](https://www.iso.org/standard/46428.html)


