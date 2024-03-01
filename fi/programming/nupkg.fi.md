{
  "date": "2022-03-09",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "NUPKG-tiedosto - NuGet-pakettitiedosto",
  "description": "Opi NUPKG-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata NUPKG-tiedostoja.",
  "linktitle": "NUPKG",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-nupk-fig"
}
},
  "lastmod": "2022-03-09"
}

## Mikä on NUPKG-tiedosto?

NUPKG-tiedosto on pakettitiedosto, joka sisältää lähdekoodin, jota NuGet-ohjelmisto käyttää .NET-projekteissa käytettävien pakettien luomiseen. NuGet Package Manager -komponentti asennetaan osana Microsoft Visual Studiota pakettien hakemista varten online-pakettien arkistosta. NUPKG-tiedostot auttavat kehittäjiä noutamaan uusimmat paketit osoitteesta [Nuget.org](https://nuget.org) NuGet Package Managerin avulla kehityspakettien manuaalisen lataamisen ja asentamisen sijaan. NUPKG-tiedostot rakennetaan NUSPEC-tiedostoista ja asenna paketti käyttäjän järjestelmään noudettaessa.

## NUPKG-tiedostomuoto

NUPKG-tiedostot ovat [ZIP](/compression/zip/)-arkistoja, jotka sisältävät pakatut kirjastot. Kun se ladataan, se voidaan nimetä uudelleen muotoon .zip ja purkaa millä tahansa tavallisella zip-apuohjelmalla, kuten WinZIP, 7-Zip ja Apple Archive Utility.

## Viite

* [Nuget.org](https://nuget.org)

* [Pika-aloitus: Asenna ja käytä pakettia Visual Studiossa (vain Windows)](https://learn.microsoft.com/en-us/nuget/quickstart/install-and-use-a-package-in-visual- studio)

* [Nuget-paketin luominen ja julkaiseminen](https://learn.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package-using-visual-studio?tabs=netcore- cli)


