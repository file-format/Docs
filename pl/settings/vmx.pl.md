{
"data": "2023-06-08",
  "keywords": [
"plik vmx",
"co to jest plik vmx",
"przykład pliku vmx",
"jak otworzyć plik vmx",
"co zawiera plik vmx",
"jaki jest format pliku vmx",
"plik",
"rozszerzenie pliku vmx",
"rozszerzenie"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format pliku VMX - plik konfiguracyjny maszyny wirtualnej VMware",
  "description":"Dowiedz się o formacie VMX i interfejsach API, które umożliwiają tworzenie i otwieranie plików VMX.",
"tytuł łącza": "VMX",
  "menu": {
    "docs": {
      "identifier": "settings-vmx",
      "parent": "settings"
}
},
"lastmod": "2023-06-08"
}

## Czym jest plik VMX?

Plik VMX, znany również jako plik konfiguracyjny maszyny wirtualnej, to zwykły plik tekstowy używany przez oprogramowanie do wirtualizacji VMware do definiowania ustawień i konfiguracji maszyny wirtualnej (VM). Pliki VMX zawierają informacje, takie jak konfiguracja sprzętowa maszyny wirtualnej, mapowania dysków wirtualnych, ustawienia sieciowe i inne parametry.

## Przykład pliku VMX

Oto przykład tego, jak może wyglądać plik VMX:

```
# version for configuration
config.version = "8"
# version for virtual machine (Regular version is 4)
virtualHW.version = "7"
# enable vnc
RemoteDisplay.vnc.enabled = "TRUE"
RemoteDisplay.vnc.port = "5900"
VMware, Inc. 3

# type of guest os
guestOS = "linux"
# display name for the VI Client/WebCenter
displayName = "RHEL3"
# scsi controller 0
scsi0.present = "true"
scsi0.virtualDev = "lsilogic"
# scsi hard drive
scsi0:0.present = "true"
scsi0:0.fileName = "/volumes/your-path/passthru.vmdk"
scsi0:0.deviceType = "scsi-hardDisk"
scsi0:0.redo = ""
# IDE CD drive
ide0:0.present ="true"
ide0:0.startConnected = "TRUE"
ide0:0.fileName = "/volumes/your-path/your-iso-image"
ide0:0.deviceType = "cdrom-image"
memsize = "512"
sched.mem.max = "512"
sched.mem.minsize = "512"
sched.swap.derivedName = "/volumes/your-path/passthru-12345.vswp"
svga.vramSize = "16777216"
```

## Co zawiera plik VMX?

Plik VMX zawiera różne ustawienia konfiguracyjne maszyny wirtualnej (VM). Oto niektóre z często spotykanych ustawień w pliku VMX:

- `.encoding:` Określa kodowanie znaków użyte w pliku.
- `config.version:` Wskazuje wersję formatu pliku VMX.
- `virtualHW.version:` Określa wersję sprzętu wirtualnego dla maszyny wirtualnej.
- `guestOS:` Określa system operacyjny gościa zainstalowany na maszynie wirtualnej.
- `memSize:` Określa ilość pamięci przydzielonej maszynie wirtualnej.
- `displayName:` Ustawia nazwę wyświetlaną lub etykietę maszyny wirtualnej.
- `powerType:` Definiuje zachowanie zasilania dla różnych operacji (wyłączenie, włączenie, reset, zawieszenie).
- `floppyX:` Ustawienia konfiguracyjne związane ze stacjami dyskietek, takie jak obecność i mapowanie plików.
- `numvcpus:` Określa liczbę wirtualnych procesorów przypisanych do maszyny wirtualnej.
- `scsiX:` Ustawienia konfiguracyjne dla kontrolerów SCSI i powiązanych z nimi dysków wirtualnych.
- `ethernetX:` Ustawienia konfiguracyjne kart sieciowych, w tym typ urządzenia wirtualnego, nazwa sieci i typ adresu.
- `ideX:` Ustawienia konfiguracyjne dla kontrolerów IDE i powiązanych z nimi dysków wirtualnych.
- `usbX:` Ustawienia konfiguracyjne urządzeń USB, takie jak szczegóły obecności i połączenia.
- `dźwięk:` Ustawienia konfiguracyjne wirtualnego adaptera dźwiękowego.
- `tools.syncTime:` Wskazuje, czy włączona jest synchronizacja czasu z systemem hosta.
- `uuid.bios:` Określa identyfikator UUID BIOS-u maszyny wirtualnej.
- `uuid.location:` Określa identyfikator UUID lokalizacji maszyny wirtualnej.

## Jak otworzyć plik VMX?

Nie zaleca się ręcznego otwierania pliku VMX. Kiedy uruchamiasz maszynę wirtualną za pomocą VMware Fusion, oprogramowanie automatycznie ładuje informacje z pliku VMX.

Jeśli jednak chcesz ręcznie edytować plik VMX, możesz to zrobić za pomocą dowolnego edytora tekstu, np. Notatnika (Windows) lub TextEdit (Mac).

## Jaki jest format pliku VMX?

Plik VMX to zwykły plik tekstowy o określonym formacie. Format jest zgodny ze strukturą pary klucz-wartość, w której każda linia reprezentuje osobną opcję konfiguracji.

Ogólny format pliku VMX jest następujący:

```
key1 = value1
key2 = value2
key3 = value3
```

Każda linia składa się z klucza, po którym następuje znak równości (=) i odpowiednia wartość. Klucz reprezentuje określone ustawienie konfiguracyjne, a wartość reprezentuje wartość przypisaną do tego ustawienia.

Na przykład `memSize = "8192"` w pliku VMX określa, że limit pamięci maszyny wirtualnej wynosi 8192 MB pamięci RAM.

Format pliku VMX może zawierać także komentarze oznaczone znakiem krzyżyka (#) na początku linii, które są ignorowane przez oprogramowanie VMware podczas analizowania pliku. Komentarze są często używane w celu dostarczenia dodatkowych informacji lub wyjaśnień dotyczących określonych ustawień.

## Bibliografia
* [Przykładowy plik VMX](https://www.vmware.com/pdf/vsp_4_vmdirectpath_host.pdf)




