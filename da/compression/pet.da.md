{
  "date" : "2022-06-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "PET-filformat - Puppy Linux Install Package File",
  "description":"Lær om PET-filformat og API'er, der kan oprette og åbne PET-filer.",
  "linktitle" : "PET",
  "menu" : {
    "docs" : {
      "identifier":"compression-pet-da",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-23"
}

## Hvad er en Linux PET fil?

En PET-fil er en applikationsinstallationspakkefil, der er oprettet og brugt med PuppyLinux-varianten af Linux-operativsystemet. Den er oprettet som en komprimeret [TGZ](/compression/tgz/) fil, der reducerer filstørrelsen på det komprimerede arkiv. Integriteten af PET-filformatet sikres af md5sum-kontrolsummen, der er tilføjet til slutningen af filen til verifikation i den eksterne ende. PET-filer kan udpakkes ved hjælp af standard TGZ-filudtrækkeren og WinRAR. PET-filer erstattede de gamle [PUP](/compression/pup/)-pakkeinstallationsfiler.

## PET filformat

PET-filer gemmes på disken som komprimerede arkiver i binært filformat. De interne filformatdetaljer for PET-filformatet kendes dog ikke. I lighed med [.exe](/executable/exe/)- og [.msi](/executable/msi/)-pakkeinstallationsfilerne starter PET-filerne en installation, når de udføres.

## Referencer

 * [PuppyLinux](https://en.wikipedia.org/wiki/Puppy_Linux)
 * [Indeks over PuppyLinux PET-pakker](https://distro.ibiblio.org/puppylinux/pet-packages-lucid/)

