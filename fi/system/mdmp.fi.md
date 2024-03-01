{
  "date": "2022-08-19",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MDMP-tiedosto - Windows Minidump -tiedostomuoto",
  "description": "Opi MDMP-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata MDMP-tiedostoja.",
  "linktitle": "MDMP",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-mdm-fip"
}
},
  "lastmod": "2022-08-19"
}

## Mikä on MDMP-tiedosto?

MDMP-tiedosto on Microsoft Windows -sovelluksen muistivedos, joka luodaan, kun sovellus sulkeutuu epänormaalisti tai kaatuu. Se sisältää tietoja ja datavedoksia, joita voidaan käyttää kaatumisen syyn selvittämiseen. MDMP-tiedostoja voidaan soveltaa minkä tahansa alustan luomiin sovelluksiin, kuten Java, C++, .NET ja muut. MDMP:n lisäksi

Sovelluksia, jotka voivat avata MDMP-tiedostoja, ovat Microsoft Visual Studio Debugger.

## MDMP tiedostomuoto

MDMP-tiedostot tallennetaan binääritiedostoina levylle ja ne voidaan avata Microsoft Visual Studion debuggerilla. Se sisältää seuraavat tiedot, jotka auttavat tunnistamaan onnettomuuden syyn.

 * Stop-viestin tiedot, sen parametrit ja muut tiedot
 * Luettelo ladatuista ohjaimista
 * Prosessorikonteksti (PRCB) prosessorille, joka lakkasi toimimasta
 * Pysähtyneen prosessin prosessitiedot ja ytimen konteksti (EPROCESS).
 * Käsittele pysäytetyn säikeen tiedot ja ytimen konteksti (ETHREAD).
 * Ydintilan kutsupino pysähtyneelle säikeelle

Nämä tiedot auttavat selvittämään, mitä tapahtui, korjaamaan ongelman ja estämään sen toistumisen.

### Analysoi Minidump

Windows vaatii sivutustiedoston käynnistystaltiolla muistivedostiedoston luomiseksi. Sivutustiedosto luodaan käynnistystaltiolle ja sen tulee olla kooltaan vähintään 2 megatavua (MB). Vetotiedosto luodaan, kun sovellus kaatuu. Toisen ongelman sattuessa luodaan toinen pieni muistivedostiedosto, kun taas edellinen säilytetään. Vetotiedoston nimi on erillinen päällekirjoittamisen välttämiseksi.

Windows pitää luettelon kaikista muistivedostiedostoista %SystemRoot%\Minidump-kansiossa. Voit analysoida MDMP-tiedostoja suorittamalla ne Visual Studio Debuggerissa alla olevien ohjeiden mukaisesti.

## Kuinka avaan MDMP-tiedoston Visual Studiossa?

Seuraavien vaiheiden avulla voidaan avata MDMP-tiedosto Visual Studiossa.

 * Valitse Visual Studion Tiedosto-valikosta Avaa | Crash Dump.
 * Siirry vedostiedostoon, jonka haluat avata.
 * Valitse Avaa.

## Viite

* [Windowsin luoman pienen muistivedostiedoston lukeminen kaatuessa](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump -tiedosto)


