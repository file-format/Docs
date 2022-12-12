{
  "date" : "2021-08-11",
  "keywords" :[ "plik vdi", "format pliku vdi", "co to jest plik vdi", "plik", "przykład vdi", "rozszerzenie pliku vdi", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Poznaj format plików VDI i interfejsy API, które mogą tworzyć i otwierać pliki VDI.",
  "title" :"VDI - Plik obrazu dysku wirtualnego VirtualBox",
  "linktitle" : "VDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## Czym jest plik VDI?
Plik z rozszerzeniem .vdi jest obrazem dysku wirtualnego; specyficzne dla programu Oracle do wirtualizacji komputerów typu open source o nazwie VirtualBox. Pliki VDI służą do uruchamiania maszyny wirtualnej VirtualBox. Maszyny wirtualne umożliwiają użytkownikom uruchamianie dodatkowych systemów operacyjnych lub programów na jednym komputerze. Dlatego zaletą plików VDI jest to, że użytkownicy mogą zapisywać te pliki obrazów dysków na swoim dysku twardym i uruchamiać je za pomocą emulatorów, kiedy tylko tego potrzebują.

## Format pliku VDI
Virtual Disk Image (VDI) to podstawowy format pliku dysku dla aktywnie rozwijanej maszyny wirtualnej Oracle o otwartym kodzie źródłowym, znanej jako VirtualBox, która jest produktem do wirtualizacji klasy korporacyjnej. Format pliku VDI jest przeznaczony do tworzenia przenośnego obrazu dysku, który można łatwo uruchomić za pomocą innych programów do wirtualizacji. Obsługuje zarówno pamięć alokowaną dynamicznie, jak i pamięć o stałym rozmiarze. Pozwala rozszerzyć plik obrazu po jego utworzeniu, nawet jeśli zawiera już dane.

### Wirtualizacja dysków
System emuluje dyski twarde w formacie obrazu dysku VDI. VirtualBox VM może korzystać z wcześniejszych dysków utworzonych w Microsoft Virtual PC lub VMware, a także własnego formatu natywnego. VirtualBox może również łączyć się z celami iSCSI i surowym partycjonowaniem na hoście, używając jako wirtualnych dysków twardych. VirtualBox emuluje IDE (kontrolery PIIX4 i ICH6), SATA (kontroler ICH8M), kontrolery SAS, do których można podłączyć dyski twarde oraz SCSI.

Wsparcie dla Open Virtualization Format (OVF) jest dostępne od wersji 2.2.0 VirtualBox. Zarówno urządzenia fizyczne podłączone do hosta, jak i obrazy ISO można montować jako napędy CD lub DVD.
Domyślnie VirtualBox obsługuje grafikę za pośrednictwem niestandardowej wirtualnej karty graficznej zgodnej ze standardem VESA.

### Obsługa wirtualizacji dla sieci Ethernet
VirtualBox wirtualizuje następujące karty sieciowe dla karty sieciowej Ethernet:
- AMD PCnet PCI II (Am79C970A)
- AMD PCnet-Fast III (Am79C973)
- Komputer stacjonarny Intel Pro/1000 MT (82540EM)
— Serwer Intel Pro/1000 MT (82545EM)
— Serwer Intel Pro/1000 T (82543GC)
- Parawirtualna karta sieciowa (virtio-net)

Emulowane karty sieciowe umożliwiają działanie systemów gościa bez konieczności wyszukiwania i instalowania sterowników sprzętu sieciowego, ponieważ są one dostępne jako część systemu gościa. Specjalna parawirtualna karta sieciowa poprawia wydajność sieci, zmniejszając potrzebę dopasowania określonego interfejsu sprzętowego. Dlatego wymaga specjalnego wsparcia kierowcy w gościu.


## Bibliografia

* [VirtualBox – z Wikipedii](https://en.wikipedia.org/wiki/VirtualBox#VirtualBox_Disk_Image)


