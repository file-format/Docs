{
  "date" : "2023-01-31",
  "keywords" :["rulați fișierul", "ce este un fișier de rulare", "fișierul", "cum se deschide fișierul de rulare", "extensia fișierului rulat", "extensia"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier RUN și despre API-urile care pot crea și deschide fișiere RUN.",
  "title" :"RUN File Format - Linux Executable File",
  "linktitle" : "RUN",
  "menu" : {
    "docs" : {
      "identifier":"executable-run",
      "parent" : "executable"
}
},
  "lastmod" : "2023-01-31"
}

## Ce este un fișier RUN?

Formatul de fișier .run este utilizat în mod obișnuit pentru distribuirea de programe de instalare sau aplicații în mediul Linux. Pentru a instala software-ul, va trebui să faceți fișierul executabil, ceea ce se poate face folosind următoarea comandă:

```bash
chmod +x file_name.run 
```

Apoi, puteți rula fișierul folosind următoarea comandă:

```bash
./file_name.run 
```

Procesul de instalare poate varia în funcție de fișierul și programul specific pe care încercați să îl instalați.

Formatul de fișier .run este un tip de script shell folosit pentru a distribui programe de instalare software sau aplicații în mediul Linux. Este un pachet autonom care include tot ceea ce este necesar pentru a instala software-ul, inclusiv fișiere binare, biblioteci și fișiere de configurare.

Este important să rețineți că fișierele .run pot conține și cod rău intenționat, așa că este întotdeauna o idee bună să verificați sursa fișierului și să o scanați pentru viruși înainte de a-l rula.

În plus, unele fișiere .run pot necesita privilegii de rădăcină pentru a rula și instala, așa că poate fi necesar să utilizați comanda "sudo" pentru a rula fișierul cu permisiuni ridicate:

```bash
sudo ./filename.run
```

## Cum se deschide fișierul RUN?

Pentru a deschide un fișier .run, trebuie să îl faceți executabil, ceea ce se poate face cu comanda "chmod":

```bash
chmod +x filename.run 
```

Odată ce fișierul devine executabil, îl puteți rula tastând:

```bash
./filename.run
```

Rularea unui fișier .run nu este același lucru cu deschiderea acestuia într-un editor de text. Rularea unui fișier .run va executa instrucțiunile acestuia, care ar putea fi orice, de la instalarea unui program până la rularea unui script. Pentru a vizualiza conținutul unui fișier .run, trebuie să îl deschideți într-un editor de text, cum ar fi nano sau vim:

```
nano filename.run
```
sau
```
vim filename.run
```

## Referințe
* [Cum se execută fișiere .bin și .run în Ubuntu](https://vitux.com/how-to-execute-bin-and-run-files-in-ubuntu/)


