{
  "date" : "2021-08-30",
  "keywords" :[ "fișier ipa", "format fișier ipa", "ce este un fișier ipa", "fișier", "exemplu ipa", "extensie fișier ipa", "extensie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier IPA și despre API-urile care pot crea și deschide fișiere IPA.",
  "title" :"IPA – fișierul pachet de aplicații iOS",
  "linktitle" : "IPA",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-30"
}

## Ce este un fișier IPA?
Un fișier cu extensia .ipa aparține iOS și este cunoscut ca fișier de pachet de aplicație. Acesta este un fișier de arhivă (comprimat utilizând compresia [ZIP](/ro/compression/zip/)) care stochează o aplicație iOS, dar acea aplicație poate fi instalată numai pe un dispozitiv iOS sau MacOS bazat pe ARM, cum ar fi un iPad, iPhone sau iPod Touch. În principal, iTunes, Apple Configurator 2 sau orice software terță parte pot fi folosite pentru a instala fișiere IPA.

## Format de fișier IPA
Dezvoltatorii IOS care dezvoltă aplicațiile folosind Apple Xcode sunt bine familiarizați cu fișierele IPA, deoarece trebuie să-și împacheteze aplicațiile dezvoltate ca fișiere IPA, fie pentru testarea în scopuri de implementare a magazinului de aplicații. Deși se știe că fișierele IPA sunt instalate ca aplicații iOS, totuși, le puteți decomprima și pentru a vizualiza datele aplicației conținute. Deoarece un fișier IPA conține un singur binar pentru arhitectura ARM a telefoanelor mobile și nu conține un binar pentru arhitectura x86, multe fișiere .ipa nu pot fi instalate pe iPhone Simulator.
### Structura unui fișier .ipa
Următorul exemplu arată structura unui IPA:

```
/Payload/
/Payload/Application.app/
/iTunesArtwork
/iTunesArtwork@2x
/iTunesMetadata.plist
/WatchKitSupport/WK
/META-INF
```
Cele de mai sus este o structură încorporată pe care iTunes și App Store o pot recunoaște. Conform acestei structuri:
- Directorul Payload conține toate datele aplicației.
- Fișierul iTunes Artwork este o imagine PNG de 512×512 pixeli, care conține pictograma aplicației pentru afișare în iTunes și în aplicația App Store pe iPad.
- iTunesMetadata.plist conține diverse informații, de la numele și ID-ul dezvoltatorului, informațiile privind drepturile de autor, identificatorul pachetului, numele aplicației, genul, data lansării, data achiziției etc.
- Dosarul META-INF conține doar metadate despre ce program a fost folosit pentru a crea IPA.


## Referințe

* [.ipa - de la Wikipedia](https://en.wikipedia.org/wiki/.ipa)


