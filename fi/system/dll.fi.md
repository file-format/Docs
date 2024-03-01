{
  "date": "2021-06-29",
  "keywords": [
"DLL",
"laajennus",
"tiedosto",
"muoto",
"järjestelmä",
"Dynaaminen linkkikirjasto",
"asetukset",
"ohjelmia",
"tietokone",
"sovellus"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "DLL - Dynaaminen linkkikirjasto",
  "description": "Opi DLL-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata DLL-tiedostoja.",
  "linktitle": "DLL",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-dl-fil"
}
},
  "lastmod": "2021-06-29"
}

## Mikä on DLL-tiedosto? ##

DLL-tiedosto tai Dynamic Link Library on suoritettavan tiedoston tyyppi. Se on yksi yleisimmistä laitteesi laajennustiedostoista, ja se on yleensä tallennettu Windowsin System32-kansioon. DLL-laajennustiedoston on kehittänyt Microsoft, ja he käyttävät sitä yleisesti. Sillä on korkea suosio käyttäjäluokitus. DLL toimii hyllynä, joka sisältää Windows-palvelimen ohjelmalle/sovellukselle suunnittelemat ja soveltamat *ohjaimet/procedures/functions/properties*. Yksi DLL-tiedosto voidaan myös jakaa eri Windows-ohjelmien kesken. Nämä laajennustiedostot ovat elintärkeitä Windows-ohjelmien sujuvan toiminnan kannalta laitteessasi, koska ne ovat vastuussa ohjelman eri toimintojen, kuten tiedostojen kirjoittamisesta ja lukemisesta, yhdistämisestä muihin laitteisiin, jotka ovat asennuksesi ulkopuolisia.
Nämä tiedostot voidaan kuitenkin avata vain laitteella, joka tukee mitä tahansa Windows-versiota (windows 7/windows 10/jne.), eikä niitä näin ollen voi avata suoraan laitteella, joka tukee Mac OS:ää. (Jos haluat avata DLL-tiedoston Mac OS:ssä, useat ulkoiset sovellukset voivat auttaa avaamaan ne.)


## DLL-tiedostomuoto ##

DLL-tiedoston on kehittänyt Microsoft, ja sen tunniste .dll edustaa tyyppiä. Se on ollut olennainen osa Windows 1.0 -palvelinta ja sen jälkeen. Se on binääritiedostotyyppi, ja sitä tukevat kaikki Microsoft Windowsin versiot. Tämä tiedostotyyppi luotiin keinona luoda jaettu kirjastojärjestelmä Windows-ohjelmien sisällä, jotta ohjelmakirjastoissa voidaan tehdä erillisiä ja itsenäisiä muokkauksia tai muutoksia ilman ohjelmien uudelleenlinkittämistä.


## DLL-esimerkki ##

Esimerkkikoodi DLL-tulopisteelle löytyy alta:

```
BOOL APIENTRY DllMain(
HANDLE hModule,// Handle to DLL module
DWORD ul_reason_for_call,// Reason for calling function
LPVOID lpReserved ) // Reserved
{
    switch ( ul_reason_for_call )
    {
        case DLL_PROCESS_ATTACHED: // A process is loading the DLL.
        break;
        case DLL_THREAD_ATTACHED: // A process is creating a new thread.
        break;
        case DLL_THREAD_DETACH: // A thread exits normally.
        break;
        case DLL_PROCESS_DETACH: // A process unloads the DLL.
        break;
}
    return TRUE;
}

```

## Viite ##

* [DLL - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/deployment/dynamic-link-library)
