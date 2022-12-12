{
  "date" : "2019-12-13",
  "keywords" :[ "MP3", "fájl", "kiterjesztés", "formátum", "Audio", "MPEG" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Ismerje meg az MP3 fájlformátumot és az API-kat, amelyek MP3 fájlokat nyithatnak meg és hozhatnak létre.",
  "title" :"MP3 - Audio fájl formátum",
  "linktitle" : "MP3",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2020-09-04"
}

## Mi az MP3 fájl?

Az .mp3 kiterjesztésű fájlok digitálisan kódolt fájlformátumok olyan hangfájlokhoz, amelyek formálisan az MPEG-1 Audio Layer III vagy MPEG-2 Audio Layer III szabványon alapulnak. A Moving Picture Experts Group (MPEG) fejlesztette ki, amely 3. rétegbeli hangtömörítést használ. Az MP3 fájlformátum által elért tömörítés a .WAV vagy .AIF fájlok méretének 1/10-e. A formátum előnyöket nyújt az ilyen hangfájlok interneten keresztüli streamelésében, és online hallgatáshoz, ami korábban nem volt lehetséges az audiofájlok nagy fájlmérete miatt. Az MP3 audiofájl hangminősége olyan paraméterbeállításokkal vezérelhető, mint a bitsebesség, a mintavételi sebesség, a közös vagy a normál sztereó.

## Az MP3 fájlformátum rövid története

Az MP3 formátumot egy német cég, a Fraunhofer-Gesellshart találta ki és fejlesztette ki. Az algoritmus licencelt szabadalmakkal rendelkezik az általa használt tömörítési technológiára. Íme egy praktikus MP3 idővonal:

• **1987** – A németországi Fraunhofer Intézet megkezdte a kiváló minőségű, alacsony bitsebességű hangkódolás kutatását. Az EUREKA projekt EU147, Digital Audio Broadcasting nevet kapta.

• **1988. január** – Megalakult a Moving Picture Experts Group (MPEG).

• **1989. április** – Fraunhofer szabadalmat kapott Németországban az MP3-ra.

• **1992** – Dieter Seitzer, aki segített a Fraunhofer kutatásában, integrálta hangkódolását MPEG-1-gyel.

• **1993** – Megjelent az MPEG-1 szabvány.

• **1994** – Az MPEG-2 szabványt kidolgozták, majd egy évvel később kiadták.

• **nov. 1996. 26.** – Kiadták az MP3 amerikai szabadalmát.

• **1998. szeptember** – Fraunhofer megkezdte a szabadalmi jogok érvényesítését. Aki az MP3 hangkódolást használta, licencdíjat fizetett a Fraunhofernek.

• **1999. február** – A SubPop, egy hanglemezcég MP3 formátumban terjesztett zenét, az első ilyen cég.

• **1999** – Megjelennek az első hordozható MP3-lejátszók.

## MP3 fájl formátum

Az MP3 fájl MP3 keretekből áll, ahol minden képkocka egy fejlécből és egy adatblokkból áll. A keretek nem függetlenek, és általában nem bonthatók ki tetszőleges kerethatárokon. A fájl adatblokkjai információt tartalmaznak a hangról frekvenciák és amplitúdók tekintetében. A fejlécben lévő szinkronizálási szó egy érvényes keret kezdetét azonosítja. Ezt követi 3 bit, ahol az első bit azt mutatja, hogy ez egy MPEG szabvány, a fennmaradó 2 bit pedig azt, hogy a 3. réteget használják; ezért MPEG-1 Audio Layer 3 vagy MP3. Ezt követően az értékek az MP3 fájltól függően eltérőek lesznek.

Az [ISO](https://en.wikipedia.org/wiki/International_Organization_for_Standardization)/[IEC](https://en.wikipedia.org/wiki/International_Electrotechnical_Commission) 11172-3 meghatározza az értéktartományt a fejlécet a fejléc specifikációival együtt. Manapság a legtöbb MP3-fájl [ID3](https://en.wikipedia.org/wiki/ID3) [metaadatokat](https://en.wikipedia.org/wiki/Metadata) tartalmaz, amely megelőzi vagy követi az MP3-kereteket, ahogy az ábrán látható. Az adatfolyam tartalmazhat egy opcionális ellenőrző összeget.

## Referenciák ##

* [MP3 – a Wikipedia által](https://en.wikipedia.org/wiki/MP3)

