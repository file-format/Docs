{
  "date" : "2022-03-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier NUPKG - Fișier pachet NuGet",
  "description":"Aflați despre formatul de fișier NUPKG și despre API-urile care pot crea și deschide fișiere NUPKG.",
  "linktitle" : "NUPKG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-09"
}

## Ce este un fișier NUPKG?

Un fișier NUPKG este un fișier pachet care conține cod sursă care va fi utilizat de software-ul NuGet pentru a crea pachete care să fie utilizate în proiecte .NET. Componenta NuGet Package Manager este instalată ca parte a Microsoft Visual Studio pentru preluarea pachetelor din depozitul de găzduire a pachetelor online. Fișierele NUPKG îi ajută pe dezvoltatori să preia cele mai recente pachete de pe [Nuget.org](https://nuget.org) folosind NuGet Package Manager în loc să descarce și să instaleze manual pachetele de dezvoltare. Fișierele NUPKG sunt construite din fișiere NUSPEC și, atunci când sunt preluate, instalează pachetul pe sistemul utilizatorului.

## Format de fișier NUPKG

Fișierele NUPKG sunt arhive [ZIP](/ro/compression/zip/) care conțin bibliotecile ambalate în interiorul lor. Când este descărcat, poate fi redenumit în .zip și extras cu orice utilitare standard zip, cum ar fi WinZIP, 7-Zip și Apple Archive Utility.

## Referinţă

* [Nuget.org](https://nuget.org)
* [Pornire rapidă: Instalați și utilizați un pachet în Visual Studio (numai Windows)](https://docs.microsoft.com/en-us/nuget/quickstart/install-and-use-a-package-in-visual- studio)
* [Cum se creează și se publică un pachet Nuget](https://docs.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package-using-visual-studio?tabs=netcore- cli)

