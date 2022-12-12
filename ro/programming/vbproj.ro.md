{
  "date" : "2019-10-11",
  "keywords" :[ "vbproj", "fișier", "extensie", "format fișier", "Fișier proiect VB", "Ghid de programare"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBPROJ",
  "description":"Aflați despre formatul de fișier VBPROJ și despre API-urile care pot crea și deschide fișiere VBPROJ.",
  "linktitle" : "VBPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Ce este un fișier VBPROJ?

Un fișier cu extensia .vbproj este un fișier de proiect Microsoft Visual Basic care este utilizat de motorul MSBuild al Microsoft pentru a construi proiectele într-o soluție Visual Studio. Este similar cu fișierul [CSPROJ](/ro/programming/csproj/) pentru proiectele .NET scrise în [C#](/ro/programming/cs/). Motorul MSBuild citește informațiile conținute în diferite grupuri din fișierele VBPROJ și generează fișierul de ieșire. Un fișier VBPROJ poate conține informații legate de identificatorii globali, clasele și proprietățile care definesc proiectul. Fișierele VBPROJ pot fi deschise și editate folosind Microsoft Visual Studio și orice editor de text obișnuit, cum ar fi Notepad pe sistemele de operare Windows și MacOS.

## Format de fișier VBPROJ - Mai multe informații

Fișierele VBPROJ sunt fișiere textuale care sunt scrise în format de fișier [XML](/ro/web/xml/) bazat pe [MSBuild XML Schema](https://docs.microsoft.com/en-us/visualstudio/msbuild/msbuild- proiect-file-schema-reference?view=vs-2019). Un fișier VBPROJ conține informații sub formă de etichete XML care definesc informații legate de acel grup special de setări. Este foarte recomandat să deschideți și să editați aceste fișiere de setare în Microsoft Visual Studio IDE.

### Elemente VBPROJ

Elementele constitutive ale unui fișier de setări VB sunt așa cum se arată în imaginea următoare.

{{< figure src="../vbproj.png" alt="Format de fișier VBPROJ" >}}

Următorul tabel oferă o scurtă descriere a acestor elemente.

|Element|Descriere|
---|---|
|Proiect| Element rădăcină al fiecărui fișier de proiect și poate include atribute pentru a specifica punctele de intrare pentru procesul de construire, pe lângă identificarea schemei XML pentru fișierul de proiect |
|Proprietăți și condiții| Proprietățile constau din perechi cheie-valoare și sunt definite într-un element PropertyGroup. Numele elementului de proprietate reprezintă cheia de proprietate, iar conținutul elementului definește valoarea proprietății.|
|Elementele și grupurile de articole|Elementele dintr-un fișier proiect sunt intrări în procesul de construire, cum ar fi fișiere-cod fișiere, fișiere de configurare, fișiere de comandă și altele necesare ca parte a procesului de construire. Elementele sunt și trebuie să fie definite într-un element ItemGroup.|
|Tinte și sarcini| Un element de sarcină reprezintă o instrucțiune de construcție individuală (sau sarcină). MSBuild include o multitudine de sarcini predefinite, cum ar fi Copy, CSC, VBC, Exec. Sarcinile trebuie să fie întotdeauna conținute într-un element `Target`, care este un set de una sau mai multe sarcini care sunt executate secvenţial, iar un fișier de proiect poate conține mai multe ținte.|

## Referințe

* [Înțelegerea fișierului de proiect](https://docs.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)
* [Elemente Schema MSBuild](https://docs.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019)

