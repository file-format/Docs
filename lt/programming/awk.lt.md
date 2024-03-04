{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AWK failo formatas – AWK scenarijaus failas",
  "description":"Sužinokite apie AWK failo formatą ir API, kurios gali kurti ir atidaryti AWK failus.",
  "linktitle" : "AWK",
  "menu" : {
    "docs" : {
      "identifier" : "programming-awk-lt",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Kas yra AWK failas?

AWK failas yra scenarijaus failas, sukurtas teksto apdorojimo programai **AWK**, kuri pateikiama kartu su Unix ir Linux operacinėmis sistemomis. Jame yra loginių nurodymų, kaip atlikti veiksmus su tekstu ar failo turiniu, pvz., suderinti, pakeisti ir spausdinti tekstą. Tai padeda generuoti ataskaitas ir suformatuotą tekstą iš įvesties failo. awk programa dažniausiai yra /usr/bin/awk daugelyje Linux / unix paskirstymų.

## Kaip sukurti AWK scenarijų?

AWK failą galima sukurti arba atidaryti bet kuriame Linux / Unix OS teksto rengyklėje. Naują AWK scenarijaus failą galima sukurti taip.

```
$ vi script.awk
```

Tai atvers AWK failą teksto rengyklėje. Įveskite kai kuriuos teiginius teksto rengyklėje taip.

```
#!/usr/bin/awk -f
BEGIN { printf "%s\n","Writing my first Awk executable script!" }
```
Pirmoji šio teksto turinio eilutė paaiškinta taip.

 * \#! – vadinamas Shebang, kuris nurodo scenarijaus instrukcijų vertėją
 * /usr/bin/awk – yra vertėjas
 * -f – vertėjo parinktis, naudojama nuskaityti programos failą

## Kaip paleisti AWK scenarijų?

Išsaugokite failą ir padarykite scenarijų vykdytiną išleisdami žemiau esančią komandą:
```
$ chmod +x script.awk
```

Tada scenarijų galima paleisti taip.

```
$ ./script.awk
```

todėl gaunama tokia produkcija.

```
Writing my first Awk executable script!
```

## Nuoroda ##

* [Rašykite scenarijus naudodami Awk programavimo kalbą](https://www.tecmint.com/write-shell-scripts-in-awk-programming/)


