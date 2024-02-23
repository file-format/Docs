{
  "date" : "2023-01-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OSC - OpenStreetMap Modificați formatul fișierului",
  "description":"Aflați despre formatul de fișier OSC și despre API-urile care pot crea și deschide fișiere OSC.",
  "linktitle" : "OSC",
  "menu" : {
    "docs" : {
      "identifier":"gis-osc-ro",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-02"
}

## Ce este un fișier OSC?

Un fișier OSC este un format de fișier de modificare care conține date modificate ale hărții stradale pentru o hartă stradală .osm existentă. Conține informații despre modificările care urmează să fie aduse în [OSM file](/gis/osm/). Fișierul OSC poate avea trei tipuri posibile de operațiuni de modificare a datelor OSM și anume `inserare`, `modificare` sau `ștergere`. Aceste fișiere de modificare sunt utilizate în mod obișnuit pentru a exporta date din editorul OSM și pentru a le importa într-un alt editor.

Puteți deschide fișiere OSC cu software-ul Merkaartar și osmchange.

## Format de fișier OSC

Fișierele OSC sunt de obicei salvate în format de fișier JOSM, unde modificările sunt reprezentate de etichete. Începe cu eticheta `osmChange` care indică începutul fișierului. Sub-etichetele specifică dacă este o operație de inserare, modificare sau ștergere care urmează să fie efectuată pe nodul corespunzător din fișierul OSM. Conținutul unui nod conține de fapt conținutul unei etichete osm.

### Exemplu de format de fișier OSC

Următorul este un exemplu de operație de modificare pe un nod. Fiecare element trebuie să aibă un ID de set de modificări și un număr de versiune.

```
<osmChange version="0.6" generator="acme osm editor">
    <modify>
        <node id="1234" changeset="42" version="2" lat="12.1234567" lon="-8.7654321">
            <tag k="amenity" v="school"/>
        </node>
    </modify>
</osmChange>
```

## Referințe

* [Format de fișier JOSM](https://wiki.openstreetmap.org/wiki/JOSM_file_format)


