{
  "date" : "2021-08-10",
  "keywords" :[ "soubor .ova", "formát souboru", "co je soubor .ova", "soubor", "přípona souboru"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Zjistěte, co je formát souboru .ova a rozhraní API, která mohou vytvářet a otevírat soubory ova.",
  "title" :"Formát souboru OVA - Otevřít soubor virtuálního zařízení",
  "linktitle" : "OVA",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## Co je soubor OVA?

Soubor OVA (Open Virtual Appliance) je adresář OVF uložený jako archiv pomocí archivačního formátu .tar. Jedná se o soubor balíčku virtuálního zařízení, který obsahuje soubory pro distribuci softwaru, který běží na virtuálním počítači. Balíček OVA obsahuje soubor deskriptoru [.ovf](/cs/disc-and-media/ovf/), soubory certifikátů, volitelný soubor [.mf](/cs/programming/mf/) spolu s dalšími souvisejícími soubory. Soubory OVA mají typ média jako application/ovf.

## Formát souboru OVA

Jak již bylo zmíněno, soubor OVA je archivní soubor, který je vytvořen pomocí adresáře OVF ve formátu souboru TAR. Samotný soubor je uložen jako binární soubor. Většina virtualizačních platforem, jako jsou VMware, Microsoft, Oracle a Citrix, může instalovat virtuální zařízení ze souboru OVF, což je soubor deskriptoru s podrobnostmi o obrazu, který se má načíst do virtuálního počítače.

## Výhody souboru OVA

* Soubory OVA jsou komprimovány, což umožňuje rychlejší stahování.
* Klient vSphere ověří soubor OVA před jeho importem a zajistí, že je kompatibilní se zamýšleným cílovým serverem. Pokud zařízení není kompatibilní s vybraným hostitelem, nelze jej importovat a zobrazí se chybová zpráva.
* OVA může zapouzdřit vícevrstvé aplikace a více než jeden virtuální stroj.

## Reference

* [Formáty a šablony souborů OVA](https://docs.vmware.com/en/VMware-vSphere/7.0/com.vmware.vsphere.vm_admin.doc/GUID-AE61948B-C2EE-436E-BAFB-3C7209088552.html )
* [Specifikace formátu souboru OVF](https://products.conholdate.app/viewer/view/3XKCLQbwAw/open-virtualization-format-specification-dsp0243_1-1-0.pdf)

