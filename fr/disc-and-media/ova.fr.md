{
  "date" : "2021-08-10",
  "keywords" :[ "fichier .ova", "format de fichier", "qu'est-ce qu'un fichier .ova", "fichier", "extension de fichier"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Découvrez ce qu'est un format de fichier .ova et les API qui peuvent créer et ouvrir des fichiers ova.",
  "title" :"Format de fichier OVA - Ouvrir le fichier de l'appliance virtuelle",
  "linktitle" : "OVA",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## Qu'est-ce qu'un fichier OVA ?

Un fichier OVA (Open Virtual Appliance) est un répertoire OVF enregistré en tant qu'archive au format d'archivage .tar. Il s'agit d'un fichier de package d'appliance virtuelle qui contient des fichiers pour la distribution de logiciels qui s'exécutent sur une machine virtuelle. Un package OVA contient un fichier descripteur [.ovf](/fr/disc-and-media/ovf/), des fichiers de certificat, un fichier facultatif [.mf](/fr/programming/mf/) ainsi que d'autres fichiers associés. Les fichiers OVA ont le type de média application/ovf.

## Format de fichier OVA

Comme mentionné, un fichier OVA est un fichier d'archive créé à l'aide du répertoire OVF au format de fichier TAR. Le fichier lui-même est enregistré en tant que fichier binaire. La plupart des plates-formes de virtualisation, telles que VMware, Microsoft, Oracle et Citrix, peuvent installer des appliances virtuelles à partir d'un fichier OVF qui est un fichier descripteur contenant les détails de l'image à charger dans la machine virtuelle.

## Avantages d'un fichier OVA

* Les fichiers OVA sont compressés, ce qui permet des téléchargements plus rapides.
* Le client vSphere valide un fichier OVA avant de l'importer et s'assure qu'il est compatible avec le serveur de destination prévu. Si l'appliance est incompatible avec l'hôte sélectionné, elle ne peut pas être importée et un message d'erreur s'affiche.
* OVA peut encapsuler des applications multiniveaux et plusieurs machines virtuelles.

## Références

* [Formats et modèles de fichiers OVA](https://docs.vmware.com/en/VMware-vSphere/7.0/com.vmware.vsphere.vm_admin.doc/GUID-AE61948B-C2EE-436E-BAFB-3C7209088552.html )
* [Spécifications du format de fichier OVF](https://products.conholdate.app/viewer/view/3XKCLQbwAw/open-virtualization-format-specification-dsp0243_1-1-0.pdf)

