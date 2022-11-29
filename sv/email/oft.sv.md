{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFT - Microsoft Outlook e-postmallfil",
  "description":"Läs mer om OFT-filformat och API:er som kan skapa och öppna OFT-filer.",
  "linktitle" : "OFT",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en OFT fil?

Filer med filtillägget .oft är mallfiler som skapas med Microsoft Outlook. Den förformaterade layouten för meddelandemallar används sedan för att skicka ut e-postmeddelanden med vanlig information för att spara tid. Sådana filer kan skapas genom att skapa ett nytt e-postmeddelande, lägga till nödvändig information och sedan använda rullgardinsmenyn Spara som Office-mall (.oft) från Microsoft Outlook. Användare kan öppna OFT-filerna genom att dubbelklicka på dem och de öppnas i tillhörande applikation på det specifika systemet.

## OFT filstruktur ##

Filformatet .OFT använder filformatet [MSG](/sv/email/msg/) som bas. Den enda skillnaden är att OFT-filer har CLSID_TemplateMessage ({0006F046-0000-0000-C000-0000000000046}) som lagringsklass (WriteClassStg), medan MSG-filer använder CLSID_MailMessage ({0000000D000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000.

CFB_3-formatet är basen för MSG-filen. Paradigmet är baserat på lagrings- och strömningskoncepten, ganska nära kataloger och filer. Därför är en stor skillnad i den förra hela hierarkin, paketerad i en distinkt fil, kallad en sammansatt fil. Objekt utgör meddelandefilerna och består av en enskild egenskap eller dess samlingar. Denna förmåga underlättar applikationer att lagra intrikata, strukturerade data i en enda fil. Detta format specificerar också flera lagringar, varje lagring representerar meddelandeobjektet som en huvudkomponent. Dessa lagringar innehåller ett antal strömmar som representerar en egenskap hos den komponenten. Kapsling av förvaring är också möjlig.

### OFT-egenskaper

På den översta nivån av .msg-filen innehåller lagringar strömmar som lagrar egenskaper i dem. Egenskaper kan kategoriseras enligt följande:

* Fast längd egenskaper
* Variabel längd egenskaper
* Fastigheter med flera värden

Oavsett kategori är en egenskap antingen taggad eller namngiven. Lämplig mappningsinformation krävs dock för namngivna egenskaper som specificeras av deras mappningslagring.

### OFTA lagringar

Lagringar utgör nyckelkomponenterna i meddelandeobjektet. MSG-filformatet anger följande lagringar:

### Struktur på högsta nivå

Meddelandeobjekt representerar hela översta nivån i Msg-filformatet. Beroende på typ, egenskaper, antal mottagare och bilagaobjekt kan ett meddelandeobjekt ha olika strömlagringar i sin motsvarande .MSG-fil.

#### Relation med andra strukturer

MSG/OFT-filformatet har följande relationer till andra strukturer:

* Basen för .msg är Compound File Binary File Format.
* Egenskaperna som används av Message and Attachment Object Protocol används av detta format.

## Referenser

* [[MS-OXMSG]: Outlook MSG-filformat](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

