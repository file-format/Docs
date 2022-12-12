{
  "date" : "2021-06-11",
  "keywords" :[ "wpl", "soubor wpl", "přípona", "formát", "co je soubor wpl", "hudba", "formát souboru wpl"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů WPL a rozhraních API, která mohou vytvářet, převádět a otevírat soubory WPL.",
  "title" :"WPL - Windows Media Player Playlist File",
  "linktitle" : "WPL",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## Co je soubor WPL?

Soubor s příponou .wpl obsahuje seznam skladeb, které mají být spuštěny v programu Microsoft Windows Media Player. Tyto soubory obvykle vytvářejí uživatelé pro své sbírky videa a zvuku. Obsah zapsaný v souboru WPL jsou pouze cesty k adresářům nebo umístění pro multimediální soubory vybrané tvůrcem souboru .wpl, takže aplikace přehrávače médií může okamžitě najít a přehrát multimediální obsah z jejich umístění v adresáři.

## Formát souboru WPL

WPL (Windows Media Player Playlist) je proprietární formát souboru používaný v programu Microsoft Windows Media Player verze 9 nebo vyšší. Jedná se o počítačový formát souborů, který ukládá multimediální seznamy skladeb. Ve výchozím nastavení je seznam stop uložen s příponou .wpl (seznam stop Windows Media Player). Místo toho můžete použít rozšíření [.m3u](/cs/audio/m3u), pokud chcete přehrávat své datové disky v zařízení, které toto rozšíření nepodporuje. Prvky souboru WPL jsou reprezentovány ve formátu XML.

Prvek nejvyšší úrovně „smil“ určuje, že prvky souboru se řídí strukturou SMIL (Synchronized Multimedia Integration Language). Soubor je vytvořen a uložen s příponou .wpl a jeho typ MIME je application/vnd.ms-wpl.

### Příklad WPL

Zde je příklad souboru wpl:
```
<?wpl version="1.0"?>
<smil>
    <head>
        <meta name="Generator" content="Microsoft Windows Media Player -- 11.0.5721.5145"/>
        <meta name="AverageRating" content="33"/>
        <meta name="TotalDuration" content="1102"/>
        <meta name="ItemCount" content="3"/>
        <author/>
        <title>Bach Organ Works</title>
    </head>
    <body>
        <seq>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio01.mp3"/>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio02.mp3"/>
            <media src="SR15.mp3" tid="{35B39D45-94D8-40E1-8FC2-9F6714191E47}"/>
        </seq>
    </body>
</smil>
```




## Reference ##

* [MPEG-1 Audio Layer II – podle Wikipedie](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

