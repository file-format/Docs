{
  "date" : "2021-06-29",
  "keywords" :[ "CUR", "tillägg", "fil", "format", "bild", "Enhetsoberoende bitmapp", "markörfilformat", "markör", "Windows", "applikation" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CUR - Cursor File Format",
  "description":"Läs mer om CUR-filformat och API:er som kan skapa och öppna CUR-filer.",
  "linktitle" : "CUR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-06-29"
}

## Vad är CUR fil? ##

En CUR-fil är ett statiskt Microsoft Windows-markörfilformat. I grund och botten är de stationära bilder identiska med ICO-filer (ikon) på alla sätt utom tillägget. Både CUR och [ICO](/sv/image/ico/) är etablerade på basis av specifikationen för enhetsoberoende bitmapp [DIB](/sv/image/dib/) (enhetsoberoende bitmapp). Standard, samt anpassad markör som Windows muspekare för Windows operativsystem, lagras i CUR-filer. Det kan vara en pil för normal användning, ett snurrande timglas för att visa väntetider eller en I-stapel för textredigering. CUR-filer kommer tillsammans med installationspaketet för de anpassade skrivbordsteman för att säkerställa att Windows-markören matchar det anpassade skrivbordstemat.

## Teknisk specifikation ##

CUR-filer är binära systemfiler som kan hittas på enheter som fungerar på Microsoft Windows operativsystem. CUR-pekarbilder finns i olika standardstorlekar som 16×16, 32×32, etc. CUR-filer är väldigt lika ICO-filerna; båda består av små stationära bilder. Endast förlängningen av CUR- och ICO-filer är olika. Dessutom är förklaringen av en hotspot i rubriken på CUR-filen skild från ICO-filen. Hotspot tolkar pixelförskjutningen från det övre vänstra hörnet till den plats där du pekar med musen. Windows-system använder fortfarande CUR-filerna, men nu har de animerade markörerna vanligtvis filtillägget ANI istället för CUR.

## Kortfattad bakgrund ##

CUR-filen är gjord från ICO-filen. Det första CUR-filformatet införlivades i Microsofts Windows 1.0-operativsystem 1981 för att underlätta kommersiell användning. Snart introducerades fler interaktiva markörer som gör det möjligt för användare att ändra sina markörinställningar från de förinstallerade alternativen. Det är dock lätt att redigera en CUR-fil på egen hand även om du har otillräcklig teknisk kunskap.


## CUR exempel ##

CUR-filerna finns på *C:\Windows\Cursors* :

{{< figure src="../cur.png" alt="CUR filformat" >}}

