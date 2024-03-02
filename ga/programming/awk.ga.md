{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Formáid Comhaid AWK - Comhad Script AWK",
  "description":"Foghlaim faoi fhormáid comhaid AWK agus APIs ar féidir leo comhaid AWK a chruthú agus a oscailt.",
  "linktitle" : "AWK",
  "menu" : {
    "docs" : {
      "identifier" : "programming-awk-ga",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Cad is comhad AWK ann?

Is comhad scripte é comhad AWK a cruthaíodh don fheidhmchlár próiseála téacs **AWK** a thagann cuachta le córais oibriúcháin Unix agus Linux. Tá treoracha loighciúla ann chun gníomhartha a dhéanamh ar théacs nó ar ábhar comhaid ar nós téacs a mheaitseáil, a athsholáthar agus a phriontáil. Cuidíonn sé seo le tuarascálacha agus téacs formáidithe a ghiniúint ón gcomhad ionchuir. Is iondúil go mbíonn an áirgiúlacht awk suite in /usr/bin/awk ar fhormhór na ndáiltí linux/unix.

## Conas Script AWK a Chruthú?

Is féidir comhad AWK a chruthú nó a oscailt in aon eagarthóir téacs ar Linux/Unix OS. Is féidir comhad scripte AWK nua a chruthú mar seo a leanas.

```
$ vi script.awk
```

Osclóidh sé seo an comhad AWK in eagarthóir téacs. Cuir roinnt ráiteas isteach san eagarthóir téacs mar seo a leanas.

```
#!/usr/bin/awk -f
BEGIN { printf "%s\n","Writing my first Awk executable script!" }
```
Mínítear an chéad líne den ábhar téacs seo mar seo a leanas.

 * \#! – dá ngairtear `Shebang`, a shonraíonn ateangaire do na treoracha i script
 * /usr/bin/awk – is é an teangaire é
 * -f – rogha ateangaire, a úsáidtear chun clárchomhad a léamh

## Conas Script AWK a Fhorghníomhú?

Sábháil an comhad agus déan an script inrite tríd an ordú thíos a eisiúint:
```
$ chmod +x script.awk
```

Is féidir an script a rith ansin mar a leanas.

```
$ ./script.awk
```

a mbíonn an t-aschur seo a leanas mar thoradh air.

```
Writing my first Awk executable script!
```

## Tagairt ##

* [Scríobh Scripteanna Ag Úsáid Teanga Ríomhchlárúcháin Awk](https://www.tecmint.com/write-shell-scripts-in-awk-programming/)


