{
  "date" : "2023-08-07",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Shell-skripti - Kuinka käyttää sitä Ubuntussa ja Linuxissa",
  "description":"Opi mitä on Shell Script ja kuinka sitä käytetään Ubuntussa ja Linuxissa",
  "linktitle" : "SHELL SCRIPT",
  "menu" : {
    "docs" : {
      "identifier": "misc-shell-script-fi",
      "parent" : "misc"
}
},
  "lastmod" : "2023-08-07"
}

## Mikä on Shell Script?

Shell-komentosarjaan kuuluu komentosarjan kirjoittaminen tekstitiedostoon, jota usein kutsutaan **Shell-komentosarjaksi**. Nämä skriptit suorittaa komentotulkki, joka on komentorivitulkki. Yleisimmät kuoret sisältävät

1. Bash (Bourne Again SHell)
2. Zsh (Z Shell)
3. Kalastaa.

Shell-skriptit voivat vaihdella yksinkertaisista yksilinjaisista monimutkaisiin ohjelmiin, ja niitä käytetään monenlaisten tehtävien suorittamiseen, kuten tiedostojen käsittelyyn, järjestelmänhallintaan ja toistuvien tehtävien automatisointiin.

## Shell-komentosarjan edut:

1.  **Automaatio:** Shell-skriptien avulla käyttäjät voivat automatisoida toistuvia tehtäviä, mikä säästää aikaa ja vähentää inhimillisten virheiden mahdollisuutta.
    
2.  **Räätälöinti:** Käyttäjät voivat luoda erityistarpeisiinsa räätälöityjä komentosarjoja, jotka tarjoavat laajan mukauttamisen.
    
3.  **Eräkäsittely:** Shell-skriptit ovat erinomaisia eräkäsittelytehtävien käsittelyyn, joissa useita komentoja on suoritettava peräkkäin.
    
4.  **Järjestelmänhallinta:** Shell-komentosarjoja käytetään yleisesti järjestelmän hallintatehtäviin, kuten varmuuskopiointiin, lokien kiertoon ja ohjelmiston asennukseen.

## Yksinkertaisen Shell-skriptin kirjoittaminen:

Luodaan perus shell-skripti, joka tulostaa tervehdysviestin. Avaa tekstieditori ja luo tiedosto nimeltä greeting.sh. Lisää seuraavat rivit:

```
#!/bin/bash
# This is a simple shell script

echo "Hello, welcome to the world of shell scripting!"
```

Tallenna tiedosto ja tee siitä suoritettava suorittamalla seuraava komento terminaalissa:

```
chmod +x greeting.sh
```

Nyt voit suorittaa skriptin:

```
./greeting.sh
```

Tulosteen tulee olla:

```
Hello, welcome to the world of shell scripting!
```

## Shell-skriptien suorittaminen Ubuntussa ja Linuxissa:

Nyt keskustelemme **miten ajaa .sh-tiedosto Ubuntussa ja Linuxissa**.

1.  **Tee komentosarjasta suoritettava:** Varmista ennen komentosarjan suorittamista, että se on suoritettava. Käytä chmod-komentoa kuten aiemmin on esitetty.
    
2.  **Siirry komentosarjahakemistoon:** Avaa pääte ja käytä `cd`-komentoa navigoidaksesi komentosarjasi sisältävään hakemistoon.
    
3.  **Suorita komentosarja:** Suorita komentosarja kirjoittamalla terminaaliin `./scriptname.sh` ja korvaa scriptname komentosarjasi todellisella nimellä.
    
```
cd path/to/script
./greeting.sh
``` 

4.  **Bash-komennon käyttäminen:** Jos komentosarjasi alkaa #!/bin/bash-merkillä (tunnetaan nimellä **shebang**), voit suorittaa sen myös käyttämällä `bash'-komentoa.

```
bash greeting.sh
```

## Mitä $@ tarkoittaa Shell Scriptissa?

Shell-skriptissä $@ edustaa kaikkia komentoriviargumentteja, jotka lähetetään skriptille. Sitä käytetään usein viittaamaan argumenttien luetteloon erillisinä kokonaisuuksina. Kun sitä käytetään lainausmerkeissä, kuten `$@`, se säilyttää yksittäiset argumentit huomioiden välilyönnit ja erikoismerkit.

Tässä lyhyt selitys:

- `$@`: Edustaa kaikkia komentosarjalle tai funktiolle välitettyjä sijaintiparametreja (argumentteja). Jokaista argumenttia käsitellään erillisenä sanana.
    
- `$@`: Kun kirjoitetaan kaksoislainausmerkkeihin, se säilyttää argumenttien erottelun sallien välilyönnit tai erikoismerkit yksittäisten argumenttien sisällä.
    

Tässä on yksinkertainen esimerkki havainnollistamaan:

```
#!/bin/bash

# Save this script as example.sh

echo "The total number of arguments is: $#"
echo "The arguments are: $@"
echo "The arguments with double quotes are: \"$@\""
```

Kun suoritat tämän skriptin argumenteilla, esimerkiksi:

```
bash example.sh arg1 "argument 2" arg3
```

Se antaisi:

```
The total number of arguments is: 3
The arguments are: arg1 argument 2 arg3
The arguments with double quotes are: "arg1" "argument 2" "arg3"
```

Kuten näet, `$@` edustaa kaikkia argumentteja ja `$@` säilyttää yksittäiset argumentit, vaikka ne sisältävät välilyöntejä.

