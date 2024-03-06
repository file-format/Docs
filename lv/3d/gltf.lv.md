{
  "date": "2019-12-12",
  "keywords": [
"GLTF",
"failu",
"pagarinājumu",
"formātā",
"3D",
"Khronos grupa 3D"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par GLTF failiem un API, kas var izveidot un atvērt GLTF failus.",
  "title": "GLTF — GL pārraides faila formāts",
  "linktitle": "GLTF",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-glt-lvf"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir GLTF fails?

glTF (GL Transmission Format) ir 3D faila formāts, kas saglabā 3D modeļa informāciju JSON formātā. JSON izmantošana samazina gan 3D līdzekļu lielumu, gan izpildlaika apstrādi, kas nepieciešama šo līdzekļu izpakošanai un lietošanai. Tas tika pieņemts efektīvai 3D ainu un modeļu pārraidei un ielādei lietojumprogrammās. glTF izstrādāja Khronos Group 3D formātu darba grupa, un tā veidotāji to arī raksturo kā 3D [JPEG](/image/jpeg/).

GLTF faila formāts definē paplašināmu, kopīgu publicēšanas formātu 3D satura rīkiem un pakalpojumiem, kas racionalizē autorēšanas darbplūsmas un nodrošina sadarbspējīgu satura izmantošanu visā nozarē. glTF faila formāta izveides nolūks bija definēt paplašināmu, kopīgu publicēšanas formātu 3D satura rīkiem un pakalpojumiem, kam vajadzētu racionalizēt autorēšanas darbplūsmas un nodrošināt sadarbspējīgu satura izmantošanu visā nozarē. Tas samazina izpildlaika apstrādi lietojumprogrammās, kuras izmanto WebGL un citas API.

## Īsa GLTF faila vēsture

The first specifications for glTF file format 1.0 were announced in October 2015. Tas notika kā virkne centienu, ko Khronos sāka 2012. gada martā. Šo centienu mērķis bija novērtēt WebGL vilces iespējas. Rezultātā 2012. gadā WebGl sanāksmē tika prezentēta pirmā glTF formāta demonstrācija, kuras pamatā ir JSON formāts. Šo formātu laiku pa laikam pieņēma vairāki uzņēmumi, tostarp Cesium, 3D Tiles, Oculus, Microsoft, Archilogic un citi.

glTF 2.0 tika publicēts 2017. gada 5. jūnijā Web3D 2017 konferencē. Ir garš uzņēmumu saraksts, kas pēc tam pieņēma glTF faila formātu.

## GLTF faila formāts

glTF 2.0 faila formāta specifikācijas ir pieejamas uzziņai [online](https://github.com/KhronosGroup/glTF/tree/main/specification/2.0), un tās ir jāskata jebkurā ieviešanā, kas saistīta ar lasīšanu/rakstīšanu, lai atbalstītu glTF faila formātu.

glTF definē līdzekļus kā JSON failus ar atbalsta ārējiem datiem. Tas attēlo 3D modeļus, izmantojot:

* Full scene description contained in a JSON-formatted .glTF file that includes information about node hierarchy, materials, cameras, as well as descriptor information for meshes, animations and other constructs
* Binārie faili (.bin), kas satur ģeometrijas un animācijas datus, kā arī citus bufera datus

* Attēlu faili ([.jpg](/image/jpeg/), [.png](/image/png/)) tekstūrām


Visi ārējie līdzekļi, piemēram, attēli, tiek glabāti ārējos failos, uz kuriem ir atsauces, izmantojot URI. Šie URI tiek glabāti kopā ar GLB konteineru vai iegulti tieši JSON, izmantojot datu URI. Katram derīgajam glTF ir jānorāda tā versija.

glTF ir izstrādāts, lai sasniegtu mazu faila izmēru, ātru ielādi, pilnīgu 3D ainas attēlojumu un paplašināmību. Šie unikālie dizaina mērķi ir galvenie iemesli glTF faila formāta popularitātei 3D domēnā. Tālāk ir norādīti mime veidi, ko atbalsta glTF failu formāts dažādiem failu tipiem:

* .gltf failos tiek izmantots modelis/gltf+json

* .bin faili izmanto lietojumprogrammu/octet-stream

* Tekstūras faili izmanto oficiālo attēla/* tipu, pamatojoties uz konkrēto attēla formātu. Lai nodrošinātu saderību ar mūsdienu tīmekļa pārlūkprogrammām, tiek atbalstīti šādi attēlu formāti: image/jpeg, image/png.


### JSON kodējums

glTF uzliek šādus papildu ierobežojumus JSON faila formātam

Lai vienkāršotu klienta puses ieviešanu, glTF ir papildu ierobežojumi JSON formātam un kodēšanai.

1. JSON ir jāizmanto UTF-8 kodējums bez MK.
1. Visas šajā specifikācijā definētās virknes (īpašību nosaukumi, enums) izmanto tikai ASCII rakstzīmju kopu, un tās ir jāraksta kā vienkāršs teksts, piemēram, buffer, nevis \u0062\u0075\u0066\u0066\u0065\u0072`.
1. Nosaukumiem (atslēgām) JSON objektos ir jābūt unikāliem, ti, atslēgu dublikāti nav atļauti.

### URI

Uz buferiem un attēla resursiem ir atsauces, izmantojot URI. Klientiem ir jāatbalsta šādi divi URI veidi.

**Datu URI:** Datu URI ir definēti RFC 2397, un tos izmanto glTF, lai iegultu resursus JSON.

**Relative URI Paths:** or path-noscheme as defined by RFC 3986, [Section 4.2](https://datatracker.ietf.org/doc/html/rfc3986#section-4.2) — without scheme, authority, or parameters. Reserved characters must be percent-encoded, per RFC 3986, [Section 2.2](https://datatracker.ietf.org/doc/html/rfc3986#section-2.2).

## Atsauces Nr.

* [glTF 2.0 specifikācijas — Khronos](https://github.com/KhronosGroup/glTF)

* [glTF faila formāts — Wikipedia](https://en.wikipedia.org/wiki/GlTF)


