{
  "date": "2019-10-11",
  "keywords": [
"3DS",
"failu",
"formātā",
"faila tips",
"pagarinājumu",
"kas ir 3DS fails?"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par 3DS failu formātu un API, kas var atvērt un izveidot 3DS failus.",
  "title": "3DS faila formāts",
  "linktitle": "3DS",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-3ds"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir 3DS fails?

Fails ar paplašinājumu .3ds ir 3D Sudio (DOS) tīkla faila formāts, ko izmanto Autodesk 3D Studio. Autodesk 3D Studio ir bijis 3D failu formātu tirgū kopš 1990. gadiem, un tagad tas ir attīstījies līdz 3D Studio MAX darbam ar 3D modelēšanu, animāciju un renderēšanu. 3DS fails satur datus ainu un attēlu 3D attēlošanai, un tas ir viens no populārākajiem failu formātiem 3D datu importēšanai un eksportēšanai. Tajā tiek ņemta vērā tāda informācija kā kameru atrašanās vietas, tīkla dati, apgaismojuma informācija, skata loga konfigurācijas, izlīdzināšanas grupu dati, bitkartes atsauces un atribūti, lai izveidotu virsotnes un daudzstūrus ainas renderēšanai.

## 3DS faila formāts — vairāk informācijas
Pamatā 3DS ir binārs faila formāts, un tas seko iepriekš noteiktai struktūrai datu glabāšanai un izguvei. Binārais faila formāts nodrošina ātrāku 3DS faila formātu, kas ir mazāks, salīdzinot ar teksta failu formātiem. Dati 3DS failā tiek glabāti gabalos.

### 3DS gabals

Katrs gabals 3DS failā ir datu bloks, kas satur ID, bloka garumu nākamā bloka atrašanās vietai un pašus datus. Daļas ID ļauj 3DS failu formāta lasītājiem izlaist blokus, kurus tie neatpazīst. Tas arī palīdz formāta paplašināšanai. Katrā gabalā tiek glabāta informācija, kas saistīta ar formām, apgaismojumu un skatīšanās informāciju, kas kopā atveido ainu. Daļas ir sakārtotas hierarhiskā struktūrā 3DS failā, un tās attēlojumā atgādina XML dokumentu objektu koku.

**Chunk ID:** The first two bytes of a chunk represent a chunk identifier that lets the file reader decide whether to consider it during reading or skip i-lvt.

**Daļas garums:** gabala ID seko 4 baitu vesels skaitlis (mazā endianā), kas apzīmē gabala garumu. Šis garums ietver arī datu garumu, to apakšbloku garumu un 6 baitu galveni.

**Lietderīgā slodze:** gabala garumam seko faktiskie gabala datu baiti, kam seko tā apakšgabali tajā pašā hierarhiskā struktūrā, ko var paplašināt līdz vairākiem līmeņiem.

### Daļas struktūra

Vienkārša gabala hierarhiskā struktūra ir šāda:

**gabaliņš**

|sākums|beigas|izmērs|nosaukums
--- | --- | --- | ---
|0|1|2|Daļa ID
|2|5|4|Nākamais gabals

Gabaliem ir noteikta hierarhija, kas tiek identificēta pēc tā ID. 3ds failam ir primārā gabala ID 4D4Dh. Šī vienmēr ir pirmā faila daļa. Primārajā daļā ir galvenie gabali.

**Galvenie gabali**

|id|Apraksts
--- | ---
|3D3D|Objektu tīkla datu sākums.
|B000|Atslēgkadra datu sākšana.

Nākamā gabala rādītājs aiz ID bloka norāda uz nākamo galveno daļu.
Tieši aiz galvenā gabala ir vēl viens gabals. Tas varētu būt jebkura cita veida gabals, kas ir pieļaujams tās galvenajā gabalu darbības jomā.
For the Mesh description (3D3D) they could be any multiples of.

**3D3D apakšgrupas — acs bloks**


|id|Apraksts
--- | ---
|1100|nezināms
|1200|Fona krāsa.
|1201|nezināms
|1300|nezināms
|1400|nezināms
|1420|nezināms
|1450|nezināms
|1500|nezināms
|2100|Apkārtējās vides krāsu bloks
|2200|migla?
|2201|migla?
|2210|migla?
|2300|nezināms
|3000|nezināms
|4000|Objektu bloks
|7001|nezināms
|AFFF|nezināms

**4000 apakšgabali — objekta apraksta bloks**
Subchunk 4000 pirmais vienums ir objektu nosaukuma ASCIIZ virkne.
Atcerieties, ka objekts var būt siets, gaisma vai kamera.

|id|Apraksts
--- | ---
|4010|nezināms
|4012|ēna?
|4100|Trīsstūra daudzstūra objekts
|4600|Gaisma
|4700|Kamera

## Atsauces

* [Ģeometrijas failu formāti — Autodesk](https://help.autodesk.com/view/3DSMAX/2015/ENU/?guid=GUID-566E59EE-8221-4AC6-824B-5062C5AE0B32)

* [3DS — Wikipedia](https://en.wikipedia.org/wiki/.3ds)


