{
  "date" : "2021-02-26",
  "keywords" :[ "OPUS", "soubor", "přípona", "formát", "Kódování zvuku"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů OPUS a rozhraních API, která mohou vytvářet a otevírat soubory OPUS.",
  "title" :"OPUS",
  "linktitle" : "OPUS",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-02-26"
}

## Co je soubor OPUS?

Opus je formát audio souborů vytvořený nadací Xiph.Org a později standardizovaný organizací IETF (Internet Engineering Task Force). Byl vyvinut hlavně pro internetové streamování, Voice over IP (VOIP), videokonference a chat ve hře, a proto je navržen tak, aby si zachoval nízkou latenci při zachování interaktivní komunikace v reálném čase. Aby byla zachována kvalita zvuku souboru Opus, mnoho testů slepého poslechu označilo Opus za vysoce kvalitní zvukový formát než jakýkoli jiný zvukový formát při jakémkoli datovém toku.

## Specifikace formátu souborů OPUS

Formát Opus využívá kodeky SILK (používá Skype) i Xiph.Org a podporuje variabilní přenosové rychlosti od 6 kb/s do 510 kb/s. Rozšíření Opus používá řečově orientovaný algoritmus SILK založený na LPC a algoritmus CELT založený na MDCT s nižší latencí, někdy přepíná mezi oběma nebo někdy kombinací obou algoritmů pro zajištění maximální účinnosti. Soubory ve formátu Opus mají příponu .opus. Na rozdíl od formátu souboru Vorbis Opus nevyžaduje velké číselníky pro každý jednotlivý soubor, proto je tento formát poměrně efektivní.

## Reference ##

* [OPUS – z Wikipedie](https://en.wikipedia.org/wiki/Opus_(audio_format))

