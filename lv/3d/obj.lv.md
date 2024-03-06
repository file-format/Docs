{
  "date": "2019-10-11",
  "keywords": [
"obj fails",
"obj faila formātā",
"kas ir obj fails",
"failu",
"obj piemērs",
"obj faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OBJ faila formāts",
  "description": "Uzziniet par OBJ faila formātu un API, kas var atvērt un izveidot OBJ failus.",
  "linktitle": "OBJ",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-ob-lvj"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir OBJ fails?

**OBJ** failus izmanto Wavefront Advanced Visualizer lietojumprogramma, lai definētu un saglabātu ģeometriskos objektus. Ģeometrisko datu pārraide atpakaļ un uz priekšu ir iespējama, izmantojot OBJ failus. OBJ formātā tiek atbalstīta gan daudzstūra ģeometrija, piemēram, punkti, līnijas, faktūras virsotnes, virsmas, gan brīvas formas ģeometrija (līknes un virsmas). Šis formāts neatbalsta animāciju vai informāciju, kas saistīta ar gaismu un ainu novietojumu.

OBJ fails parasti ir 3D modelēšanas procesa galaprodukts, ko ģenerē CAD (Computer Aided Design). Noklusējuma secība virsotņu glabāšanai ir pretēji pulksteņrādītāja virzienam, izvairoties no skaidras sejas normālu deklarēšanas. Lai gan OBJ faili komentāra rindā deklarē mēroga informāciju, OBJ koordinātām nav deklarētas vienības.

## 3D OBJ formāta vēsture

Wavefront Technologies created OBJ file format for its Advanced Visualizer application to store geometric objects and 3D data. Its version 2.11 is superseded by a newly documented version 3. Faila formāts ir atvērts, un to ir ieviesuši citi pārdevēji savā 3D grafikas lietojumprogrammā. Wavefront Technologies saglabāja šo faila formātu atvērtā pirmkoda un neitrālu.

## OBJ faila formāts

3D objektos virsmas ģeometrijas kodēšana ir sarežģīts darbs, ko OBJ faila formāts paveica ļoti labi. Šis formāts ir diezgan daudzpusīgs, jo piedāvā vairākas izvēles iespējas virsmas ģeometrijas kodēšanai. Tālāk ir norādīti trīs atļautie formāti, kuriem ir savas priekšrocības un trūkumi:

### Teselācija ar daudzstūru virsmām

OBJ faila formāts ļauj lietotājam izveidot 3D modeļa virsmu, izmantojot vienkāršas vai sarežģītas ģeometriskas formas. Modeļa virsmas ģeometrijas kodēšanai failā tiek saglabātas katra daudzstūra virsotnes un normas. Lai gan teselācija palielina modeļa rupjību, tomēr ir jāatrod pareizais līdzsvars starp faila izmēru un tā drukas kvalitāti.

### Brīvas formas līkne

OBJ faila formāts ļauj lietotāja definētām brīvas formas virsmas līknēm norādīt modeļa virsmas ģeometriju. Tā kā brīvas formas līknes ir sarežģītākas nekā daudzstūra skaldnes, jo ar dažiem matemātiskiem parametriem izliektas līnijas vislabāk var noteikt ar brīvas formas līknēm. Tāpēc ar mazāku datu daudzumu, salīdzinot ar daudzstūrainu tēselāciju, brīvas formas līknes tiek izmantotas, lai ģenerētu jebkura 3D modeļa augstas kvalitātes kodējumu, nepalielinot faila lielumu.

### Brīvas formas virsmas

OBJ faila formāts nosaka arī virsmas ģeometrijas flīzēšanu ar brīvas formas virsmas ielāpiem. Šāda veida brīvas formas virsmas ielāpi (NURBS) ir ļoti piemēroti virsmām bez stingriem radiāliem izmēriem, piemēram, kravas automašīnas virsbūvei, helikoptera spārniem vai laivas korpusam. Brīvas formas virsmu izmantošana ir ļoti izdevīga, jo tās ir precīzākas, lai ar lielāku precizitāti saglabātu mazākus failu izmērus. Šīs virsmas ir būtiska aviācijas un automobiļu rūpniecības sastāvdaļa, kur zemā precizitāte ir nepielūdzama.

Tālāk norādītie atslēgvārdi ir sakārtoti pēc datu veida, lai definētu virsmas ģeometriju.


|Elementi|Brīvas formas līknes/virsmas korpusa paziņojumi|Brīvas formas līknes/virsmas atribūti
---|---|---|
|p|Punkts|parm|Parametru vērtības|deg|Grāds
|l|Line|trim|Ārējā apgriešanas cilpa|bmat|Pamata matrica
|f|Seja|caurums|Iekšējā apgriešanas cilpa|solis|Soļa izmērs
|curv|Curve|scrv|Īpaša līkne|cstype|Līknes vai virsmas veids
|līkne2|2D līkne|sp|Īpašs punkts|**Savienojamība un virsmu grupēšana**
|surf|Virsma|beigas|Beigu paziņojums|con|connect
|**Rādīt/renderēt atribūti**|g|Grupas nosaukums
|bevel|Slīpuma interpolācija|shadow_obj|Ēnu liešana|s|Izlīdzināšanas grupa
|lod|Detalizācijas līmenis|trace_obj|Ray tracing|mg|Apvienojama grupa
|d_interp|Izšķīdināt interpolāciju|ctech|Līknes tuvināšanas paņēmiens|o|Objekta nosaukums
|c_interp|Krāsu interpolācija|stech|Virsmas aproksimācijas tehnika|
|usemtl|Materiāla nosaukums|mtllib|Materiālu bibliotēka|
|**Ģeometriskās virsotnes**|
|v|Ģeometriskās virsotnes|vn|Vertex normals|
|vt|Tektūras virsotnes|vp|Parametru telpas virsotnes|

### Krāsa un tekstūra

OBJ fails ļauj saglabāt informāciju par krāsām un tekstūru saistītā faila formātā, ko sauc par materiālu veidņu bibliotēku (MTL). Daudzkrāsu ģeometriskie modeļi tiek renderēti, izmantojot šos divus failus kopā. MTL faili ir balstīti uz ASCII un atvieglo datora renderēšanu, aprakstot virsmas gaismu atstarojošās īpašības, izmantojot Phong atstarošanas modeli. Standartu ir pieņēmuši daudzi programmatūras pārdevēji, kuri izmanto tā priekšrocības materiālu apmaiņai. MTL formāts ir nedaudz novecojis, jo tam nav atbalsta jaunākajām tehnoloģijām, piemēram, spoguļkartēm un paralakses kartēm.

## Atsauces

* [Wavefront .obj fails](https://en.wikipedia.org/wiki/Wavefront_.obj_file)


