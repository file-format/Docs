{
  "date" : "2022-06-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku PET — plik pakietu instalacyjnego Puppy Linux",
  "description":"Poznaj format plików PET i interfejsy API, które mogą tworzyć i otwierać pliki PET.",
  "linktitle" : "PET",
  "menu" : {
    "docs" : {
      "identifier":"compression-pet",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-23"
}

## Co to jest plik Linux PET?

Plik PET to plik pakietu instalacyjnego aplikacji utworzony i używany z wariantem PuppyLinux systemu operacyjnego Linux. Jest tworzony jako skompresowany plik [TGZ](/pl/compression/tgz/), który zmniejsza rozmiar pliku skompresowanego archiwum. Integralność formatu pliku PET jest zapewniona przez sumę kontrolną md5, która jest dołączana na końcu pliku w celu weryfikacji na zdalnym końcu. Pliki PET można wyodrębnić za pomocą standardowego ekstraktora plików TGZ i WinRAR. Pliki PET zastąpiły stare pliki instalacyjne pakietów [PUP](/pl/compression/pup/).

## Format pliku PET

Pliki PET są zapisywane na dysku jako skompresowane archiwa w formacie pliku binarnego. Jednak wewnętrzne szczegóły formatu plików PET nie są znane. Podobnie jak pliki instalacyjne pakietów [.exe](/pl/executable/exe/) i [.msi](/pl/executable/msi/), pliki PET rozpoczynają instalację w momencie ich wykonania.

## Bibliografia

* [PuppyLinux](https://en.wikipedia.org/wiki/Puppy_Linux)
* [Indeks pakietów PuppyLinux PET](https://distro.ibiblio.org/puppylinux/pet-packages-lucid/)

