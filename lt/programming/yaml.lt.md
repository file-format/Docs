{
  "date": "2019-10-11",
  "keywords": [
"yaml",
".yaml",
"kas yra yaml failas",
"kaip atidaryti yaml failą",
"pratęsimas",
"failą",
"yaml failą",
"yaml failo formatas",
".yaml plėtinys",
"yaml vs json",
"YAML failo pavyzdys",
"docker yaml failo pavyzdys"
],
  "author": {
    "display_name": "Muhammad Ahmad Chishti"
},
  "draft": "false",
  "toc": true,
  "description": " Sužinokite apie YAML failo formatą ir API, kurios gali sukurti ir atidaryti YAML failą.",
  "title": "YAML failo formatas",
  "linktitle": "YAML",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-yam-ltl"
}
},
  "lastmod": "2021-05-05"
}

## Kas yra YAML failas? ##

**YAML failą** sudaro kalba YAML (YAML Ain't Markup Language), kuri yra Unikodo duomenų serializavimo kalba; naudojamas konfigūracijos failams, internetiniams pranešimams, objektų išlikimui ir kt. YAML failams naudoja .yaml plėtinį. Jo sintaksė nepriklauso nuo konkrečios programavimo kalbos. Iš esmės, YAML yra sukurta žmonių sąveikai ir gerai dirbti su šiuolaikinėmis programavimo kalbomis. Savavališkų vietinių duomenų struktūrų nuoseklumo palaikymas padidino YAML failų skaitomumą, tačiau tai šiek tiek apsunkino analizavimo ir failų generavimo procesą.

## Trumpa istorija ##

YAML pirmą kartą buvo pasiūlyta 2001 m., o ją sukūrė Clark Evans, Ingy döt Net ir Oren Ben-Kiki. Pirmiausia buvo pasakyta, kad YAML reiškia dar vieną žymėjimo kalbą, kad būtų nurodyta jos kaip žymėjimo kalbos paskirtis. Vėliau ji buvo pervadinta į YAML Aint Markup Language, kad būtų nurodyta, kad ji yra orientuota į duomenis.


## YAML failo formatas ##

YAML failą sudaro šie duomenų tipai

– **Skaliarai**: skaliarai yra tokios reikšmės kaip eilutės, sveikieji skaičiai, loginiai skaičiai ir kt.
- **Sekos**: sekos yra sąrašai, kurių kiekvienas elementas prasideda brūkšneliu (-). Sąrašai taip pat gali būti įdėti.
- **Susivaizdavimas**: atvaizdavimas suteikia galimybę įtraukti raktus su reikšmėmis.

### Sintaksė ###

- **Tarpas**: tarpo įtrauka naudojama nurodyti lizdą ir bendrą struktūrą.

``` yaml
vardas: John Smith
kontaktas:
namai: 1012355532
biuras: 5002586256
adresas:
gatvė: |
123 Tornado alėja
Liukso numeris 16
miestas: East Centerville
valstybė: KS
```

- **Komentarai**: Komentarai rašomi pradedant simboliu #.

``` yaml
# Tai YAML komentaras
```

- **Sąrašai**: brūkšnelis (-) naudojamas sąrašo nariams nurodyti, kai kiekvienas narys yra atskiroje eilutėje. Sąrašo nariai taip pat gali būti pateikiami laužtiniuose skliaustuose ([...]), o nariai atskiriami kableliais (,).

``` yaml
  - "A"
  - "B"
  - "C"
```

``` yaml
[A, B, C]
```

- **Asociatyvinis masyvas**: asociatyvus masyvas yra apsuptas riestiniais skliaustais ({...}). Raktai ir reikšmės yra atskirtos dvitaškiu (:), o kiekviena pora atskiriama kableliu (,).

``` yaml
{vardas: Johnas Smithas, amžius: 20}
```

- **Eilutės**: eilutę galima parašyti su dvigubomis kabutėmis () arba viengubomis kabutėmis (') arba be jų.

``` yaml
Pavyzdinė eilutė
"Pavyzdinė eilutė"
Sample String
```

- **Skaliarinio bloko turinys**: skaliarinį turinį galima parašyti bloko žymėjimu naudojant šiuos veiksmus:
  - "**|**: visos tiesioginės pertraukos yra reikšmingos."
  - "**>**: kiekviena eilutės pertrauka perlenkiama į tarpą. Tai pašalina kiekvienos eilutės priekinį tarpą."

``` yaml
duomenys: |
YAML
(YAML nėra žymėjimo kalba)
yra duomenų serializavimo kalba
```

``` yaml
duomenys: ?
YAML (YAML nėra žymėjimo kalba)
yra duomenų serializavimo kalba
```

- **Keli dokumentai**: keli dokumentai viename sraute atskiriami trimis brūkšneliais (---). Brūkšneliai nurodo dokumento pradžią. Brūkšneliai taip pat naudojami atskirti direktyvas nuo dokumento turinio. Dokumento pabaiga žymima trimis taškais (...).

``` yaml
  ---
1 dokumentas
  ---
2 dokumentas
...
```

- **Tipas**: norint nurodyti reikšmės tipą, naudojami dvigubi šauktukai (!!).

``` yaml
a: !!plūduriuoti 123
b: !!str 123
```

- **Žyma**: norint užrašui priskirti žymą, naudojamas ampersandas (&), o norint nurodyti tą mazgą – žvaigždutė (*).

``` yaml
vardas: John Smith
sąskaitos gavėjas: &id01
gatvė: |
123 Tornado alėja
Liukso numeris 16
miestas: East Centerville
valstybė: KS

siuntimas į: *id01
```

- **Direktyvos**: prieš YAML dokumentus sraute gali būti pateiktos direktyvos. Direktyvos prasideda procento ženklu (%), po kurio nurodomas pavadinimas ir parametrai, atskirti tarpais.

``` yaml
%YAML 1.2
  ---
Dokumento turinys
```
## YAML failo pavyzdys
Toliau galite pamatyti **docker yaml failo pavyzdį**:

```
topology:
database_node_name: docker_controller
docker_controller_node_name: docker_controller
self_service_portal_node_name: docker_controller
kvm_compute_node_names: kvm_compute1
docker_compute_node_names: docker_compute1
```

## YAML prieš JSON
Iš esmės tiek JSON, tiek YAML yra sukurti taip, kad būtų užtikrintas žmogaus skaitomas duomenų mainų formatas. YAML yra realizuotas kaip JSON formato superrinkinys. Tai reiškia, kad galime išanalizuoti JSON naudodami YAML analizatorių. Nors praktinis šios teorijos įgyvendinimas yra mažai keblus. Todėl žemiau pateikiami kai kurie pagrindiniai YAML ir JSON skirtumai:

|YAML| JSON|
---|---|
|Sudėtingas ir daug laiko reikalaujantis nuosekliųjų duomenų analizės procesas |Greitai ir lengvai analizuokite JSON serijinius duomenis naudodami paprastesnį dizainą|
|Mažiau bendruomenės paramos| Didesnis bendruomenės palaikymas ir populiarumas|
|Palaiko komentarus| Nepalaiko komentarų|
|Gebėjimas naudoti nuorodas į kitus duomenų objektus| Neįmanoma suskirstyti sudėtingų struktūrų su objektų nuorodomis|
|Hierarchija žymima naudojant dvigubus tarpus. Tabukų simboliai neleidžiami|Objektai ir masyvai žymimi skliaustuose ir skliaustuose.|
|Eilutės kabutės yra neprivalomos, bet palaiko vienkartines ir dvigubas kabutes.|Eilutės turi būti su dvigubomis kabutėmis.|
|Šakninis mazgas gali būti bet kuris iš galiojančių duomenų tipų|Šakninis mazgas turi būti masyvas arba objektas.|


## Nuorodos Nr.

- [YAML - Wikipedia](https://en.wikipedia.org/wiki/YAML)
- [YAML](https://yaml.org/spec/1.2/spec.html)

