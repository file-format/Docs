{
  "date" : "2019-12-12",
  "keywords" :[ "GLTF", "fișier", "extensie", "format", "3D", "Grupul Khronos 3D"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre fișierele GLTF și API-urile care pot crea și deschide fișiere GLTF.",
  "title" :"GLTF - Format fișier de transmisie GL",
  "linktitle" : "GLTF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier GLTF?

glTF (GL Transmission Format) este un format de fișier 3D care stochează informații despre modelul 3D în format JSON. Utilizarea JSON minimizează atât dimensiunea activelor 3D, cât și procesarea de rulare necesară pentru a despacheta și a utiliza aceste active. A fost adoptat pentru transmiterea și încărcarea eficientă a scenelor și modelelor 3D de către aplicații. glTF a fost dezvoltat de Khronos Group 3D Formats Working Group și este, de asemenea, descris ca [JPEG](/ro/image/jpeg/) al 3D de către creatorii săi.

Formatul de fișier GLTF definește un format de publicare extensibil, comun pentru instrumentele și serviciile de conținut 3D, care simplifică fluxurile de lucru de creație și permite utilizarea interoperabilă a conținutului în întreaga industrie. Intenția din spatele creării formatului de fișier glTF a fost de a defini un format de publicare extensibil și comun pentru instrumente și servicii de conținut 3D, care ar trebui să simplifice fluxurile de lucru de creație și să permită utilizarea interoperabilă a conținutului în întreaga industrie. Minimizează procesarea timpului de execuție de către aplicațiile care utilizează WebGL și alte API-uri.

## Scurt istoric al fișierului GLTF

Primele specificații pentru formatul de fișier glTF 1.0 au fost anunțate în octombrie 2015. Aceasta a venit ca o serie de eforturi începute în martie 2012 de către Khronos. Scopul acestor eforturi a fost de a evalua oportunitățile din jurul tracțiunii WebGL. În consecință, primul demo al formatului glTF, bazat pe formatul JSON a fost prezentat la întâlnirea WebGl din 2012. Formatul a fost adoptat de mai multe companii din când în când, inclusiv Cesium, 3D Tiles, Oculus, Microsoft, Archilogic și altele.

glTF 2.0 a fost publicat pe 5 iunie 2017 la Conferința Web3D 2017. Există o listă lungă de companii care au adoptat formatul de fișier glTF după aceea.

## Format de fișier GLTF

Specificațiile formatului de fișier pentru glTF 2.0 sunt disponibile [online](https://github.com/KhronosGroup/glTF/tree/master/specification/2.0) pentru referință și ar trebui consultate în orice implementare legată de citire/scriere pentru suport pentru format de fișier glTF.

glTF definește activele ca fișiere JSON cu date externe compatibile. Reprezintă modele 3D cu ajutorul:

* Descrierea completă a scenei conținută într-un fișier .glTF în format JSON, care include informații despre ierarhia nodurilor, materiale, camere, precum și informații despre descriptori pentru rețele, animații și alte construcții
* Fișiere binare (.bin) care conțin date de geometrie și animație și alte date bazate pe buffer
* Fișiere imagine ([.jpg](/ro/image/jpeg/), [.png](/ro/image/png/)) pentru texturi

Orice active externe, cum ar fi imaginile, sunt stocate în fișiere externe la care se face referire prin URI. Aceste URI-uri sunt stocate alături de containerul GLB sau încorporate direct în JSON folosind URI-uri de date. Fiecare glTF valid trebuie să specifice versiunea sa.

glTF a fost proiectat pentru a obține dimensiuni mici ale fișierului, încărcare rapidă, reprezentare completă a scenei 3D și extensibilitate. Aceste obiective unice de design sunt principalele motive pentru popularitatea formatului de fișier glTF în domeniul 3D. Următoarele sunt tipurile mime acceptate de formatul de fișier glTF pentru diferite tipuri de fișiere:

* Fișierele .gltf folosesc model/gltf+json
* Fișierele .bin folosesc aplicație/octet-stream
* Fișierele cu texturi folosesc tipul oficial de imagine/* bazat pe formatul de imagine specific. Pentru compatibilitate cu browserele web moderne, sunt acceptate următoarele formate de imagine: imagine/jpeg, imagine/png.

### Codificare JSON

glTF impune următoarele restricții suplimentare privind formatul fișierului JSON

Pentru a simplifica implementarea pe partea client, glTF are restricții suplimentare privind formatul și codificarea JSON.

1. JSON trebuie să utilizeze codificarea UTF-8 fără BOM.
1. Toate șirurile definite în această specificație (nume de proprietăți, enumerari) folosesc numai setul de caractere ASCII și trebuie scrise ca text simplu, de exemplu, „buffer” în loc de „"\u0062\u0075\u0066\u0066\u0065\u0072"`.
1. Numele (cheile) din obiectele JSON trebuie să fie unice, adică cheile duplicate nu sunt permise.

### URI-uri

Bufferele și resursele de imagine sunt referite prin intermediul URI-urilor. Următoarele două tipuri de URI trebuie să fie acceptate de clienți.

**URI-uri de date:** URI-urile de date sunt așa cum sunt definite de RFC 2397 și sunt utilizate de glTF pentru a încorpora resurse în JSON.

**Căi URI relative:** sau cale-noscheme așa cum este definită de RFC 3986, [Secțiunea 4.2](https://tools.ietf.org/html/rfc3986#section-4.2) — fără schemă, autorizare sau parametri. Caracterele rezervate trebuie să fie codificate în procente, conform RFC 3986, [Secțiunea 2.2](https://tools.ietf.org/html/rfc3986#section-2.2).

## Referințe ##

* [Specificații glTF 2.0 - Khronos](https://github.com/KhronosGroup/glTF)
* [Format de fișier glTF - După Wikipedia](https://en.wikipedia.org/wiki/GlTF)

