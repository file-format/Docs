{
  "date" : "2021-08-10",
  "keywords" :[ "plik .ova", "format pliku", "co to jest plik .ova", "plik", "rozszerzenie pliku"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Dowiedz się, co to jest format pliku .ova i interfejsy API, które mogą tworzyć i otwierać pliki ova.",
  "title" :"Format pliku OVA - Otwórz plik urządzenia wirtualnego",
  "linktitle" : "OVA",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## Czym jest plik OVA?

Plik OVA (Open Virtual Appliance) to katalog OVF zapisany jako archiwum przy użyciu formatu archiwizacji .tar. Jest to plik pakietu urządzenia wirtualnego, który zawiera pliki do dystrybucji oprogramowania działającego na maszynie wirtualnej. Pakiet OVA zawiera plik deskryptora [.ovf](/pl/disc-and-media/ovf/), pliki certyfikatów, opcjonalny plik [.mf](/pl/programming/mf/) wraz z innymi powiązanymi plikami. Pliki OVA mają typ nośnika jako application/ovf.

## Format pliku OVA

Jak wspomniano, plik OVA to plik archiwum utworzony przy użyciu katalogu OVF w formacie pliku TAR. Sam plik jest zapisywany jako plik binarny. Większość platform wirtualizacyjnych, takich jak VMware, Microsoft, Oracle i Citrix, może instalować urządzenia wirtualne z pliku OVF, który jest plikiem deskryptora zawierającym szczegóły obrazu, który ma zostać załadowany do maszyny wirtualnej.

## Zalety pliku OVA

* Pliki OVA są skompresowane, co pozwala na szybsze pobieranie.
* Klient vSphere weryfikuje plik OVA przed jego zaimportowaniem i upewnia się, że jest on zgodny z docelowym serwerem. Jeśli urządzenie jest niezgodne z wybranym hostem, nie można go zaimportować i pojawia się komunikat o błędzie.
* OVA może hermetyzować aplikacje wielowarstwowe i więcej niż jedną maszynę wirtualną.

## Bibliografia

* [Formaty i szablony plików OVA](https://docs.vmware.com/en/VMware-vSphere/7.0/com.vmware.vsphere.vm_admin.doc/GUID-AE61948B-C2EE-436E-BAFB-3C7209088552.html )
* [Specyfikacje formatu plików OVF](https://products.conholdate.app/viewer/view/3XKCLQbwAw/open-virtualization-format-specification-dsp0243_1-1-0.pdf)

