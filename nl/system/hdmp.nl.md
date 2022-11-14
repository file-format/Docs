{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDMP-bestand - Windows Heap Dump-bestandsindeling",
  "description":"Meer informatie over het HDMP-bestandsformaat en API's die HDMP-bestanden kunnen maken en openen.",
  "linktitle" : "HDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## Wat is een HDMP-bestand?

HDMP-bestand is een niet-gecomprimeerde geheugendump wanneer een toepassing of programma crasht als gevolg van een fout. Het wordt alleen gemaakt door Windows XP/Vista en bevat een dump van de applicatiestatus toen het gecrasht was. Omdat ze niet zijn gecomprimeerd, nemen de HDMP-bestanden meer ruimte in op de schijf in vergelijking met de Minidump [MDMP](/nl/system/mdmp/)-bestanden die zijn gecomprimeerd voor rapportagedoeleinden.

Toepassingen die kunnen worden gebruikt om HDMP-bestanden te **openen** of te analyseren, zijn onder meer Microsoft Visual Studio met Debugging-tools voor Windows.

## HDMP-bestandsindeling

HDMP-bestanden worden op schijf opgeslagen als binaire bestanden en bieden geen enkel voordeel als ze worden geopend zonder geschikte toepassingen. Deze bevatten relevante systeemgegevens die zijn geregistreerd toen de fout optrad.

### Verschil tussen HDMP- en MDMP-bestandsindelingen

HDMP zijn niet-gecomprimeerde geheugendumpbestanden. MDMP daarentegen zijn minidumpbestanden die worden gecomprimeerd om de bestandsgrootte te verkleinen en naar Microsoft te verzenden om het probleem te melden.

## Referentie ##

* [DMP - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

