{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSG - Microsoft Outlook e-postformat",
  "description":"Läs mer om MSG-filformat och API:er som kan skapa och öppna MSG-filer.",
  "linktitle" : "MSG",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är MSG fil?

MSG är ett filformat som används av [Microsoft Outlook](https://products.office.com/en-us/outlook/email-and-calendar-software-microsoft-outlook?rtc#1) och Exchange för att lagra e-postmeddelanden , kontakt, möte eller andra uppgifter. Sådana meddelanden kan innehålla ett eller flera e-postfält, med avsändare, mottagare, ämne, datum och meddelandetext, eller kontaktinformation, mötesuppgifter och en eller flera uppgiftsspecifikationer. Egenskaperna som utgör Message-objektet, inklusive är också en del av MSG-filen. MSG-filen har rubriker, huvudmeddelandetext och hyperlänkar som vanlig ASCII-text. MSG-filer är också lämpliga med de program som behöver Microsofts Messaging Applications Programming Interface (MAPI).

## MSG-filstruktur

CFB_3-formatet är basen för MSG-filen. Paradigmet är baserat på lagrings- och strömningskoncepten, ganska nära kataloger och filer. Därför är en stor skillnad i den förra hela hierarkin, paketerad i en distinkt fil, kallad en sammansatt fil. Objekt utgör meddelandefilerna och består av en enskild egenskap eller dess samlingar. Denna förmåga underlättar applikationer att lagra intrikata, strukturerade data i en enda fil. Detta format specificerar också flera lagringar, varje lagring representerar meddelandeobjektet som en huvudkomponent. Dessa lagringar innehåller ett antal strömmar som representerar en egenskap hos den komponenten. Kapsling av förvaring är också möjlig.

## Mapi Properties

På den översta nivån av .msg-filen innehåller lagringar strömmar som lagrar egenskaper i dem. Egenskaper kan kategoriseras enligt följande:

* Fast längd egenskaper
* Variabel längd egenskaper
* Fastigheter med flera värden

Oavsett kategori är en egenskap antingen taggad eller namngiven. Lämplig mappningsinformation krävs dock för namngivna egenskaper som specificeras av deras mappningslagring.

## Förråd

Lagringar utgör nyckelkomponenterna i meddelandeobjektet. MSG-filformatet anger följande lagringar:

## Struktur på högsta nivå

Meddelandeobjekt representerar hela översta nivån i MSG-filformatet. Beroende på typ, egenskaper, antal mottagare och bilagaobjekt kan ett meddelandeobjekt ha olika strömlagringar i sin motsvarande .MSG-fil.

### Relation med andra strukturer

Msg-filformatet har följande relationer till andra strukturer:

* Basen för .msg är Compound File Binary File Format.
* Egenskaperna som används av Message and Attachment Object Protocol används av detta format.

## Scenarier för att undvika MSG-format

Meddelandeobjekt kan delas mellan klienter eller meddelandebutiker som använder .msg-filsystemet. Det finns få omständigheter där det inte är lämpligt att lagra ett meddelandeobjekt i .msg-filformatet. Till exempel:

* I händelse av att upprätthålla ett stort fristående arkiv är det bättre att använda ett fullfjädrat format där vyer kan återges mer exakt.
* Om mottagaren är okänd är det möjligt att formatet inte stöds av mottagaren och att privat eller irrelevant kan levereras.

## Exempel på MSG-fil

För att få en uppfattning om hur en MSG-fil ser ut kan du ladda ner en [exempel MSG-fil](https://products.conholdate.app/viewer/view/mL7cmq6qYbcNG329P/sample-msg-file.msg) och öppna på din dator för att se dess innehåll.

## Referenser

* [[MS-OXMSG]: Outlook MSG-filformat](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

