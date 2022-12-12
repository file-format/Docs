{
  "date" : "2022-02-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WSDL File Format - Web Services Description Language File",
  "description":"Aflați despre ce este un fișier WSDL și API-urile care pot crea și deschide fișiere WSDL.",
  "linktitle" : "WSDL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-02-03"
}

## Ce este un fișier WSDL?

Un fișier WSDL este un fișier Web Services Description Language care este scris în limbaj XML pentru descrierea serviciilor Web. Conține informații despre punctele finale sau interfețele pentru conectivitate cu lumea exterioară într-un format universal acceptat. [Specificațiile formatului fișierului WSDL](https://www.w3.org/TR/2007/REC-wsdl20-20070626/) (menținute de W3C.org) definesc termenii pentru publicarea fluxurilor de date pentru schimbul de date pentru a avea acces de la distanță la aplicații prin porturi și puncte finale.

## Format de fișier WSDL - Mai multe informații

Fișierele WSDL sunt salvate ca fișiere XML care pot fi citite de om și pot fi deschise în orice editor de text pentru a vizualiza conținutul.

## Descrierea serviciului WSDL

Specificațiile de format de fișier WSDL 2.0 descriu serviciul WSDL ca fiind compus din două etape:

- Etapa abstractă
- Etapa de beton

Reutilizarea descrierii și a modelelor de preocupări independente este guvernată de un serviciu web. Acest lucru se realizează folosind mai multe tipuri diferite de elemente, inclusiv tipuri (definiții ale tipurilor de date), mesaje (datele comunicate), operațiuni (acțiuni) și protocoale utilizate de serviciu. Toate acestea sunt gestionate la nivel abstract. Legarea detaliilor de transport și formatul firului sunt specificate de legare, care grupează punctele finale pentru a implementa o interfață comună.

### Ce tehnologii pot fi utilizate pentru interfațarea cu serviciile WSDL?

Mai multe tehnologii diferite pot fi utilizate pentru interfațarea cu serviciile WSDL, inclusiv aplicațiile ASP.NET, C/C++ și Java.

## Exemplu WSDL

```
<message name="getTermRequest">
  <part name="term" type="xs:string"/>
</message>

<message name="getTermResponse">
  <part name="value" type="xs:string"/>
</message>

<portType name="glossaryTerms">
  <operation name="getTerm">
    <input message="getTermRequest"/>
    <output message="getTermResponse"/>
  </operation>
</portType>
```

În acest exemplu, portType „glossaryTerms” definește o operație unidirecțională numită „setTerm”.

## Referințe

* [WSDL XML](https://www.w3schools.com/xml/xml_wsdl.asp)
* [Specificații de format de fișier WSDL](https://www.w3.org/TR/2007/REC-wsdl20-20070626/)

