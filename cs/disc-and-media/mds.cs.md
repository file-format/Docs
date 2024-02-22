{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Přečtěte si o formátu souborů MDS a rozhraních API, která mohou vytvářet a otevírat soubory MDS.",
  "title" : "Formát souboru MDS - Sidecar File Descriptor",
  "linktitle" : "MDS",
  "menu" : {
    "docs" : {
      "identifier":"disc-and-media-mds-cs",
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2023-01-23"
}

## Co je soubor MDS?

MDS (Media Descriptor Sidecar File) je soubor spojený se softwarem Alcohol 120% a Daemon Tools, které se oba používají k vytváření a správě virtuálních jednotek CD a DVD. Soubor MDS obsahuje informace o rozložení dat na disku, včetně umístění všech souborů a struktury disku. To umožňuje virtuální jednotce emulovat chování fyzického disku, takže software může číst data na virtuálním disku, jako by to byl skutečný disk.

When you want to mount an image file to a virtual drive, the MDS file is used along with the corresponding image file in a format such as ISO, BIN or CUE. The MDS file contains a description of the layout of the data on the disc, and the virtual drive software uses this information to create a virtual disc. This allows you to use the software as if you were using a physical disc, without having to physically insert the disc into the drive.

## Vztah s alkoholem 120%

Alcohol 120% je oblíbený software pro vytváření a správu virtuálních jednotek CD a DVD a používá formát souborů MDS k ukládání a přístupu k obrazům disků. Formát souboru MDS je vlastnictvím Alcohol 120% a může být otevřen a používán pouze softwarem Alcohol 120% nebo jiným softwarem, který jej podporuje.

## Jak otevřít soubor MDS?

Chcete-li otevřít soubor MDS v Alcohol 120%, musíte mít na svém počítači nainstalovaný software. Jakmile budete mít Alcohol 120% nainstalovaný, můžete otevřít soubor MDS takto:

1. Spustit Alcohol 120%.
2. Klikněte na nabídku Soubor a vyberte Otevřít.
3. Přejděte do umístění souboru MDS v počítači a vyberte jej.
4. Soubor MDS se nyní otevře v Alcohol 120% a budete vyzváni k výběru odpovídajícího souboru obrázku (jako je ISO, BIN nebo CUE).
5. Po výběru souboru s obrazem Alcohol 120 % připojí obraz na virtuální disk.

Případně můžete také otevřít soubor MDS dvojitým kliknutím na něj, pokud je Alcohol 120% nastaven jako výchozí program pro otevírání souborů MDS. Můžete také použít jiný software, který podporuje formát MDS, jako je Daemon Tools, Virtual CloneDrive, Virtual Drive Manager a MagicISO.

## Reference
* [Alcohol 120% – software pro vypalování CD a DVD](https://www.alcohol-soft.com/)


