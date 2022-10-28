{
  "date" : "2021-08-10",
  "keywords" :[ ".ova-Datei", "Dateiformat", "was ist eine .ova-Datei", "Datei", "Dateierweiterung"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Erfahren Sie, was ein .ova-Dateiformat und APIs sind, die ova-Dateien erstellen und öffnen können.",
  "title" :"OVA-Dateiformat - Datei der virtuellen Appliance öffnen",
  "linktitle" : "OVA",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## Was ist eine OVA-Datei?

Eine OVA-Datei (Open Virtual Appliance) ist ein OVF-Verzeichnis, das als Archiv im .tar-Archivierungsformat gespeichert wird. Es handelt sich um eine Paketdatei für virtuelle Appliances, die Dateien zur Verteilung von Software enthält, die auf einer virtuellen Maschine ausgeführt wird. Ein OVA-Paket enthält eine [.ovf](/de/disc-and-media/ovf/)-Deskriptordatei, Zertifikatsdateien, eine optionale [.mf](/de/programming/mf/)-Datei zusammen mit anderen zugehörigen Dateien. OVA-Dateien haben den Medientyp application/ovf.

## OVA-Dateiformat

Wie bereits erwähnt, ist eine OVA-Datei eine Archivdatei, die mithilfe des OVF-Verzeichnisses im TAR-Dateiformat erstellt wird. Die Datei selbst wird als Binärdatei gespeichert. Die meisten Virtualisierungsplattformen wie VMware, Microsoft, Oracle und Citrix können virtuelle Appliances aus einer OVF-Datei installieren, bei der es sich um eine Deskriptordatei mit den Details des in die virtuelle Maschine zu ladenden Abbilds handelt.

## Vorteile einer OVA-Datei

* OVA-Dateien sind komprimiert, was schnellere Downloads ermöglicht.
* Der vSphere-Client validiert eine OVA-Datei vor dem Importieren und stellt sicher, dass sie mit dem beabsichtigten Zielserver kompatibel ist. Wenn die Appliance nicht mit dem ausgewählten Host kompatibel ist, kann sie nicht importiert werden und es wird eine Fehlermeldung angezeigt.
* OVA kann mehrschichtige Anwendungen und mehr als eine virtuelle Maschine kapseln.

## Verweise

* [OVA-Dateiformate und -Vorlagen](https://docs.vmware.com/en/VMware-vSphere/7.0/com.vmware.vsphere.vm_admin.doc/GUID-AE61948B-C2EE-436E-BAFB-3C7209088552.html )
* [OVF-Dateiformatspezifikationen](https://products.conholdate.app/viewer/view/3XKCLQbwAw/open-virtualization-format-specification-dsp0243_1-1-0.pdf)

