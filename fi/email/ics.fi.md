{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ICS - iCalendar-tiedostomuoto",
  "description": "Opi ICS-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata ICS-tiedostoja.",
  "linktitle": "ICS",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-ic-fis"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on ICS-tiedosto?

Internet-kalenterin ja -aikataulun ydinobjektimääritys (iCalendar) on Internet-standardi (RFC 2445) kalenteritapahtumien ja aikataulujen vaihtamiseen ja käyttöönottoon. iCalendar-muoto on yhteentoimiva, mikä varmistaa kalenteritietojen vaihdon eri sähköpostisovelluksia käyttävien käyttäjien kesken. iCalendar muotoilee syöttötiedot Multipurpose Internet Mail Extensions (MIME) -laajennuksiksi ja helpottaa eri siirtoprotokollien kautta vaihdettua objektia. Nämä siirtoprotokollat voivat olla SMTP, HTTP, pisteestä pisteeseen asynkroninen viestintä ja fyysinen mediapohjainen verkkokuljetus.

iCalendarin avulla käyttäjät voivat jakaa tapahtumia, päivämäärästä/ajasta riippuvia tehtäviä ja vapaa-/varattu-tietoja sähköpostin kautta muille käyttäjille, jotka voivat vastata. iCalendar-tiedostot tallennetaan käyttämällä jälkiliitteitä .ics .iCalendar tai .ifb ja MIME-tyyppiä text/calendar. iCalendar pidetään omavaraisena ilman siirtoprotokollariippuvuutta. Web-palvelimet (HTTP-protokollalla) voivat siirtää iCalendar-tietoja ja verkkosivut voivat sisältää iCalendar-tietoja upotetussa muodossa iCalendarin avulla.

## ICS-tiedostomuodon lyhyt historia

In 1998, the Internet Engineering Task Force (IETF) defined iCalendar as a standard (RFC 2445). The standard was documented by Frank Dawson(Lotus Notes Corporation) and Derik Stenerson ( Microsoft). In 2009, the standard was again refined by Bernard Desruisseaux (Oracle) as RFC 5545. Tällä kertaa uusia ominaisuuksia lisättiin ja jotkin vanhentuneet ominaisuudet poistettiin käytöstä. Vuonna 2016 RFC 7986 julkaistiin ja laajennettiin alkuperäiseksi iCalendar RFC:ksi. RFC 7986 lisäsi uusia ominaisuuksia VCALENDAR-pääobjektiin ja uusia tukiominaisuuksia esiteltiin myös neuvottelujärjestelmille.

## ICS-tiedostomuoto ##

iCalendarin tietojen käyttämä MIME-tyyppi on teksti/kalenteri. iCalendarin oletusmerkistö on UTF-8, mutta antamalla parametrit MIME:ssä voidaan käyttää erilaista merkistöä. iCalendar-tiedosto sisältää osioita, joista yksi VCALENDAR on yleinen osio, joka kapseloi kaikki muut osat. VEVENT-osio määrittää tapahtumat, VTODO listaa kaikki tehtävät, VJOURNAL sisältää päiväkirjamerkinnät ja VTIMEZONE määrittää aikavyöhyketiedot. useita saman luokan osioita sallitaan. Useiden tapahtumien yhteydessä iCalendar-tiedostossa voi olla useita VEVENT-osioita.

### Sisältölinjat ###

iCalendar-objektit on järjestetty erillisiksi tekstiriveiksi sisältöriveiksi. Tässä tiedostomuodossa CRLF-sekvenssi päättää rivin, kun taas rivin pituus on rajoitettu 75 oktettiin ilman rivinvaihtoa. Pitkä tietokohde voidaan jakaa useille riveille.

### Luettelo- ja kenttäerottimet ###

Ominaisuudet ja parametrit määrittävät luettelon arvoista, jotka on erotettu COMMA-merkillä. Lainausmerkkijonoja käytetään URI-pohjaisissa parametriarvoissa. Parametriluettelo voidaan muodostaa kiinteistön arvon perusteella. Jokainen tämän luettelon ominaisuusparametri on erotettava PUOLIPILLALLA.

Arvoluettelossa PUOLISULLA eristää ominaisuusparametrit ja PIKU erottaa ominaisuusarvot. Esimerkki on annettu alla:

```
ATTENDEE;RSVP#TRUE;ROLE#REQ- contestant:mailto:
name@example.com
DATE;VALUE#DATE:20170304,20180504,2015704,201270904
```

### Useita arvoja

Joillakin ominaisuuksilla voi olla useita arvoja. Yksinkertaisesti uuden sisältörivin luominen ominaisuuden nimellä on moniarvoisten ominaisuuksien perussääntö. Yhdelle arvolle, jossa on useita kielimuunnelmia, ei kuitenkaan saa käyttää moniarvoisia ominaisuuksia.

### Binäärisisältö

iCalendar-objektissa ominaisuuden arvo voi viitata binäärisisältöön, joka on sijoitettu ulkoiseen MIME-olioon URI:n avulla. Sisäistä binaarisisältöä voidaan käyttää erikoistilanteissa ENCODING-parametrilla, jossa sovelluksen on ilmaistava iCalendar-objekti ainoana kokonaisuutena. Seuraava esimerkki selittää ATTACH-ominaisuuden URI-viittauksella:

ATTACH: https://products.conholdate.app/viewer/view/KDDURXKkLk/fileformat.doc

### Merkistö

Vaikka iCalendarin oletusmerkkisarja on UTF-8, mitään ominaisuusparametria ei ole määritetty ominaisuuden arvon merkistöä varten. MIME-siirroissa charset-parametria PITÄÄ käyttää olemassa olevalle merkistölle.

## Kuinka avata ICS-tiedosto?

ICS-tiedosto voi avata useilla tavoilla. Nämä on kuvattu yksityiskohtaisesti alla.

1. Avaa ICS kalenterisovellusten avulla

Voit avata ICS-tiedostoja käyttämällä kalenterisovelluksia, kuten Microsoft Outlook, Google Calendar tai Apple Calendar. Jos sinulla on nämä sovellukset asennettuna laitteellesi, voit avata ICS-tiedoston näillä sovelluksilla yksinkertaisesti kaksoisnapsauttamalla sitä. Tämä tuo ICS-tiedoston tapahtumat kalenteriisi.

1. Avaa ICS-tiedosto tekstieditorissa

Voit myös avata ICS-tiedoston missä tahansa tekstieditorissa, kuten Microsoft Notepadissa tai Apple TextEditissä. Kun olet avannut, näet DTSTART- ja DTEND-rivit, jotka edustavat tapahtuman alkamis- ja päättymisajoja.

1. Tuo ICS-tiedosto manuaalisesti kalenterisovelluksessa

Voit myös tuoda ICS-tiedoston manuaalisesti kalenterisovellukseesi käyttämällä näiden kalenterisovellusten Imiprot & vienti -asetuksia. Tämä lisää ICS-tiedoston tapahtumat kalenteriisi.

## Viitteet

* [Internet Calendaring and Scheduling Core Object Specification](https://www.ietf.org/rfc/rfc5545.txt)

* [iCalendar (RFC 5545)](https://icalendar.org/RFC-Specifications/iCalendar-RFC-5545/)

* [iCalendar](https://en.wikipedia.org/wiki/ICalendar#History_and_design)


