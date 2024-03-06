{
  "date": "2019-10-11",
  "keywords": [
"u3d fails",
"u3d faila formāts",
"kas ir u3d fails",
"failu",
"u3d piemērs",
"u3d faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "U3D — universāls 3D faila formāts",
  "description": "Uzziniet par U3D failu formātu un API, kas var atvērt un izveidot U3D failus.",
  "linktitle": "U3D",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-u3-lvd"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir U3D fails?

**U3D** (Universal 3D) is a compressed file format and data structure for 3D computer graphics. It contains 3D model information such as triangle meshes, lighting, shading, motion data, lines and points with color and structure. The format was accepted as[ ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) standard in August 2005. 3D [PDF](/pdf/) dokumenti atbalsta U3D objektu iegulšanu, un tos var skatīt programmā Adobe Reader (7. un jaunāka versija).

U3D formāts tika izstrādāts, ņemot vērā mērķi izveidot universālu standartu trīsdimensiju datu uzglabāšanai un apmaiņai. Tomēr šis formāts tiek galvenokārt izmantots 3D PDF kodēšanai, nevis kā apmaiņas formāts. Acrobat 3D konvertē atbalstīto 3D faila tipu U3D vai ĶTR pēc konvertēšanas PDF failā.

## U3D faila formāts

U3D files are in binary file format that underwent four editions as described by the [ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) reference document, resulting in specifications update with each edition. The PDF file standard ISO-32000 accepts U3D as allowed annotation and multimedia type.

Pirmais U3D izdevums bija vērsts uz galvenajiem 3D grafikas īpašību attēlojumiem, piemēram, ģeometriju, krāsām, faktūrām, apgaismojumu, kauliem un transformāciju balstītu animāciju. Otrais un trešais izdevums izlaboja dažas kļūdas pirmajā izdevumā, un trešā versija bija nozares programmatūrā visbiežāk izmantotais veids. Ceturtais izdevums sniedz definīcijas augstākas kārtas primitīviem (izliektām virsmām). [U3D specifications](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) ir pieejami tiešsaistē lietotāju uzziņai ECMA vietnē.

### Datu tipi U3D failos

Binārajā failā būs šādi veidi: U8, U16, U32, U64, I16, I32, F32, F64 un String.

 * U8: neparakstīts 8 bitu vesels skaitlis
 * U16: neparakstīts 16 bitu vesels skaitlis
 * U32: neparakstīts 32 bitu vesels skaitlis
 * U64: neparakstīts 64 bitu vesels skaitlis
 * I16: 16 bitu vesels skaitlis ar zīmi
 * F32: IEEE vienas precizitātes pludiņš.
 * F64: IEEE dubultās precizitātes pludiņš.
 * Virkne: virknes U3D failā sākas ar neparakstītu 16 bitu veselu skaitli, kas nosaka virknes rakstzīmju kopējo garumu. Virknes vienmēr tiek apstrādātas kā reģistrjutīgas.

## U3D faila struktūra

U3D fails satur bloku secību. Katrā U3D failā ir 3 dažādi bloku veidi.

 * Faila galvenes bloks
 * Deklarācijas bloks
 * Turpinājuma bloks

Ielādētājs nosaka bloka beigas, ja dati šajā blokā nav nepieciešami vai ja šim bloka veidam nav pieejams dekodētājs.

{{< figure src="../u3d.png" alt="U3D faila formāts" >}}

### Faila galvenes bloks
Faila galvenes bloks satur faila informāciju, ko ielādētais izmanto, lai noteiktu, kā lasīt failu.

### Deklarācijas bloks

Deklarācijas blokos ir informācija par failā esošajiem objektiem. Deklarācijas blokā esošie objekti ir jādefinē.

### Turpināšanas bloks

Papildu informācija par deklarāciju blokā deklarētajiem objektiem ir sniegta turpinājuma blokā. Katrs turpinājuma bloks ir jāsaista ar deklarācijas bloku.


## Atsauces Nr.

* [U3D faila formāts — Wikipedia](https://en.wikipedia.org/wiki/Universal_3D)

* [ECMA U3D faila formāta specifikācijas](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/)


