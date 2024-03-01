{
  "date": "2019-12-03",
  "keywords": [
"DOCX",
"tiedosto",
"muoto",
"tiedostotyyppi",
"laajennus",
"mikä on DOCX-tiedosto?"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DOCX",
  "description": "Opi DOCX-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata DOCX-tiedostoja.",
  "linktitle": "DOCX",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-doc-fix"
}
},
  "lastmod": "2019-12-03"
}

## Mikä on DOCX-tiedosto? ##

DOCX on tunnettu muoto Microsoft Word -asiakirjoille. Vuodesta 2007 alkaen Microsoft Office 2007:n julkaisun myötä tämän uuden asiakirjamuodon rakenne muutettiin tavallisesta binäärimuodosta XML- ja binääritiedostojen yhdistelmäksi. Docx-tiedostoja voidaan avata Word 2007:llä ja sivuversioilla, mutta ei aiemmilla MS Wordin versioilla, jotka tukevat DOC-tiedostotunnisteita.

## Lyhyt historia ##

After Microsoft opened the specifications for the DOC file format, it was easy for its competitors to reverse engineer the format and provide the same support in their own applications. In addition, the competition from Open Office in the form of its Open Document Format, compelled Microsoft to adopt more open and wide standards. It was in early 2000 when Microsoft decided to go for the change to accommodate the standard for **Office Open XML**. Documents under this new Standard were given [.docx extension](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd), the "X" being for XML. By 2007, this new file format became part of Office 2007 and is carried on in the new versions of Microsoft Office as well. The new file type has added advantages of small file sizes, fewer changes of corruption and well-formatted images representation.

## DOCX-tiedostomuodon tekniset tiedot – lisätietoja

Docx-tiedosto koostuu kokoelmasta XML-tiedostoja, jotka ovat ZIP-arkiston sisällä. Uuden Word-asiakirjan sisältöä voi tarkastella purkamalla sen sisältö. Kokoelma sisältää luettelon XML-tiedostoista, jotka on luokiteltu seuraavasti:

* MetaData Files - sisältää tietoja muista arkistossa olevista tiedostoista

* Asiakirja - sisältää asiakirjan todellisen sisällön


### Metatietotiedostot ###

Microsoft Word käyttää näitä tiedostoja tiedostojen välisen suhteen ja asiakirjan sisällön paikantamiseen. Kun Word-asiakirjaarkisto puretaan, se sisältää useita alla kuvattuja tiedostoja.

#### Suhteet - \_rels/.rels ####

Tämä tiedosto sisältää tietoja, jotka kertovat MS Wordille, mistä etsiä asiakirjan sisältöä ja muita viittauksia. Jokainen suhde tunnistetaan yksilöllisen suhdetunnuksen avulla ja määrittää kohteena olevan XML-tiedoston. Esimerkkisuhdetiedosto näytetään seuraavasti:

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"word/document.xml"/>.
```

#### Sisältötyypit ####

Asiakirja voi sisältää sisällä useita mediatyyppejä, kuten kuvia, teemoja, sanataidetta jne. [Content_Types].xml sisältää tietoja sellaisista asiakirjassa olevista mediatyypeistä. Tällaisen XML-tiedoston sisältö näytetään seuraavasti:

```
<Override PartName#"/word/document.xml" ContentType#"application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/>
```

#### Viittaukset resursseihin - \_rels/document.xml.rels ####

Tässä XML-tiedostossa viitataan tietoihin resursseista, kuten asiakirjaan upotetuista kuvista.

#### Pääasiakirjan sisältö ####

Tämä viittaa arkiston pääasialliseen XML-tiedostoon, joka sisältää asiakirjan tekstisisällön. Tätä sisältöä edustavat useat solmut OpenOffice XML -määritysten mukaisesti. Useimmiten tämän tiedoston sisältö koostuu kappaleista ja taulukoista, vaikka ne voivat olla myös muita solmuja.

### Tiedostomuotosolmut ###

Päädokumentti.xml-tiedosto on kokoelma solmuja, jotka edustavat tiedoston kokonaissisältöä. Jokaisella solmulla on alku ja loppu, jotka kapseloivat joko lisäsolmuja tai sisällön. Yksinkertaistettu esimerkki tällaisesta xml-tiedostosta on seuraava:

```
<w:document>
   <w:body>
       <w:p w:rsidR#"005F670F" w:rsidRDefault#"005F79F5">
           <w:r><w:t>Example Document</w:t></w:r>
       </w:p>
       <w:sectPr w:rsidR#"005F670F">
           <w:pgSz w:w#"12240" w:h#"15840"/>
           <w:pgMar w:top#"1440" w:right#"1440" w:bottom#"1440" w:left#"1440" w:header#"720" w:footer#"720"
                    w:gutter#"0"/>
           <w:cols w:space#"720"/>
           <w:docGrid w:linePitch#"360"/>
       </w:sectPr>
   </w:body>
</w:document>
```

Seuraavassa on tietoja joistakin DOCX-tiedoston sisältämistä solmuista sisällön esittämiseksi.

`<w:document> ` - Edustaa tiedoston pääsisällön juurielementtiä.

`<w:body> ` - Edustaa asiakirjan runkoa, joka voi sisältää monia muita elementtisolmuja, kuten kappaleita, taulukoita ja osia.

#### Kappaleet ####

Kappale on asiakirjan pääsisällön haltija. Sitä edustaa **<w:p> ** elementti asiakirjassa. Lisäksi kappale koostuu yhdestä tai useammasta ajosta **<w:r> ** joka sisältää kappaleen varsinaisen tekstin. Ajojen lisäksi kappaleet voivat sisältää myös muita asiakirjaelementtejä, kuten hyperlinkkejä, kommentteja jne. Esimerkki kappalerakenteesta on seuraavanlainen:

```
<w:p>
<w:pPr>
<w:pStyle> w:val#"MyStyle"/>
<w:spacing w:before#"120" w:after#"120"/>
</w:pPr>
<w:r>
<w:t xml"space#"preserve">A paragraph is main container in a document that further consists of a one or more runs where the text of paragraph is actually contained.</w:t>
</w:r>
</w:p>
```

## DOCX:n UKK

 * **Onko DOCX tiedostopääte?** - DOCX:ää käytetään tiedostopäätteenä edustamaan Microsoft Word 2007:ää ja uudempia Word-tiedostojen tallentamiseen käytettyjä tiedostomuotoja. Se myös kertoo käyttöjärjestelmällesi, että tämä DOCX-tiedosto vaatii Microsoft Word 2007:n avaamaan sen ja näyttämään sen kuvakkeen.
 * **Onko DOCX sama kuin Word** - DOCX on tiedostomuoto, jota Microsoft Word käyttää dokumenttien tallentamiseen Open XML -muodossa. Word puolestaan on Microsoft Officen sovellusohjelmisto, joka tukee myös muita tiedostomuotoja, kuten DOC, DOT, DOTM ja muita.
 * **Mitä eroa on DOC:lla ja DOCX:llä** - DOC on Word 2007:ssä ja aiemmassa tiedostomuodossa tallennettu Word-tiedosto. DOCX perustuu Open XML -tiedostomuotoon, jota Microsoft 2007 ja uudemmat versiot tukevat. Katso lisätietoja kohdasta [DOC:n ja DOCX:n erot](https://blog.fileformat.com/2022/08/11/doc-vs-docx/).

## Viitteet ##

* [MS - DOCX-tiedostomuoto](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd)

* [Office Open XML](http://officeopenxml.com/)


