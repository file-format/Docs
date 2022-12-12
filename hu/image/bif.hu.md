{
  "date" : "2022-11-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BIF fájl - Ventana teljes dia képformátuma",
  "description":"További információ a BIF fájlformátumról és az API-król, amelyek BIF-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "BIF",
  "menu" : {
    "docs" : {
      "identifier":"image-bif",
      "parent" : "image"
}
},
  "lastmod" : "2022-11-17"
}

## Mi az a BIF fájl?

A BIF-fájl egy raszteres képfájl, amely a diaminta képét tartalmazza. Több TIFF-képből áll, amelyeket a dianéző alkalmazások egyetlen összetett képpé egyesítenek. A BIF fájlokat a Ventana Medical Systems digitális diaszkenner hozza létre, és teljes mértékben megfelelnek a [TIFF](/hu/image/tiff/) v 6.0 definíció BigTIFF-változatának.

## BIF fájl formátum

A BIF fájl bináris képfájlként kerül mentésre, és legfeljebb 200 000 x 200 000 képpontból állhat. Ez nagy fájlméretekhez vezethet, ami átlépi a TIF szabvány által meghatározott 32 bites fájlmutatók által megszabott 4 GB-os méretkorlátot. A 64 bites fájlmutatókkal azonban ezt a fájlméret-korlátot a TIFF-szabvány BigTIFF-változata legyőzi.

### Ki használja a BIF fájlt?

A BIF fájlokat a digitális diaszkennerek használják a tárgylemezminták beolvasására és digitális másolatok készítésére. Ha Ön patológus, megnyithatja ezeket a BIF fájlokat dianéző alkalmazásokban. A nagy részletességű és nagy felbontású adatok révén nagyíthatja és kicsinyítheti a diaképet, hogy több vagy kevesebb részletben megtekinthesse a mintadarabokat. Az ezekben a fájlokban található [XML](/hu/web/xml/) metaadatfájl meghatározza a képek kombinálásának módját, és azt, hogy melyik képet kell használni a fájl miniatűrjeként.

## Hogyan lehet megnyitni a BIF fájlt?

A BIF fájlokat a következőkkel nyithatja meg:

* OpenSlide (platformok közötti)
* ImageJ (platformok közötti)
* NetScope Viewer (Windows)

## Hivatkozások ##

* [Roche Digital Pathology BIF Whitepaper](https://diagnostics.roche.com/content/dam/diagnostics/Blueprint/en/pdf/rmd/Roche-Digital-Pathology-BIF-Whitepaper.pdf)

