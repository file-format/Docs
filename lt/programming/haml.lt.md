{
  "date": "2022-04-07",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HAML failo formatas – Haml šaltinio kodo failas",
  "description": "Sužinokite apie HAML failo formatą ir API, kurios gali sukurti ir atidaryti HAML failą.",
  "linktitle": "HAML",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ham-ltl"
}
},
  "lastmod": "2022-04-07"
}

## Kas yra HAML failas?

HAML failas yra HTML abstrakcijos žymėjimo kalbos failas, kuriame yra šaltinio kodas, parašytas [Haml](https://haml.info/) kalba. Jis gali būti naudojamas kaip ERB (Ruby šablono scenarijų) pakaitalas. HAML faile yra šablono šaltinio kodas, skirtas žiniatinklio dokumento HTML generavimui. ERB failus galima pakeisti paprasčiausiai pakeičiant šiuos failus programos / rodinių aplanke į Haml, pakeitus failo plėtinį. HAML failus galima atidaryti naudojant bet kurį teksto rengyklę, pvz., Microsoft Notepad, Notepad++, Apple TextEdit,

## HAML failo formatas

HAML failai yra šaltinio failai, įrašyti į diską kaip paprasto teksto failai. Jame yra kodas, parašytas HAML sintaksė. HAML pakeičia **<>** žymas **%** ženklu, kad kodas būtų paprastesnis ir lengvesnis. ERB failus galima pakeisti HAML, kaip parodyta šiame paprastame pavyzdyje.

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### HAML pavyzdys

Toliau pateikiamas HAML pavyzdys Hello World.

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
kuri atvaizduojama į šią HTML išvestį.

```
<p class="sample" id="welcome">Hello, World!</p>
```

## Nuorodos

* [HAML – Github](https://github.com/haml/haml)


