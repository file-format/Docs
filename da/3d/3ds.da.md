{
  "date": "2019-10-11",
  "keywords": [
"3DS",
"fil",
"format",
"filtype",
"udvidelse",
"hvad er en 3DS fil?"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om 3DS-filformater og API'er, der kan åbne og oprette 3DS-filer.",
  "title": "3DS filformat",
  "linktitle": "3DS",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-3ds-da"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er 3DS fil?

En fil med filtypenavnet .3ds repræsenterer 3D Sudio (DOS) mesh-filformat, der bruges af Autodesk 3D Studio. Autodesk 3D Studio har været i 3D-filformatmarkedet siden 1990'erne og har nu udviklet sig til 3D Studio MAX til at arbejde med 3D-modellering, animation og gengivelse. En 3DS-fil indeholder data til 3D-repræsentation af scener og billeder og er et af de populære filformater til import og eksport af 3D-data. Den tager hensyn til oplysninger som kameraplaceringer, mesh-data, lysoplysninger, viewport-konfigurationer, udjævning af gruppedata, bitmap-referencer og attributter for at skabe hjørner og polygoner til gengivelse af en scene.

## 3DS-filformat - flere oplysninger
Som udgangspunkt er 3DS et binært filformat og følger en foruddefineret struktur til lagring og hentning af data. Det binære filformat muliggør 3DS-filformatet hurtigere og mindre sammenlignet med tekstbaserede filformater. Data inde i en 3DS-fil gemmes i form af bidder.

### 3DS Chunk

Hver del af en 3DS-fil er en datablok, der indeholder et ID, længden af blokken for placering af næste blok og selve dataene. Chunk-id'et lader 3DS-filformatlæsere springe de blokke over, som de ikke genkender. Det hjælper også med at udvide formatet. Hver del gemmer information relateret til former, belysning og visningsinformation, der tilsammen gengiver scenen. Chunks er arrangeret i en hierarkisk struktur i en 3DS-fil og ligner XML Document Object-træet i repræsentation.

**Chunk ID:** The first two bytes of a chunk represent a chunk identifier that lets the file reader decide whether to consider it during reading or skip i-dat.

**Klumpens længde:** Chunk-id'et efterfølges af et 4-bytes heltal (i little-endian), der står for stykkets længde. Denne længde inkluderer også længden af data, længden af dens underblokke og 6-bytes header.

**Nyttlast:** Længden af chunk er efterfulgt af faktiske bytes af data for chunken, efterfulgt af dens under-chunks i den samme hierarkiske struktur, der kan udvides til flere niveauer dybt.

### Struktur af en del

Den hierarkiske struktur af en simpel chunk er som vist nedenfor:

**En del**

|start|slut|størrelse|navn
--- | --- | --- | ---
|0|1|2|Chunk ID
|2|5|4|Næste del

Chunks har et hierarki pålagt dem, der er identificeret ved deres ID. En 3ds-fil har det primære chunk-id 4D4Dh. Dette er altid den første del af filen. Med i den primære chunk er de vigtigste chunks.

**Hovedstykker**

|id|Beskrivelse
--- | ---
|3D3D|Start af objektmaskedata.
|B000|Start af keyframer-data.

Next Chunk-markøren efter ID-blokken peger på den næste Main-chunk.
Direkte efter en Main chunk er en anden chunk. Dette kan være en hvilken som helst anden type chunk, der er tilladt inden for dens hovedchunk-omfang.
For the Mesh description (3D3D) they could be any multiples of.

**Understykker af 3D3D - Mesh Block**


|id|Beskrivelse
--- | ---
|1100|ukendt
|1200|Baggrundsfarve.
|1201|ukendt
|1300|ukendt
|1400|ukendt
|1420|ukendt
|1450|ukendt
|1500|ukendt
|2100|Ambient Color Block
|2200|tåge?
|2201|tåge?
|2210|tåge?
|2300|ukendt
|3000|ukendt
|4000|Objektblok
|7001|ukendt
|AFFF|ukendt

**Subchunks af 4000 - Objektbeskrivelsesblok**
Det første element i Subchunk 4000 er en ASCIIZ-streng af objektets navn.
Husk et objekt kan være et net, et lys eller et kamera.

|id|Beskrivelse
--- | ---
|4010|ukendt
|4012|skygge?
|4100|Trekantet polygonobjekt
|4600|Lys
|4700|Kamera

## Referencer

* [Geometri filformater - Autodesk](https://help.autodesk.com/view/3DSMAX/2015/ENU/?guid=GUID-566E59EE-8221-4AC6-824B-5062C5AE0B32)

* [3DS - af Wikipedia](https://en.wikipedia.org/wiki/.3ds)


