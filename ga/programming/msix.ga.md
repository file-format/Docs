{
  "date": "2021-04-22",
  "keywords": [
"comhad msix",
"síneadh",
"formáid",
"Conas a oscailt msix comhad",
"formáid comhaid msix"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MSIX - Cad is comhad MSIX ann?",
  "description": "Foghlaim faoi chomhad MSIX agus APIs is féidir comhaid MSIX a chruthú agus a oscailt.",
  "linktitle": "MSIX",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-msi-gax"
}
},
  "lastmod": "2021-12-16"
}

## Cad is comhad MSIX ann?

An MSIX file is a Windows app packaging format that is used to create and distribute applications in Windows 10. Seo an fhormáid chomhaid pacáiste nua-aimseartha i gcomparáid leis an [APPX](/programming/appx/) agus MSI a dhéanfar a chéimniú amach go dtí an fhormáid comhaid nua seo. Is féidir é a úsáid chun feidhmchláir Win32, WPF, agus Windows Forms a imscaradh. Tá comhaid MSIX iontaofa, agus leas iomlán a bhaint as spás líonra agus diosca. Úsáideann forbróirí iad seo chun cláir a dháileadh ar úsáideoirí deiridh tríd an Microsoft Store (ar a dtugtaí Windows Store roimhe seo).

## Formáid Chomhaid MSIX - Tuilleadh Eolais

Tá comhaid MSIX [ZIP](/compression/zip/)-chomhbhrúite, agus tá na comhaid go léir san áireamh sa chomhad pacáistithe. Chomh maith leis na comhaid a bhaineann leis an aip, tá comhaid cumraíochta [.xml](/web/xml/) sa chomhad MSIX ina bhfuil faisnéis a bhaineann le suiteáil na haipe.

## Cad atá taobh istigh de phacáiste MSIX?

Tá pacáiste MSIX comhdhéanta de na comhaid seo a leanas.

 * `AppxBlockMap.xml` - Ar a dtugtar an comhad léarscáile bloc pacáiste, is doiciméad XML é ina bhfuil liosta de chomhaid an aip le hinnéacsanna agus hashes cripteagrafach do gach bloc sonraí atá stóráilte sa phacáiste.
 * `AppxManifest.xml` - Doiciméad XML ina bhfuil an fhaisnéis atá riachtanach chun aip MSIX a imscaradh, a thaispeáint agus a nuashonrú. Áirítear leis an bhfaisnéis seo céannacht pacáiste, spleáchais pacáiste, cumais riachtanacha, gnéithe amhairc agus pointí insínteachta.
 * `AppxSignature.p7x` - Comhad a ghintear nuair a shínítear an pacáiste. Ní mór gach pacáiste MSIX a shíniú roimh a shuiteáil. Leis an AppxBlockmap.xml, tá an t-ardán in ann an pacáiste a shuiteáil agus a bhailíochtú.

## Tagairtí

 * [Forbhreathnú MSIX](https://learn.microsoft.com/en-us/windows/msix/overview)
 * [Cruthaigh comhaid APPX ag baint úsáide as Microsoft Visual Studio](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

