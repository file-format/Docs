{
  "date": "2022-01-26",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LOCK faila formāts — kas ir bloķēšanas fails?",
  "description": "Uzziniet par LOCK faila formātu un tā .",
  "linktitle": "LOCK",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-loc-lvk"
}
},
  "lastmod": "2022-01-26"
}

## Kas ir LOCK fails?

**LOCK** fails ir pārdēvēts fails, ko izmanto lietojumprogrammas un operētājsistēmas, lai atzīmētu failu vai kādu ierīci kā bloķētu. Tas norāda citām lietojumprogrammām neizmantot failu, ja vien tas nav brīvs no lietojumprogrammas, kas to izmanto. Vairumā gadījumu šie bloķēšanas faili ir tukši, bet citos gadījumos tajos var būt ar bloķēšanu saistīta informācija, piemēram, rekvizīti un iestatījumi.

Dažreiz Microsoft .NET Framework izmanto .lock failu, lai izveidotu datu bāzes faila **lockeed** kopijas. Šādā gadījumā tiks atvērta datu bāzes faila kopija ar paplašinājumu .lock. Tas neļauj lietotājam veikt izmaiņas failā, kamēr to izmanto cits lietotājs.

## BLOĶĒT faila formātu — vairāk informācijas

Katra lietojumprogramma izveido LOCK failu, un tā faila formāts ir specifisks lietojumprogrammai. Šos bloķēšanas failus var saglabāt gan teksta, gan binārā faila formātā.

Bloķēšanas failu klātbūtne neļauj resursam vienlaikus piekļūt vairākiem failiem, kas mēģina piekļūt šim resursam. Tiek izveidota oriģinālā faila kopija ar paplašinājumu .lock ar sufiksu tā nosaukumam. Tas norāda, ka citām lietojumprogrammām ir tikai lasīšanas piekļuve failam. Piemēram, resource.dat kļūs par resource.data.lock.

Ruby programmēšanas valodā jūs varat saskarties ar failu **gemfile.lock**. Šeit Bundler reģistrē precīzas instalētās versijas. Tādējādi, kad projekts/bibliotēka tiek pārvietota uz citu mašīnu, palaistā pakete Gemfile meklēs precīzu atbilstošo versiju.

## Bloķējiet failu operētājsistēmā Linux

Linux atbalsta divu veidu failu bloķēšanu: konsultatīvās bloķēšanas un obligātās bloķēšanas.

 * **Ieteicamās slēdzenes**: bloķēšanas veids, kas netiek īstenots. Šajā gadījumā iesaistītie procesi sadarbojas viens ar otru, nepārprotami iegūstot slēdzenes. Ja tas nav iespējams, konsultatīvās slēdzenes tiek ignorētas.

 * **Obligāti bloķēšana**: Obligātās bloķēšanas gadījumā operētājsistēma nodrošina faila bloķēšanu, neļaujot citiem procesiem nolasīt vai rakstīt failu. Tam nav nepieciešama sadarbība starp procesiem.

obligāta bloķēšana neprasa sadarbību starp iesaistītajiem procesiem. Kad failā ir aktivizēta obligātā bloķēšana, operētājsistēma neļauj citiem procesiem nolasīt vai rakstīt failu.

## Atsauces

* [GemFile un Gemfile.lock in Ruby](https://medium.com/never-hop-on-the-bandwagon/gemfile-and-gemfile-lock-in-ruby-65adc918b856)

* [Bloķēšana operētājsistēmā Linux](https://www.baeldung.com/linux/file-locking#:~:text=File%20locking%20is%20a%20mechanism,very%20dangerous%20command%20in%20Linux.)


