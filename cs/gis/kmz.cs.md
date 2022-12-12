{
  "date" : "2019-10-11",
  "keywords" :[ "soubor kmz", "co je soubor kmz", "soubor", "příklad kmz", "přípona souboru kmz", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KMZ - KML komprimovaný formát souboru",
  "description":"Další informace o formátu souboru KMZ a rozhraních API, která mohou vytvářet a otevírat soubory KMZ.",
  "linktitle" : "KMZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor KMZ?

Soubor KMZ (KML Zipped) je reprezentace komprimovaného souboru [KML](/cs/gis/kml/), který obsahuje geoprostorové informace zobrazitelné v aplikacích GIS, jako je Google Earth. Informace o značkách míst jsou v souboru uvedeny jako zeměpisná šířka a délka spolu s vlastním názvem. Jediný zabalený soubor KMZ lze snadno sdílet s ostatními uživateli. Soubory KMZ mohou obsahovat data 3D modelu i pro geografickou reprezentaci modelu. Soubor KMZ lze otevřít v Mapách Google uložením souboru do online umístění a zadáním adresy URL do vyhledávacího pole v Mapách Google.

## Struktura souboru ##

Obsah souboru MKZ se skládá z hlavního souboru KML a žádného nebo více přidružených souborů. Lze jej extrahovat pomocí standardního dekompresního nástroje, jako je WinZIP. Formát souboru KMZ je také komprimován do archivu s kompresním poměrem 10:1. Data z aplikace Google Earth, jako jsou aplikace, můžete exportovat přímo do formátu souboru KMZ. Hlavní soubor KML se jmenuje **doc.kml**. Při balení souboru KMZ do něj lze přidat více než jeden soubor KML, ale to nebude přínosné, protože aplikace Google Earth při otevírání souboru KMZ vyhledá první soubor KML a přečte jej. Ignoruje všechny další soubory KML nalezené v archivu. Chcete-li mít jistotu, že aplikace Google Earth přečte požadovaný soubor KML, doporučujeme do souboru KMZ umístit pouze jeden soubor KML.

Obrázky, modely, textury, zvukové soubory a další zdroje uvedené v souboru doc.kml jsou umístěny v jiné podsložce v hlavní složce. To může také zahrnovat určitou složitost v závislosti na počtu podpůrných souborů. Odkazy na tyto základní zdroje mohou být odkazovány relativně nebo prostřednictvím absolutního odkazování.

### Relativní odkazování ###

Když jsou zdroje umístěny vedle hlavního doc.kml v podsložce v hlavní složce, může relativní odkaz odkazovat na tyto podpůrné soubory, jak je znázorněno v následujícím příkladu (pouze pro ikonu).

```
<IconStyle>
  <scale>1.1</scale>
  <Icon>
    <href>files/icon_surfing.png</href>
  </Icon>
</IconStyle>
```

### Absolutní odkazování ###

Zdroje mohou být odkazovány úplně stejně. Absolutní odkazy obsahují úplnou adresu URL propojeného souboru. Když jsou soubory umístěny na centrální server, absolutní odkazování zajišťuje, že zůstávají jednoznačné ve srovnání s relativním odkazováním. Nedoporučuje se absolutně odkazovat na místní soubor, protože tyto odkazy se při přesunu souborů do nového systému přeruší. Příklad absolutního odkazování je následující:

```
<Icon>
  <href>http://maps.google.com/mapfiles/kml/pushpin/ylw-pushpin.png</href>
</Icon>
```

## Viz také ##

* [GeoJSON](/cs/gis/geojson/)

## Reference ##

* [Soubory Google Earth a KMZ](https://developers.google.com/kml/documentation/kmzarchives#google-earth-and-kmz-archives)

