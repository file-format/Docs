{
  "date" : "2023-08-07",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Script Shell - Conas é a rith ar Ubuntu agus Linux",
  "description":"Foghlaim faoi cad é Shell Script agus conas é a rith ar Ubuntu agus Linux",
  "linktitle" : "SHELL SCRIPT",
  "menu" : {
    "docs" : {
      "identifier": "misc-shell-script-ga",
      "parent" : "misc"
}
},
  "lastmod" : "2023-08-07"
}

## Cad é Shell Script?

Is éard atá i gceist le scripteáil bhlaosc ná sraith orduithe a scríobh i gcomhad gnáth-théacs, ar a dtugtar **Script Blaosc** go minic. Déanann sliogán na scripteanna seo, arb é ateangaire na n-orduithe é. Áirítear ar na sliogáin is coitianta

1. Bash (Bourne Again Shell)
2. Zsh (Z Shell)
3. Iasc.

Is féidir le scripteanna Blaosc raon ó línte aonlíne simplí go cláir chasta, agus úsáidtear iad chun raon leathan tascanna a dhéanamh, mar ionramháil comhad, riarachán córais, agus uathoibriú tascanna athchleachtacha.

## Buntáistí Shell Scripting:

1.  **Uathoibriú:** Ligeann scripteanna Shell d’úsáideoirí tascanna athchleachtacha a uathoibriú, rud a shábhálann am agus an seans go dtarlódh earráid dhaonna a laghdú.
    
2.  **Saincheapadh:** Is féidir le húsáideoirí scripteanna a chruthú atá oiriúnaithe dá sainriachtanais, ag soláthar ardleibhéal sainoiriúnaithe.
    
3.  **Baiscphróiseáil:** Tá scripteanna bhlaosc ar fheabhas chun tascanna próiseála baisc a láimhseáil, áit ar gá ilorduithe a fhorghníomhú in ord.
    
4.  **Riarachán Córais:** Úsáidtear scripteanna bhlaosc go coitianta le haghaidh tascanna riaracháin córais, amhail cúltacaí, rothlú loga, agus suiteáil bogearraí.

## Script Shell Simplí a Scríobh:

Cruthaímid script bhlaosc bunúsach a phriontálann teachtaireacht beannachta. Oscail eagarthóir téacs agus cruthaigh comhad darb ainm `greeting.sh`. Cuir na línte seo a leanas leis:

```
#!/bin/bash
# This is a simple shell script

echo "Hello, welcome to the world of shell scripting!"
```

Sábháil an comhad agus déan é inrite tríd an ordú seo a leanas a rith sa teirminéal:

```
chmod +x greeting.sh
```

Anois, is féidir leat an script a rith:

```
./greeting.sh
```

Ba cheart go mbeadh an t-aschur:

```
Hello, welcome to the world of shell scripting!
```

## Ag rith Scripteanna Shell ar Ubuntu agus Linux:

Anois, pléifimid **conas comhad .sh a rith in Ubuntu agus Linux**.

1.  **Déan an Script Inrite:** Sula ritheann tú script bhlaosc, cinntigh go bhfuil sé inrite. Úsáid an t-ordú `chmod` mar a thaispeántar níos luaithe.
    
2.  ** Téigh go dtí an Eolaire Scripteanna:** Oscail teirminéal agus úsáid an t-ordú `cd` chun dul chuig an eolaire ina bhfuil do bhlaosc script.
    
3.  **Rith an Script:** Rith an script trí `./scriptname.sh` a chlóscríobh sa teirminéal, agus ainm iarbhír do scripte a chur in ionad scriptname.
    
```
cd path/to/script
./greeting.sh
``` 

4.  ** Ag baint úsáide as an Ordú Bash:** Má thosaíonn do script le `#!/bin/bash` (ar a dtugtar **shebang**), is féidir leat é a rith leis an ordú `bash`.

```
bash greeting.sh
```

## Cad a chiallaíonn $@ i Shell Script?

Sa bhlaosc script, seasann `$@` do na hargóintí uile-orduithe a cuireadh ar aghaidh chuig an script. Is minic a úsáidtear é chun tagairt a dhéanamh do liostaí argóintí mar aonáin ar leith. Nuair a úsáidtear é laistigh de shleachta dúbailte, amhail `$@`, caomhnaíonn sé argóintí aonair, ag cur san áireamh spásanna agus carachtair speisialta.

Seo míniú gairid:

- `$@`: Léiríonn sé gach paraiméadair suímh (argóint) a chuirtear ar aghaidh chuig an script nó chuig an bhfeidhm. Caitear le gach argóint mar fhocal ar leith.
    
- `$@`: Nuair a dhéantar é a lua faoi dhó, caomhnaítear deighilt argóintí, ag ligean do spásanna nó carachtair speisialta laistigh d'argóintí aonair.
    

Seo sampla simplí le léiriú:

```
#!/bin/bash

# Save this script as example.sh

echo "The total number of arguments is: $#"
echo "The arguments are: $@"
echo "The arguments with double quotes are: \"$@\""
```

Nuair a ritheann tú an script seo le hargóintí, mar shampla:

```
bash example.sh arg1 "argument 2" arg3
```

Bheadh sé aschur:

```
The total number of arguments is: 3
The arguments are: arg1 argument 2 arg3
The arguments with double quotes are: "arg1" "argument 2" "arg3"
```

Mar a fheiceann tú, is ionann `$@` agus gach argóint, agus caomhnaíonn `$@` na hargóintí aonair, fiú má tá spásanna iontu.

