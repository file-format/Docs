{
  "date" : "2021-06-11",
  "keywords" :[ "wpl", "fișier wpl", "extensie", "format", "ce este un fișier wpl", "muzică", "format fișier wpl"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier WPL și despre API-urile care pot crea, converti și deschide fișiere WPL.",
  "title" :"WPL - Fișier listă de redare Windows Media Player",
  "linktitle" : "WPL",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## Ce este un fișier WPL?

Un fișier cu extensia .wpl conține lista de redare a melodiilor care urmează să fie rulate pe Microsoft Windows Media Player. Aceste fișiere sunt de obicei create de utilizatori pentru colecțiile lor video și audio. Conținutul scris într-un fișier WPL este doar căi de director sau locații pentru fișierele multimedia selectate de creatorul fișierului .wpl, astfel încât aplicația media player poate găsi și reda prompt conținutul multimedia din locațiile directorului lor.

## Format de fișier WPL

WPL (Windows Media Player Playlist) este un format de fișier proprietar utilizat în Microsoft Windows Media Player versiunile 9 sau mai mari. Este un format de fișier de computer care stochează liste de redare multimedia. În mod implicit, lista de redare este salvată cu o extensie .wpl (Windows Media Player Playlist). Puteți utiliza în schimb extensia [.m3u](/ro/audio/m3u/), dacă doriți să redați discurile de date pe un dispozitiv care nu acceptă această extensie. Elementele unui fișier WPL sunt reprezentate în format XML.

Elementul de nivel superior „smil” specifică faptul că elementele fișierului urmează structura Synchronized Multimedia Integration Language (SMIL). Fișierul este creat și salvat cu extensia .wpl, iar tipul său MIME este application/vnd.ms-wpl.

### Exemplu WPL

Iată un exemplu de fișier wpl:
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




## Referințe ##

* [MPEG-1 Audio Layer II - După Wikipedia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

