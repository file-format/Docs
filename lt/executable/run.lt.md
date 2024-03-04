{
  "date" : "2023-01-31",
  "keywords" : ["run file", "what is a run file", "file", "how to open run file", "run file extension","extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Sužinokite apie RUN failo formatą ir API, kurios gali kurti ir atidaryti RUN failus.",
  "title" : "RUN failo formatas – Linux vykdomasis failas",
  "linktitle" : "RUN",
  "menu" : {
    "docs" : {
      "identifier":"executable-run-lt",
      "parent" : "executable"
}
},
  "lastmod" : "2023-01-31"
}

## Kas yra RUN failas?

.run failo formatas dažniausiai naudojamas platinant programinę įrangą arba taikomųjų programų diegimo programas Linux aplinkoje. Norėdami įdiegti programinę įrangą, turėsite padaryti failą vykdomąjį, o tai galite padaryti naudodami šią komandą:

```bash
chmod +x file_name.run 
```

Tada galite paleisti failą naudodami šią komandą:

```bash
./file_name.run 
```

Diegimo procesas gali skirtis priklausomai nuo konkretaus failo ir programos, kurią bandote įdiegti.

.run failo formatas yra apvalkalo scenarijaus tipas, naudojamas programinei įrangai ar taikomųjų programų diegimo programoms platinti Linux aplinkoje. Tai yra savarankiškas paketas, kuriame yra viskas, ko reikia programinei įrangai įdiegti, įskaitant dvejetainius failus, bibliotekas ir konfigūracijos failus.

Svarbu pažymėti, kad .run failuose taip pat gali būti kenkėjiško kodo, todėl prieš paleidžiant visada verta patikrinti failo šaltinį ir nuskaityti, ar nėra virusų.

Be to, kai kuriems .run failams paleisti ir įdiegti gali prireikti root teisių, todėl gali reikėti naudoti komandą sudo, kad paleistumėte failą su padidintais leidimais:

```bash
sudo ./filename.run
```

## Kaip atidaryti RUN failą?

Norėdami atidaryti .run failą, turite padaryti jį vykdomąjį, o tai galima padaryti su komanda chmod:

```bash
chmod +x filename.run 
```

Kai failas bus vykdomas, galite jį paleisti įvesdami:

```bash
./filename.run
```

Paleisti .run failą nėra tas pats, kas jį atidaryti teksto rengyklėje. Vykdant .run failą bus vykdomos jo instrukcijos, kurios gali būti bet kokios – nuo programos įdiegimo iki scenarijaus paleidimo. Norėdami peržiūrėti .run failo turinį, turite jį atidaryti teksto rengyklėje, pvz., nano arba vim:

```
nano filename.run
```
arba
```
vim filename.run
```

## Nuorodos
* [Kaip vykdyti .bin ir .run failus Ubuntu](https://vitux.com/how-to-execute-bin-and-run-files-in-ubuntu/)



