{
  "date" : "2019-10-11",
  "keywords" :[ "3DS","fil", "format", "filtyp", "tillägg","vad är en 3DS-fil?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om 3DS-filformat och API:er som kan öppna och skapa 3DS-filer.",
  "title" :"3DS filformat",
  "linktitle" : "3DS",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är 3DS fil?

En fil med filtillägget .3ds representerar 3D Sudio (DOS) mesh-filformat som används av Autodesk 3D Studio. Autodesk 3D Studio har funnits på marknaden för 3D-filformat sedan 1990-talet och har nu utvecklats till 3D Studio MAX för att arbeta med 3D-modellering, animering och rendering. En 3DS-fil innehåller data för 3D-representation av scener och bilder och är ett av de populära filformaten för import och export av 3D-data. Den tar hänsyn till information som kameraplatser, mesh-data, ljusinformation, visningsportkonfigurationer, utjämning av gruppdata, bitmappsreferenser och attribut för att skapa hörn och polygoner för att rendera en scen.

## 3DS-filformat - Mer information
I grunden är 3DS ett binärt filformat och följer en fördefinierad struktur för lagring och hämtning av data. Det binära filformatet möjliggör 3DS-filformatet snabbare mindre jämfört med textbaserade filformat. Data inuti en 3DS-fil lagras i form av bitar.

### 3DS Chunk

Varje bit i en 3DS-fil är ett datablock som innehåller ett ID, längden på blocket för platsen för nästa block och själva data. Chunk-ID:t låter 3DS-filformatsläsare hoppa över de block som de inte känner igen. Det hjälper också till att utöka formatet. Varje bit lagrar information relaterad till former, ljus och visningsinformation som tillsammans återger scenen. Bitar är ordnade i en hierarkisk struktur i en 3DS-fil och liknar XML Document Object-träd i representation.

**Chunk ID:** De första två byten av en bit representerar en bitidentifierare som låter filläsaren bestämma om den ska beaktas under läsningen eller hoppa över den.

**Längd på chunken:** Chunk ID följs av ett 4-byte heltal (i little-endian) som står för längden på chunken. Denna längd inkluderar även längden på data, längden på dess underblock och 6-byte-huvudet.

**Nyttlast:** Längden på chunken följs av faktiska bytes med data för chunken, följt av dess underklumpar i samma hierarkiska struktur som kan utökas till flera nivåer.

### Struktur av en bit

Den hierarkiska strukturen för en enkel bit är som visas nedan:

**En bit**

|start|slut|storlek|namn
--- | --- | --- | ---
|0|1|2|Chunk ID
|2|5|4|Nästa bit

Chunks har en hierarki påtvingad dem som identifieras av dess ID. En 3ds-fil har Primary chunk ID 4D4Dh. Detta är alltid den första biten av filen. Med i den primära biten är de viktigaste bitarna.

**Huvudklumpar**

|id|Beskrivning
--- | ---
|3D3D|Start av objektnätdata.
|B000|Start av nyckelframerdata.

Next Chunk-pekaren efter ID-blocket pekar på nästa Main chunk.
Direkt efter en Main chunk finns en annan chunk. Detta kan vara vilken annan typ av chunk som helst som är tillåten inom dess huvudsakliga räckvidd.
För Mesh-beskrivningen (3D3D) kan de vara vilka som helst multiplar av.

**Subchunks av 3D3D - Mesh Block**


|id|Beskrivning
--- | ---
|1100|okänd
|1200|Bakgrundsfärg.
|1201|okänd
|1300|okänd
|1400|okänd
|1420|okänd
|1450|okänd
|1500|okänd
|2100|Ambient Color Block
|2200|dimma?
|2201|dimma?
|2210|dimma?
|2300|okänd
|3000|okänt
|4000|Objektblock
|7001|okänd
|AFFF|okänt

**Subchunks of 4000 - Object Description Block**
Det första objektet i Subchunk 4000 är en ASCIIZ-sträng av objektets namn.
Kom ihåg att ett föremål kan vara ett nät, ett ljus eller en kamera.

|id|Beskrivning
--- | ---
|4010|okänd
|4012|skugga?
|4100|Triangulärt polygonobjekt
|4600|Ljus
|4700|Kamera

## Referenser

* [Geometry File Formats - Autodesk](https://knowledge.autodesk.com/support/3ds-max/learn-explore/caas/CloudHelp/cloudhelp/2015/ENU/3DSMax/files/GUID-566E59EE-8221-4AC6-824B-5062C5AE0B32-htm.html)
* [3DS - av Wikipedia](https://en.wikipedia.org/wiki/.3ds)
