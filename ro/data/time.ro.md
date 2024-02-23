{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Fișier TIME - Ce este fișierul .time? Ora când fișierul a fost creat în Linux",
  "description" : "Aflați despre fișierul TIME și aflați Ora când fișierul a fost creat în Linux",
  "linktitle" : "TIME",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-time-ro",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Ce este un fișier TIME?

Formatul de fișier TIME a fost folosit de un sistem web numit LIGHT, care a ajutat utilizatorii să înregistreze, să organizeze și să-și împărtășească viața. În esență, a stocat o colecție de postări și a reprezentat un folder pe pagina de viață a utilizatorului în cadrul sistemului.

## Cum să aflați când a fost creat un fișier în Linux

În Linux, puteți folosi comanda `stat` pentru a afla când a fost creat un fișier. Iată cum o poți face:

Deschideți un terminal și tastați următoarea comandă:

```
stat <file_path>
```

Înlocuiește `<file_path> ` cu calea către fișierul care vă interesează. De exemplu:

```
stat /path/to/your/file.txt
```

Această comandă va afișa diverse informații despre fișier, inclusiv momentul creării acestuia. Căutați linia care începe cu Naștere” sau Fișier:”. Ora Nașterii” indică momentul în care fișierul a fost creat pe sistemul de fișiere.

Iată un exemplu despre cum ar putea arăta rezultatul:

```
  File: /path/to/your/file.txt
  Size: 1024       	Blocks: 8          IO Block: 4096   regular file
Device: 801h/2049d	Inode: 1643318     Links: 1
Access: (0644/-rw-r--r--)  Uid: ( 1000/   user)   Gid: ( 1000/   user)
Access: 2024-01-31 12:34:56.789012345 +0000
Modify: 2024-01-31 12:34:56.789012345 +0000
Change: 2024-01-31 12:34:56.789012345 +0000
 Birth: 2024-01-31 12:34:56.789012345 +0000
```

În acest exemplu, ora Nașterii” indică când a fost creat fișierul.

