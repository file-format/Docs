{
  "date" : "2019-10-11",
  "keywords" :[ "yaml", ".yaml","ce este un fișier yaml","cum se deschide fișierul yaml", "extensie", "fișier", "fișier yaml","format de fișier yaml", "extensie .yaml" , "yaml vs json" ,"Exemplu de fișier YAML", "Exemplu de fișier docker yaml"],
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier YAML și despre API-urile care pot crea și deschide un fișier YAML.",
  "title" :"Format fișier YAML",
  "linktitle" : "YAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-05"
}

## Ce este un fișier YAML? ##

**Fișierul YAML** constă dintr-un limbaj YAML (YAML Ain't Markup Language) care este un limbaj de serializare a datelor bazat pe Unicode; folosit pentru fișierele de configurare, mesagerie pe internet, persistența obiectelor etc. YAML folosește extensia .yaml pentru fișierele sale. Sintaxa sa este independentă de un anumit limbaj de programare. Practic, YAML este conceput pentru interacțiunea umană și pentru a funcționa bine cu limbaje de programare moderne. Suportul pentru serializarea structurilor de date native arbitrare a crescut lizibilitatea fișierelor YAML, dar a complicat puțin procesul de analiză și generare a fișierelor.

## Scurt istoric ##

YAML a fost propus pentru prima dată în 2001 și a fost dezvoltat de Clark Evans, Ingy döt Net și Oren Ben-Kiki. S-a spus mai întâi că YAML înseamnă „un alt limbaj de marcare” pentru a indica scopul său ca limbaj de marcare. Ulterior a fost reutilizat ca „YAML Aint Markup Language” pentru a indica scopul său ca fiind orientat către date.


## Format de fișier YAML ##

Fișierul YAML este format din următoarele tipuri de date

- **Scalari**: Scalarii sunt valori precum șiruri de caractere, numere întregi, valori booleene etc.
- **Secvențe**: Secvențele sunt liste cu fiecare element care începe cu o cratimă (-). Listele pot fi, de asemenea, imbricate.
- **Mappings**: Maparea oferă posibilitatea de a lista cheile cu valori.

### Sintaxă ###

- **Spațiu alb**: Indentarea spațiului alb este folosită pentru a indica imbricarea și structura generală.

```yaml
nume: John Smith
a lua legatura:
domiciliu: 1012355532
birou: 5002586256
abordare:
strada: |
123 Aleea Tornadelor
Suita 16
oraș: East Centerville
stare: KS
```

- **Comentarii**: Comentariile sunt scrise începând cu simbolul „#”.

```yaml
# Acesta este un comentariu YAML
```

- **Liste**: Cratima (-) este folosită pentru a indica membrii listei cu fiecare membru pe o linie separată. Membrii listei pot fi, de asemenea, încadrați între paranteze drepte ([...]) cu membrii separați prin virgulă (,).

```yaml
  - A
  - B
  - C
```

```yaml
[A, B, C]
```

- **Associative Array**: O matrice asociativă este înconjurată de paranteze ({...}). Cheile și valorile sunt separate prin două puncte (:) și fiecare pereche este separată prin virgulă (,).

```yaml
  {name: John Smith, age: 20}
```

- **Șiruri**: Șirul poate fi scris cu sau fără ghilimele duble (") sau ghilimele simple (').

```yaml
șir de probă
„Șir de probă”
„Șir de probă”
```

- **Conținut bloc scalar**: conținutul scalar poate fi scris în notație bloc folosind următoarele:
  - **|**: All live breaks are significant.
  - **>**: Each line break is folded to space. It removes the leading whitespace for each line.

```yaml
date: |
YAML
(YAML nu este limbaj de markup)
este un limbaj de serializare a datelor
```

```yaml
date: ?
YAML (YAML nu este limbaj de markup)
este un limbaj de serializare a datelor
```

- **Documente multiple**: mai multe documente sunt separate prin trei cratime (---) într-un singur flux. Cratimele indică începutul documentului. Cratimele sunt, de asemenea, folosite pentru a separa directivele de conținutul documentului. Sfârșitul documentului este indicat prin trei puncte (...).

```yaml
  ---
Documentul 1
  ---
Documentul 2
...
```

- **Tip**: Pentru a specifica tipul valorii, se folosesc semne duble de exclamare (!!).

```yaml
a: !!float 123
b: !!str 123
```

- **Tag**: Pentru a atribui o etichetă unei note, se folosește un ampersand (&) și pentru a face referire la acel nod, se folosește un asterisc (*).

```yaml
nume: John Smith
facturare către: &id01
strada: |
123 Aleea Tornadelor
Suita 16
oraș: East Centerville
stare: KS

expediere la: *id01
```

- **Directive**: documentele YAML pot fi precedate de directive într-un flux. Directivele încep cu un semn de procent (%) urmat de nume și apoi de parametri separați prin spații.

```yaml
%YAML 1.2
  ---
Conținutul documentului
```
## Exemplu de fișier YAML
Aici puteți vedea un **exemplu de fișier docker yaml** mai jos:

```
topology:
database_node_name: docker_controller
docker_controller_node_name: docker_controller
self_service_portal_node_name: docker_controller
kvm_compute_node_names: kvm_compute1
docker_compute_node_names: docker_compute1
```

## YAML vs JSON
Practic, atât JSON, cât și YAML sunt dezvoltate pentru a oferi un format de schimb de date care poate fi citit de om. YAML este realizat ca un superset al formatului JSON. Înseamnă că putem analiza JSON folosind un parser YAML. Deși implementarea practică a acestei teorii este puțin complicată. Prin urmare, câteva diferențe de bază între YAML și JSON sunt prezentate mai jos:

|YAML| JSON|
---|---|
|Proces complex și consumator de timp de analizare a datelor serializate |Analizează rapid și ușor datele seriale JSON cu designul său mai simplu|
|Sprijin comunității mai puțin| Sprijin și popularitate mai mare ale comunității|
|Acceptă comentarii| Nu acceptă comentarii|
|Abilitatea de a utiliza referințele altor obiecte de date| Imposibil de serializat structuri complexe cu referințe la obiect|
|Ierarhia este indicată prin folosirea caracterelor cu spațiu dublu. Caracterele tabulatoare nu sunt permise|Obiectele și tablourile sunt notate între acolade și paranteze.|
|Gulimelele sunt opționale, dar acceptă ghilimele simple și duble.|Sirurile trebuie să fie între ghilimele duble.|
|Nodul rădăcină poate fi oricare dintre tipurile de date valide|Nodul rădăcină trebuie să fie fie o matrice, fie un obiect.|


## Referințe ##

- [YAML - Wikipedia](https://en.wikipedia.org/wiki/YAML)
- [YAML](https://yaml.org/spec/1.2/spec.html)

