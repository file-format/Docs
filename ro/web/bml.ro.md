{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier BML - Fișier limbajul de marcare Bean",
  "description":"Aflați despre formatul de fișier BML și despre API-urile care pot crea și deschide fișiere BML.",
  "linktitle" : "BML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-12"
}

## Ce este un fișier BML?

Un fișier cu extensia .bml este un fișier Bean Markup Language care stochează clase Java pentru suportarea aplicațiilor Java. Acest lucru permite accesul la obiecte și metode Java și nu este necesar să se creeze noi funcționalități folosind clase Java. Specifică modul în care componentele sunt conectate între ele pentru a îndeplini sarcini utile. BML a fost dezvoltat de IBM alphaWorks pentru a descrie structurile și relațiile dintre componente. Fișierele BML pot fi deschise și vizualizate folosind orice editor de text, cum ar fi browsere web, Microsoft Notepad și Notepad++.

## Format de fișier BML

Site-ul web IBM alphaworks a oferit două implementări ale BML. Prima implementare este un interpret care „reda” un script BML pentru a genera ierarhia bean-ului dorită. A doua implementare este un compilator care compilează orice script BML în cod Java fără reflecție. Acest lucru este avantajos în sensul că permite capturarea structurii inter-componente a aplicației folosind un limbaj care este conceput pentru acest scop specific, cu capacitatea adăugată de a o compila în cod Java „obișnuit”.

## Etichete BML

Mai jos este o explicație a unora dintre etichetele utilizate în limbajul BML:

### Cel<bean> etichetă:

The<bean> elementul este folosit pentru a crea fasole noi sau pentru a căuta fasole după nume. The<bean> eticheta este de formatul:
```
<bean class = "classname or serialized file" [id = "name"]>
</bean>
```
„ID” din etichetă este asociat cu registrul de obiecte pentru JavaBean.

### Cel<string> etichetă

Există două moduri în care eticheta șir poate fi utilizată:

1. Pentru a crea un șir nevid:

```
<string [value = "value of string"]> [value of string]
</string>
```
2. Pentru a crea un șir gol:

```
<string/>
```
## Referințe

* [Mesajie orientată pe obiecte cu XML](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a86030/adx16nt5.htm)
* [Limbajul de marcare fizică](http://web.mit.edu/mecheng/pml/standards.htm)


