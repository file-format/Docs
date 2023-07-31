{
  "date" : "2021-04-22",
  "keywords": [ "msix file", "extension", "format","how to open msix file","msix file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSIX - Ce este un fișier MSIX?",
  "description":"Aflați despre fișierele MSIX și API-urile care pot crea și deschide fișiere MSIX.",
  "linktitle" : "MSIX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## Ce este un fișier MSIX?

Un fișier MSIX este un format de ambalare a aplicației Windows care este utilizat pentru a crea și distribui aplicații în Windows 10. Acesta este formatul modern de fișier de pachet în comparație cu [APPX](/ro/programming/appx/) și MSI care vor fi eliminate în cele din urmă. la acest nou format de fișier. Poate fi folosit pentru implementarea aplicațiilor Win32, WPF și Windows Forms. Fișierele MSIX sunt fiabile și vizează optimizarea rețelei și a spațiului pe disc. Dezvoltatorii le folosesc pentru a distribui programe către utilizatorii finali prin Microsoft Store (cunoscut anterior ca Windows Store).

## Format de fișier MSIX - Mai multe informații

Fișierele MSIX sunt [ZIP](/ro/compression/zip/)-comprimate, cu toate fișierele incluse în fișierul ambalat. Pe lângă fișierele legate de aplicație, fișierul MSIX conține fișiere de configurare [.xml](/ro/web/xml/) care conțin informații legate de instalarea aplicației.

## Ce este în interiorul unui pachet MSIX?

Un pachet MSIX constă din următoarele fișiere.

* `AppxBlockMap.xml` - Cunoscut ca fișierul hartă a blocurilor de pachet, este un document XML care conține o listă de fișiere ale aplicației cu indici și hashuri criptografice pentru fiecare bloc de date care este stocat în pachet.
* `AppxManifest.xml` - Un document XML care conține informațiile necesare pentru implementarea, afișarea și actualizarea unei aplicații MSIX. Aceste informații includ identitatea pachetului, dependențele pachetului, capabilitățile necesare, elemente vizuale și puncte de extensibilitate.
* `AppxSignature.p7x` - Un fișier care este generat când pachetul este semnat. Toate pachetele MSIX trebuie să fie semnate înainte de instalare. Cu AppxBlockmap.xml, platforma este capabilă să instaleze pachetul și să fie validată.

## Referințe

* [Prezentare generală MSIX](https://learn.microsoft.com/en-us/windows/msix/overview)
* [Creați fișiere APPX utilizând Microsoft Visual Studio](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

