{
  "date" : "2022-11-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Soubor BIF - formát celého snímku Ventana",
  "description":"Další informace o formátu souborů BIF a rozhraních API, která mohou vytvářet a otevírat soubory BIF.",
  "linktitle" : "BIF",
  "menu" : {
    "docs" : {
      "identifier":"image-bif",
      "parent" : "image"
}
},
  "lastmod" : "2022-11-17"
}

## Co je soubor BIF?

Soubor BIF je soubor rastrového obrázku, který obsahuje obrázek vzorku snímku. Skládá se z více obrázků TIFF, které jsou zkombinovány aplikacemi pro prohlížení snímků do jednoho složeného obrázku. Soubory BIF jsou vytvářeny digitálním skenerem diapozitivů Ventana Medical systems a jsou plně kompatibilní s variantou BigTIFF definice [TIFF](/cs/image/tiff/) v 6.0.

## Formát souboru BIF

Soubor BIF se uloží jako soubor binárního obrázku a sestává z až 200 000 x 200 000 pixelů. To může vést k velkým velikostem souborů, čímž dojde k porušení limitu velikosti 4 GB stanoveného ukazateli 32bitových souborů definovaných standardem TIF. U 64bitových ukazatelů souborů je však tato bariéra velikosti souboru překonána variantou BigTIFF standardu TIFF.

### Kdo používá soubor BIF?

Soubory BIF používají digitální skenery diapozitivů ke skenování a vytváření digitálních kopií vzorků diapozitivů. Pokud jste patolog, můžete tyto soubory BIF otevřít v aplikacích pro prohlížení snímků. Díky vysoké úrovni detailů a datům s vysokým rozlišením můžete přibližovat a oddalovat snímek snímku a prohlížet si tak řezy vzorků s více či méně podrobnostmi. Soubor metadat [XML](/cs/web/xml/) přítomný v těchto souborech definuje, jak by měly být obrázky kombinovány, a obrázek, který by měl být použit jako miniatura souboru.

## Jak otevřít soubor BIF?

Soubory BIF můžete otevřít pomocí:

* OpenSlide (pro více platforem)
* ImageJ (pro více platforem)
* NetScope Viewer (Windows)

## Reference ##

* [Roche Digital Pathology BIF Whitepaper](https://diagnostics.roche.com/content/dam/diagnostics/Blueprint/en/pdf/rmd/Roche-Digital-Pathology-BIF-Whitepaper.pdf)

