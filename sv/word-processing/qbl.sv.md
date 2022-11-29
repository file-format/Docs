{
  "date" : "2021-07-28",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QBL - QuickBooks License File",
  "description":"Läs mer om QBL-filformat och API:er som kan skapa och öppna QBL-filer.",
  "linktitle" : "QBL",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-07-28"
}

## Vad är QBL fil?

En fil med filtillägget .qbl är en QuickBooks-licensfil som innehåller licensinformation för användarens köpta kopia. Det lagras vanligtvis i det lokala systemet med namnet `license.qbl` efter att QuickBooks har installerats och användaren anger licensinformationen i programvaran när programvaran körs för första gången. QBL var det tidigare filformatet som användes för att lagra QuickBooks licensinformation. Denna har nu ersatts av QuickBooks `qbregisteration.dat`-fil och är fylld med information från användarens bekräftelsemail, köpta DVD eller på annat sätt. QBL-filer kan öppnas i alla textredigerare som Windows Notepad, Apple TextEdit, Notepad++, Github Atom editor och många fler.

## QBL-filformat - Mer information

QBL-filer skapas och lagras som vanliga textfiler. Informationen i dessa filer är läsbar för människor och kan redigeras/uppdateras när dessa filer öppnas i textredigerare. Licens- och användarregistreringsinformation kan sedan kopieras till den här filen för att komma igång med QuickBooks programvara. QBL-filer lagras vanligtvis i katalogen Program Files\Intuit\QuickBooks\INET på Windows operativsystem.

En QBL-fil innehåller två typer av information.

* `QuickBooks versionsinformation:` Avser den installerade versionen av QuickBooks och är i format som xx.x
* `Licensnyckel:` Text i 000-000 0000-0000-0000-000 000073adbf3f-format där 000-000 0000-0000-0000-000 ersätts med användarens qbregistration-nyckel

## Referenser

* [QuickBooks by Intuit](https://quickbooks.intuit.com/)
* [QuickBooks - Genererar filen qbregistration.dat](https://quickbooks.intuit.com/learn-support/en-us/license-information/create-or-re-create-the-qbregistration-dat-file/ 00/186082)

