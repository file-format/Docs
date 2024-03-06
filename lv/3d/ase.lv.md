{
  "date": "2021-01-22",
  "keywords": [
"ASE",
"failu",
"formātā",
"faila tips",
"pagarinājumu",
"kas ir ASE fails?"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par ASE failu formātu un API, kas var atvērt un izveidot ASE failus.",
  "title": "ASE — Autodesk ASCII ainas eksporta fails",
  "linktitle": "ASE",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-as-lve"
}
},
  "lastmod": "2021-01-22"
}

## Kas ir ASE fails?

A file with a .ase extension is an Autodesk ASCII Scene Export file format that is an ASCII representation of a scene, containing 2D or 3D information while exporting scene data using Autodesk. Autodesk provides options to include scene components while exporting scene data. You can include Mesh definition along with vertex and face information, Material description, transform animation data for the objects, complete mesh definition of every n frames, animation data for cameras and lights and IK joint settings.

## ASE faila formāts — vairāk informācijas

ASE faili ir ASCII formātā saglabāti teksta faili, kurus var atvērt jebkurā teksta redaktorā. ASE failā var būt šāda veida informācija, ko nodrošina Autodesk.

### Izvades opcijas

 * Acs definīcija — eksportē katra tīkla definīciju, tostarp informāciju par virsotnēm un ģeometrisko objektu virsotnēm. Turklāt, ieslēdzot šo opciju, tiek iespējoti vienumi grupas lodziņā Acs opcijas, kas aprakstītas tālāk.
 * `Materials` - Includes the material description. If a material is not assigned to an object, its wireframe color is exported. All levels of a material tree are included, so this can produce a lot of text.
 * Transformācijas animācijas atslēgas — ietver objektu transformācijas animācijas datus. Ja objekts ir mērķa kamera vai prožektors, tas ietvers mērķa animācijas datus.
 * Animated Mesh — eksportē pilnīgu tīkla definīciju katriem n kadriem. Frekvenci nosaka Controller Output spinner, kas aprakstīts tālāk. Katrs bloks satur to pašu informāciju, kas norādīta grupas lodziņā Mesh Options, kas aprakstīta tālāk. Ieslēdzot šo funkciju, var izveidoties milzīgs fails pat mazām ainām.
 * Animētas kameras/gaismas iestatījumi — eksportē kameru un apgaismojuma animācijas datus, piemēram, krāsu, intensitāti, kritumu, kartes novirzi utt. Izvada bloku ik pēc n kadriem, kā norādīts Controller Output spinner.
 * Inversie kinemātiskie savienojumi — eksportē IK savienojuma iestatījumus filiālē Hierarhija.

### Objektu veidi

Šeit esošie vienumi ļauj norādīt, kuru objekta kategoriju vēlaties iekļaut izvadē. Varat iekļaut ģeometriskus objektus, formas, kameras, gaismas un palīgobjektus.

 * Ģeometriski
 * Formas
 * Kameras
 * Gaismas
 * Palīgie

### Acs opcijas

 * `Mesh Normals` — eksportē sejas un virsotņu normas. Vispirms ir norādīts sejas normāls, kam seko trīs virsotņu normas, kas atbalsta seju. Ieslēdzot šo opciju, tiek izveidots daudz lielāks fails.
 * `Kartēšanas koordinātes` — eksportē kartēšanas virsotņu un seju sarakstu saskaņā ar TVert un TVFace struktūrām, kas aprakstītas 3ds Max programmatūras izstrādes komplektā. Ja objekts izmanto seju kartēšanu, tiek eksportēts seju karšu saraksts, kurā ir UVW koordinātas katrai sejai.
 * Vertex Colors — eksportē virsotņu krāsas.

### Kontrollera izeja

 * Izmantot atslēgas — eksportē atslēgu vērtības. Ja kontrolleris neizmanto taustiņus, tiek izmantota Force Sample metode. Transformācijas kontrolleru gadījumā opcija Use Keys darbojas tikai tad, ja visi transformācijas kontrolleri ir Lineāri/TCB vai Bezier. Ja vienā no transformācijas celiņiem tiek izmantots cita veida kontrolleris, visiem transformācijas celiņiem tiek izmantota Force Sample metode.
 * Force Samples” — paraugus kontroliera vērtībām, pamatojoties uz frekvenci, kas norādīta Frames per Sample Controller.

## Atsauces

 * [Autodesk — eksportēšana uz ASCII](https://help.autodesk.com/view/3DSMAX/2020/ENU/?guid=GUID-98B2388D-A3A7-4096-8E81-888A3F9D6069)

