{
  "date": "2022-01-26",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LOCK failo formatas – kas yra užrakinimo failas?",
  "description": "Sužinokite apie LOCK failo formatą ir jo .",
  "linktitle": "LOCK",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-loc-ltk"
}
},
  "lastmod": "2022-01-26"
}

## Kas yra LOCK failas?

**UŽRAKINTI** failas yra pervardytas failas, kurį programos ir operacinės sistemos naudoja failui ar tam tikram įrenginiui pažymėti kaip užrakintą. Tai nurodo kitoms programoms nenaudoti failo, nebent jame nėra jį naudojančios programos. Daugeliu atvejų šie užrakto failai yra tušti, tačiau kitais atvejais juose gali būti su užraktu susijusios informacijos, pvz., ypatybių ir parametrų.

Kartais .lock failą naudoja Microsoft .NET Framework, kad sukurtų **lockeed** duomenų bazės failo kopijas. Tokiu atveju bus atidaryta duomenų bazės failo kopija su plėtiniu .lock. Tai neleidžia vartotojui keisti failo, kai jį naudoja kitas vartotojas.

## Užrakinti failo formatą – daugiau informacijos

LOCK failą sukuria kiekviena programa, o jo failo formatas yra specifinis programai. Šiuos užrakto failus galima išsaugoti tiek tekstiniu, tiek dvejetainiu formatu.

Užrakinimo failų buvimas neleidžia vienu metu pasiekti išteklių prie kelių failų, bandančių pasiekti tą išteklį. Sukurta originalaus failo kopija su .lock plėtiniu prie jo pavadinimo. Tai nurodo kitoms programoms turėti tik skaitymo prieigą prie failo. Pavyzdžiui, resource.dat taps resource.data.lock.

Jei naudojate Ruby programavimo kalbą, galite rasti failą **gemfile.lock**. Čia Bundler įrašo tikslias įdiegtas versijas. Taigi, kai projektas / biblioteka perkeliama į kitą įrenginį, paleistas paketas ieškos tikslios atitinkamos versijos Gemfile.

## Užrakinti failą „Linux“.

Linux palaiko dviejų tipų failų užraktus: patariamuosius ir privalomuosius užraktus.

 * **Patariamieji užraktai**: užrakinimo tipas, kuris nėra vykdomas. Šiuo atveju dalyvaujantys procesai bendradarbiauja tarpusavyje, aiškiai įsigydami užraktus. Jei tai neįmanoma, įspėjamųjų užraktų nepaisoma.

 * **Privalomi užraktai**: Privalomo užrakinimo atveju operacinė sistema užtikrina failo užrakinimą, neleisdama kitiems procesams nuskaityti ar rašyti failo. Tam nereikia jokio bendradarbiavimo tarp procesų.

privalomas užrakinimas nereikalauja jokio dalyvaujančių procesų bendradarbiavimo. Kai faile suaktyvinamas privalomas užraktas, operacinė sistema neleidžia kitiems procesams nuskaityti ar rašyti failo.

## Nuorodos

* [GemFile ir Gemfile.lock in Ruby](https://medium.com/never-hop-on-the-bandwagon/gemfile-and-gemfile-lock-in-ruby-65adc918b856)
* [Užrakinimas sistemoje „Linux“](https://www.baeldung.com/linux/file-locking)
